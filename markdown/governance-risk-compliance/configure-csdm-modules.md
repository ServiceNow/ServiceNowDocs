---
title: Add a service to Operational Resilience reporting
description: Manage services, business services, service offerings, business processes, and application services from the CSDM modules in the Operational Resilience Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/configure-csdm-modules.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Gathering data aligned with the CSDM setup, Manage, Operational Resilience, Governance, Risk, and Compliance]
---

# Add a service to Operational Resilience reporting

Manage services, business services, service offerings, business processes, and application services from the CSDM modules in the Operational Resilience Workspace.

## Before you begin

Role required: sn\_oper\_res.manager with the itil user role, sn\_oper\_res.admin with the itil user role

## About this task

Beginning with Operational Resilience, Release 21.0.x, records in the Services, Business services, Offerings, Business processes, and Application services modules feature a vertical layout.

The following modules are displayed in the Operational Resilience Workspace.

-   Services
-   Business services
-   Offerings
-   Business processes
-   Application services

**Note:** The Services module is typically used by existing customers whereas the Business services module is used by new customers.

When the **Compute Operational Resilience Compliance** scheduled job runs in the background daily, you can view the status reports of the services in Operational Resilience. The Services module in the Operational Resilience Workspace is mostly used by the existing customers.

## Procedure

1.  Navigate to **Operational Resilience Workspace** &gt; **List** &gt; **Services**.

    A list of the available services is displayed in the form.

2.  To add a service to Operational Resilience, select **New** in the Services list view and fill in the details regarding the service on the Create New service form.

    **Note:** You must have the itil user role to create a service. If you do not have the itil user role, the **New** button for creating a service is not displayed.

    For a description of the field values on the Service form, see [Create Service form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/service-form-lists-ws-reference.md).

    The Create New Service form is displayed.

3.  In the **Details** tab, fill in the fields.

    A sample **Details** tab is shown in the following example.

    \[Omitted image "create-new-service-form-ws.png"\] Alt text: Details tab in the Create New Service form.

4.  To save details of the service, select **Save**.

    \[Omitted image "saved-service-form.png"\] Alt text: Sample form for a service.

    In releases prior to 20.x.x, a single level of hierarchy was supported, such as from a parent service to the child service, from the child service to the process, and from the process to a dependency. This hierarchy is supported for services for existing customers and it is displayed in the Services form, as shown in the example.

5.  To add the selected service to Operational Resilience reporting, select **Add to OpRes reporting**.

    A message is displayed that the selected service is synchronized with Operational Resilience reporting and dashboards.

    1.  To navigate to the entity record and maintain the upstream and downstream entities, select **Go to entity**.

        Once you add the service to Operational Resilience reporting, its entity record is created and the **Go to entity** UI action is displayed on the form.

        The service is added to Operational Resilience reporting as shown in the following example.

        \[Omitted image "ser-added-to-opres-reporting.png"\] Alt text: Service added to Operational Resilience reporting.

        **Note:** After you’ve added the service to Operational Resilience reporting, the **Add to OpRes reporting** option isn’t displayed for the service anymore on the Service form.

6.  To maintain the upstream and downstream relationships for the selected record, select **Go to entity**.

    The **Go to entity** button is visible only if the entity for the record has already been created. It is provided to maintain the upstream and downstream relationships for the selected record. Operational Resilience managers can add the upstream and downstream dependencies. Selecting **Go to entity** displays the entity record for the select object.

    1.  Navigate to the **Hierarchy** tab in the entity record.

    2.  Add upstream or downstream entities for the selected record.

        You can add upstream or downstream entities to the entity record as shown in the example.

        \[Omitted image "hierachy-tab-add-ups-downs-ent.png"\] Alt text: Upstream or downstream entities.

    3.  To save the upstream or downstream relationships, select **Save**.

7.  To view the infrastructure relationship of the service, select **Open dependency view**.

    The infrastructure relationship of a service with its parent services and child services is displayed as shown in the following example.

    \[Omitted image "sample-dependency-view.png"\] Alt text: Sample dependency view.

    You can view the dependencies in the desired map view such as the vertical, horizontal, radial, force, group, or details view.

8.  To view the relationship of the service with its related entities, select **360° view**.

    The relationship of a service with its related entities, such as the dependencies and red flags in a 360-degree view, is displayed as shown in the following example.

    \[Omitted image "360-degree-view.png"\] Alt text: Relationship of a service with its related entities in a 360°-degree view.

9.  To save the details on the form, select **Save**.

    The Service form is displayed as shown in the following example.

    \[Omitted image "sample-service-form.png"\] Alt text: Service form with the related tabs.


