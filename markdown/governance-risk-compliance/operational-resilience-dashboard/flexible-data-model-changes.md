---
title: Using the flexible data model
description: Starting with Operational Resilience, Release 21.0.x, the flexible data model enhances operational resilience metrics by improving data visualization and the flow of dependent services. It also supports multiple dashboards with insights into red flags, business service importance, and impact tolerance.
locale: en-US
release: zurich
product: Operational Resilience Dashboard
classification: operational-resilience-dashboard
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 8
breadcrumb: [Gathering data aligned with the CSDM setup, Manage, Operational Resilience, Governance, Risk, and Compliance]
---

# Using the flexible data model

Starting with Operational Resilience, Release 21.0.x, the flexible data model enhances operational resilience metrics by improving data visualization and the flow of dependent services. It also supports multiple dashboards with insights into red flags, business service importance, and impact tolerance.

Starting with Operational Resilience, Release 20.1.x, the Main node configurations, supported by the Data Relationships Framework, were introduced with Operational Resilience to define dependency roll-up chains. The Main node configurations, with the source being the OpRes CMDB, are shipped out-of-the-box. For information on the Main node configurations, creating a new Main node configuration, or updating an existing Main node configuration, see [Main node configurations: A component of the Data Relationships Framework](main-node-relationship-fw.md).

In the previous data model, the CSDM objects \[sn\_oper\_res\_profile\] table stored the entire dependency chain, including all possible combinations, making data retrieval cumbersome and maintenance challenging. This approach has been deprecated in favor of a more efficient model.

## Key features of the flexible data model

The flexible data model offers several key features that enhance operational resilience metrics.

-   Enhanced data visualization: The Services, Business services, Offerings, Business processes, and Application services modules now feature a vertical layout, replacing traditional horizontal tabs and enhancing navigation within the Operational Resilience Workspace. You can view the entire resilience metrics for an object, such as a business process or business service, from the Overview tab in the vertical layout.![Overview.](../image/sch-jobs-overview.png)

    You can then view the downstream data and various dashboards based on the selected top class. The following example shows the top controls to be strengthened for the business service.

    ![Top controls.](../image/top-controls-from-dashboard.png)

    Selecting the graph shows detailed information on the dependency records, related controls, control objectives.

    ![Details.](../image/top-controls-details.png)

-   Streamlined navigation: You can directly access related lists and metrics for a specific business service, such as its service offerings, business processes, application services, dependencies, incidents, and metrics from the vertical layout.

## Technical implementation

Starting with Operational Resilience, Release 21.0.x, the data model for operational resilience configurations has been optimized. Now, each node in a hierarchical chain, such as a business service to offering to processes, is stored separately in the \[sn\_oper\_res\_profile\] CSDM objects table along with its class and parent nodes. This means that only relevant objects \(for example, 500 out of 1,000 entities\) that are part of main node configurations are stored, improving data management efficiency.

The flexible data model introduced with Operational Resilience, Release 21.0.x provides a foundation for the dashboards and tracks the flow of dependent services. The data, including red flags by type, such as failed controls, incidents, and outages, and business service metrics such as number of flags, importance, and impact tolerance, is updated in the dashboard through changes to the flexible data model.

![Dashboard data.](../image/dashboard-data.png)

The data shown in the example is for business services such as business service by number of red flags, business service by importance, business service by impact tolerance. You can configure the **sn\_oper\_res.top\_class\_name** property to designate any class as the top class.

## Configuring the sn\_oper\_res.top\_class\_name property

You can configure the **sn\_oper\_res.top\_class\_name** property to designate any class as the top class in the dashboard view so that any node, such as business service, business process, or application service, can be the top node. You can then view the downstream data and various dashboards based on the selected top class, such as the number of application services that are under a business service. It enables you to switch between different views, such as business services, service offerings, business processes, or applications, on the dashboard and view relevant data accordingly.

For example, if the data is displayed for a business service, you can change the top class to service offerings, business processes, or application services by configuring the **sn\_oper\_res.top\_class\_name** property. You can then change the top class to another object and the system shows data with respect to that specific top class. This property is applicable only for the dashboards and not for the Workspace forms. For more information on the properties, see [Configure Operational Resilience properties](../task/configure-opres-prop.md).

The following example shows that the top class name is set to **cmdb\_ci\_service\_business**.

![Name.](../image/top-class-name.png)

You can modify the property value to represent a service offering or application, and the dashboard will populate with the corresponding data. The following example demonstrates how to update the top class name to "service offering."

![Name change.](../image/top-class-property-name.png)

Based on the updated property name, data for service offering is displayed in the Operational Resilience dashboard as shown in the example.

