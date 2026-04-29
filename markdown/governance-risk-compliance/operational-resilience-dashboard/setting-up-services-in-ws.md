---
title: Data setup for business services
description: Operational Resilience managers typically verify that data is set up for services or business services and monitor their resilience metrics on the dashboard. The Service \(CMDB\) Main node configuration fetches service-related data, while the Opres with CSDM header Main node configuration sets up the business services-related data.
locale: en-US
release: australia
product: Operational Resilience Dashboard
classification: operational-resilience-dashboard
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Gathering data aligned with the CSDM setup, Managing Operational Resilience, Operational Resilience, Governance, Risk, and Compliance]
---

# Data setup for business services

Operational Resilience managers typically verify that data is set up for services or business services and monitor their resilience metrics on the dashboard. The Service \(CMDB\) Main node configuration fetches service-related data, while the Opres with CSDM header Main node configuration sets up the business services-related data.

## Business services overview on the dashboard

A service performs a business-level function, such as email, IT services, e-commerce, or telephone banking. Existing customers use the Service \(CMDB\) Main node configuration, while new customers use the OpRes with CSDM header Main node configuration. The Service form or the business services form list risks, issues, control failures, and other areas that require attention.

**Note:** Administrators can show or hide the **Services overview** or **Business services overview** tabs based on their organizational needs. For more information, see [Show Business services overview tab in Workspace view](../../grc-operational-res/concept/displaying-services-overview-tab.md).

## Setup of entity types and pillars

Before proceeding, ensure that entity types and pillars are properly configured; refer to the [Setting up pillars, entity types, entity filters, and entities](../../grc-operational-res/concept/setting-up-hierarchy.md) for setup instructions.

## Vertical layout for Service records

Beginning with Operational Resilience, Release 21.0.x, records in the Services, Business services, Offerings, Business processes, and Application services modules feature a vertical layout.

The vertical layout within the Operational Resilience Workspace eliminates the need for horizontal tabs. Instead, it maps the business services, offerings, business processes, and application services to organize related information in a more streamlined manner.

When viewing a specific business service, such as "Cards and Payments," all dependent lists are accessible through this vertical menu. This includes service offerings, business processes, application services, dependencies, incidents, and relevant metrics. The new layout allows users to directly access related information, streamlining navigation and improving the overall user experience.

This layout displays detailed information, including service dependencies, events, red flags data, and related issues, making it easier to read and understand.

![Vertical layout for a business process.](../../grc-operational-res/image/ver-layout-bp.png)

## Assigning the itil user role to the Operational Resilience administrators or managers

To configure child services or processes for a service, assign the itil user role to Operational Resilience administrators or managers in the following steps.

![Assign the itil user role-step-1.](../image/itil-role-to-manager-1.png "Assign the itil user role")

![Assign the itil user role.](../image/itil-role-to-manager-2.png "Assign the itil user role-step-2")

**Note:**

To add or remove services and processes in the Operational Resilience Workspace, you must have the sn\_oper\_res.manager and itil role or the sn\_oper\_res.admin and itil roles. In the CMDB, granting the itil role allows users to add or remove services and processes from the backend. However, the Operational Resilience Workspace application prevents users with the sn\_oper\_res.user role from making these changes in the Operational Resilience Workspace.

## Adding a service to reporting

You can add a service to Operational Resilience reporting by selecting the **Add to OpRes reporting** UI action as shown in the following example.

**Note:** Instead of adding services directly to Operational Resilience reporting, set up the entity filters for the desired services. For instructions on setting up the entity filters, see [Setting up pillars, entity types, entity filters, and entities](../../grc-operational-res/concept/setting-up-hierarchy.md).

![Add a\ service to OpRes reporting.](../image/opres-reporting.png "Add a service to OpRes reporting")

**Note:** After adding a service to Operational Resilience reporting in the Operational Resilience Workspace, the **Add to OpRes reporting** option is no longer displayed in the UI for that service.

After adding a service to Operational Resilience reporting, you can view the **Add** or **New** options in the Service form. Use these options to configure the relationship between the service and its entities. To remove an associated service or process, select the service or process and then choose **Remove**.

## Overview and Details tabs in the Service form

On the **Overview** tab in the Service form, you can view the resilience metrics for a service as shown in the following example.

![Resilience metrics on the Overview tab.](../../grc-operational-res/image/ver-layout.png "Resilience metrics on the Overview tab")

The Red flags section displays the total number of red flags, red flags by type, and details of the assets that are impacted by the red flags.

On the **Details** tab in the Service form, you can view the key attributes of a service as shown in the following example:

![Key attributes on the Details tab.](../image/services-details-tab.png "Details tab")

## Child services, processes, and dependencies of a service

When you add a service to Operational Resilience reporting, you can view and configure its child services, processes, and dependencies, as shown in the following examples.

![Service form.](../image/tabs-business-service-view.png "Service form")

![Record form.](../image/tabs-business-service-view-2.png)

## Reporting data for an object without a business service as the parent entity

When you have a business service or service as the parent entity, any red flags or dependencies roll up to that business service or service. Even if an object like a service offering \(SO\) or business process \(BP\) does not have a business service or service as the parent entity, running the scheduled job still fetches its dependencies and integrates them with the red flags.

## Other related lists in the Service form

Depending on the integrations and installed applications, the following related lists are displayed in the Service form.

<table id="table_fwq_xlt_yvb"><thead><tr><th>

Tab

</th><th>

Description

</th><th>

New action

</th><th>

Add action

</th><th>

Remove action

</th></tr></thead><tbody><tr><td>