![Dashboard.](../image/top-class-dashboard.png)

## Calculation and roll-up of red flags

When the **Calculate red flags for CSDM and dependencies** scheduled job is executed, the red flags data is populated in the dashboard. The dashboard in the following example displays a range of 1-30 red flags in the "Business service by number of red flags" section.

![Dashboard data.](../image/dashboard-data.png)

Selecting the card shows a detailed breakdown for the business service. It shows a total of 24 red flags, with 3 specifically attributed to the "Cards and payments" service. The following illustration shows the roll-up functionality, which aggregates the red flags for the entities associated with the selected "Cards and Payments" business service, providing a hierarchical view of the data.

![red flags.](../image/red-flags-breakup.png)

The value "24" shown in the Total red flags count column is the roll-up value of the red flags for all entities under the "Cards and Payments" business service.

## CSDM objects table

In the CSDM objects \[sn\_oper\_res\_profile.list\] table, the following columns are displayed:

-   The Impacted objects column displays the parent objects.
-   The Impacted objects classes column shows the classes.
-   The Red flags count column indicates the number of the red flags that are directly assigned to a node.
-   The Total red flags count column displays the total count of the red flags directly assigned to a node and its children as shown in the table.

![CSDM objects table.](../image/csdm-objects-table.png)![Data in the table.](../image/sch-job-1-output.png)

The object classes displayed in the Object class column in the example provide a clear representation of various entities, including business applications and processes. This data is then fed into the system using fix scripts, ensuring that the information is accurately populated and up-to-date. By using these scripts, the system can effectively display and manage the complex relationships between different object classes.

You can group the objects with respect to their object classes. Then you can the object classes for service offerings, core company, business processes, and so on.

![Object classes.](../image/obj-class.png)![Grouped classes.](../image/obj-class-2.png)

The upstream impacted objects for a specific object class are added to the Impacted objects column. For example, the Java Application Server FLX has upstream impacted objects such as digital banking process and inbound payment, which get added and are shown in the Impacted objects column.

![Classes.](../image/object-classes.png)

This process starts with the lowest level object and includes the level above it, populating the impacted objects. The data is then directly integrated into the main node configurations.

## Main node configurations

The Main node configurations provide the data flow of what you want to see. The following Main node configurations, with the source being the OpRes CMDB, are shipped out-of-the-box:

-   Business process to dependencies
-   Business service to dependencies
-   Opres with CSDM header
-   Service \(CMDB\)
-   Service offering to dependencies

![Menu.](../image/main-node-menu.png)

The entire flow that goes from a business service to business process to service offering and then to an application is created in the Main node configurations and then the configurations are mapped to the impacted objects.

For information on setting up the Main node configurations, see [Configure the Main node configurations](../task/set-up-main-node.md).

## Running the scheduled jobs

Two scheduled jobs, **Update CSDM and other dependencies** and **Calculate red flags for CSDM and dependencies** run at regular intervals populate data in the CSDM objects \[sn\_oper\_res\_profile.list\] table and the red flags. For more information, see [Execute the scheduled jobs](../task/execute-sch-jobs.md).

All the Main node configurations are handled in parallel. A separate event is triggered for each Main node configuration, enabling parallel processing. The enhanced configuration eliminates the need for sequential processing, significantly improving efficiency.

![Scheduled job.](../image/sch-job-1.png)

After running the **Update CSDM and other dependencies** scheduled job, the data is fetched into the CSDM Objects table. Dependencies are updated for the objects and are shown in the modules.

![Service form.](../../grc-operational-res-ws/image/tabs-business-service-view.png "Service form")

![Record form.](../../grc-operational-res-ws/image/tabs-business-service-view-2.png)

Previously, traversing many-to-many tables to find related records was time-consuming. Now, by storing impacted objects in the table itself, you can directly retrieve related records from a single column, eliminating the need for recursive hierarchy creation, improving efficiency significantly.

Dependencies are fetched from the Entity \[sn\_grc\_profile\] \(many-to-many\) table first. When you run the **Calculate red flags for CSDM and other dependencies** scheduled job, the red flags data is fetched and rolled up according to the configured settings.

After the scheduled job is completed, the Main node configurations are no longer required. The dashboard uses the top class property to traverse the red flags staging table and retrieve downstream red flags that match the specified record type, such as business service or service offering, and so on.

![Red flags.](../image/sch-job-2.png)

The following example shows that Incident SO1 - VM is rolled up from SO1.

![Rolled up data.](../image/sch-job-2-output.png)

Failed controls from business processes and service offerings are rolled up and shown in the modules.

![Failed controls.](../image/sch-job-2-output-2.png)