Child services​

</td><td>

List of the child services for a service​. To associate an existing child service with a service, select **Add**. To create a child service for the current service, select **New**.

</td><td>

Form where you can add a child service. On this form, you can create a relationship between the child service and the current service​.

</td><td>

Table view where you can select multiple services that you can add as the child services of the current service​.

</td><td>

Form where you can remove a child service from the service.

</td></tr><tr><td>

Business processes​​

</td><td>

List of business processes that are associated with a service.

</td><td>

​Not applicable

</td><td>

Table view where you can select multiple processes that you can add as the child services of the current service​.

</td><td>

Form where you can remove a process from the service.

</td></tr><tr><td>

Dependencies​​

</td><td>

List of the dependencies that are associated with a service.

</td><td>

Not applicable

</td><td>

Table view where you can select multiple assets \(entities\) that you can add as the downstream entities of the current service​.

</td><td>

Form where you can remove an asset from the service.

</td></tr><tr><td>

Issues​

</td><td>

List of the issues that are associated with a service. You can select **Add** to associate an existing issue with a service as shown in the following example. To create an issue for a service, you can also select **New**.

</td><td>

Form where you can create an issue for a service.​

</td><td>

Form where you can add an existing issue to a service.​

</td><td>

Not applicable

</td></tr><tr><td>

High risks​​

</td><td>

List of the high-risk items or the risk assessments in the monitor state that are associated with the service. Risks are rolled up from dependencies.

</td><td>

​Not applicable

</td><td>

​Not applicable

</td><td>

​Not applicable

</td></tr><tr><td>

Failed​​ controls

</td><td>

List of the failed or common controls where the status of the control is non-compliant and the reliant entity is the service. Controls are rolled up from dependencies.

</td><td>

​Not applicable

</td><td>

​Not applicable

</td><td>

​Not applicable

</td></tr><tr><td>

Change requests​​ ​

</td><td>

List of the change requests that are associated with a service.

</td><td>

Change Request form. When you submit the Change Request form, the application creates a record in the Services table.​

</td><td>

​Not applicable

</td><td>

​Not applicable

</td></tr><tr><td>

Tasks​​​

</td><td>

List of the tasks that are associated with a service​.

</td><td>

List of the task tables, from where you can select the type of the task that you want to create. When you submit the form, the application creates a record in the Services with the Tasks table.

</td><td>

​Not applicable

</td><td>

​Not applicable

</td></tr><tr><td>

Incidents​​​​

</td><td>

List of the incidents that are associated with all the dependencies and services.

</td><td>

Incident form. When you submit the Incident form, it creates a record in the Services table.

</td><td>

​Not applicable

</td><td>

​Not applicable

</td></tr><tr><td>

Outages​​

</td><td>

List of the open outages that are associated with all the dependencies and services.

</td><td>

​Outage form. When you submit the form, the application creates a record in the Services table.

</td><td>

​Not applicable

</td><td>

​Not applicable

</td></tr><tr><td>

Business continuity plans

</td><td>

List of the Business continuity plans that are associated with a service.

</td><td>

​Not applicable

</td><td>

​Not applicable

</td><td>

​Not applicable

</td></tr><tr><td>

Vulnerabilities

</td><td>

List of vulnerabilities that are associated with a service.

</td><td>

Vulnerabilities for a service.

</td><td>

​Not applicable

</td><td>

​Not applicable

</td></tr><tr><td>

Importance and impact assessment​

</td><td>

List of the approved Importance and impact assessment​s​.

</td><td>

​Not applicable

</td><td>

​Not applicable

</td><td>

​Not applicable

</td></tr><tr><td>

Scenario analysis​​

</td><td>

List of the approved Scenario analyses​.

</td><td>

​Not applicable

</td><td>

​Not applicable

</td><td>

​Not applicable

</td></tr><tr><td>

Operational vulnerabilities

</td><td>

Operational vulnerabilities associated with a service.

</td><td>

​Not applicable

</td><td>

​Not applicable

</td><td>

​Not applicable

</td></tr></tbody>
</table>## Service added as an entity of Services \(OR\) type

When you add a service to the Operational Resilience reporting, the service is added as an entity of the Services \(OR\) type, as shown in the following example.

![Service added as an entity.](../image/service-or-entity-type.png "Service added as an entity of Services (OR) type")

All services in Operational Resilience belong to the Services pillar. As shown in the example, the Pillar column for the entities displays the Services pillar.

**Note:** You can only add the entities that are part of the \[cmdb\_ci\_service\] table to the Services \(OR\) entity type.

Similarly, a service \(as an entity\) can belong to multiple pillars. The following example shows a service that belongs to two pillars, such as the Services and Suppliers pillars.

![Multiple pillars for one service.](../image/one-entity-multiple-pillars.png "Multiple pillars for one service")

## Open dependency view and 360-degree view for a service

In the Service form, you can select the **Open dependency view** option to display the infrastructure relationship for a service. The dependency view of a service displays its relationship with the parent services, child services, and processes as shown in the following example.

![Dependency view of a service.](../image/sample-dependency-view.png "Dependency view of a service")

On the **360° view** tab, the Operational Resilience managers can monitor the 360-degree view of a service and measure its performance.

![360° view.](../../grc-operational-res/image/bs-36-view.png)

If you have the Operational Resilience manager role, in the 360-degree view for a service, you can visualize the following entities:

-   Parent and child services
-   Dependencies that are related to a pillar, such as the Process, Technology, People, Supplier, and Facility pillars in your organization
-   Operational Resilience metrics

