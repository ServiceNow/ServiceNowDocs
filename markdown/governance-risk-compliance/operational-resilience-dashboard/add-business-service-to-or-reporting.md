---
title: Add a business service to Operational Resilience reporting
description: Add a business service to Operational Resilience reporting in the Operational Resilience Workspace. The Operational Resilience managers with \[sn\_oper\_res.manager\] roles can add business services, service offerings, business processes, and application services to their entity types from the business service form or the list actions.
locale: en-US
release: xanadu
product: Operational Resilience Dashboard
classification: operational-resilience-dashboard
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Gathering data aligned with the CSDM setup, Manage, Operational Resilience, Governance, Risk, and Compliance]
---

# Add a business service to Operational Resilience reporting

Add a business service to Operational Resilience reporting in the Operational Resilience Workspace. The Operational Resilience managers with \[sn\_oper\_res.manager\] roles can add business services, service offerings, business processes, and application services to their entity types from the business service form or the list actions.

## Before you begin

Role required: sn\_oper\_res.manager with the itil user role, sn\_oper\_res.admin with the itil user role

## About this task

Beginning with Operational Resilience, Release 21.0.x, records in the Services, Business services, Offerings, Business processes, and Application services modules feature a vertical layout.

**Note:** The Services module is typically used by existing customers whereas the Business Services module is used by new customers.

## Procedure

1.  Navigate to **Operational Resilience Workspace** &gt; **List** &gt; **Business service**.

2.  Open any one record of a business Service.

    The form view of the Business Service form is visible.

    ![Business Service form.](../image/bs-form.png)

    As shown in the example, a business service could have a service offering. A service offering such as SO1 could have an embedded child service offering SO2. Similarly, associated business processes, application services, dependencies are shown in the form.

    The Operational Resilience managers can perform UI actions such as Open dependency view, 360 view. In the record header, the Operational Resilience managers can view the Record Type, Owned by, Business criticality, and Operational status.

    The following related lists are displayed:

    -   Overview
    -   Details
    -   Service offering
    -   Business Process
    -   Application Service
    -   Dependencies
    All the UI actions such as viewing the records, removing the records can be performed by the Operational Resilience managers in the related list.

    The **Add** and **Remove** buttons are visible on the related list through which the managers can add or remove the records in the related list. The related list records are the entity of the displayed record.

3.  Select **Open dependency view** to display the hierarchy relationship for the record.

    **Note:** The hierarchy relationship for the record is displayed only when the relationship is added in the records.

4.  Select **360 view** to display all the related records.

5.  To add a business service to the Operational Resilience application, select **New** in the Business services list view and fill in the details regarding the service on the Create New service form.

    For a description of the field values on the Business service form, see [Create New Business Service form](../reference/create-new-business-service-form.md).

6.  To save updates to the existing record, select **Save**.

7.  To add the selected business service to Operational Resilience reporting, select the **Add to OpRes reporting** UI action.

    A message is displayed that the selected business service is synchronized with Operational Resilience reporting and dashboards.

    1.  To navigate to the entity record and maintain the upstream and downstream entities, select **Go to entity**.

        Once you add the service to Operational Resilience reporting, its entity record is created and the **Go to entity** UI action is displayed on the form.

        The service is added to Operational Resilience reporting as shown in the following example.

        ![Service added to Operational Resilience reporting.](../../grc-operational-res-ws/image/ser-added-to-opres-reporting.png "Service added to Operational Resilience reporting")

        **Note:** After you’ve added the service to Operational Resilience reporting, the **Add to OpRes reporting** option isn’t displayed for the service anymore on the Service form.

8.  To maintain the upstream and downstream relationships for the selected record, select **Go to entity**.

    The **Go to entity** button is visible only if the entity for the record has already been created. It is provided to maintain the upstream and downstream relationships for the selected record. Operational Resilience managers can add the upstream and downstream dependencies. Selecting **Go to entity** displays the entity record for the select object.

    1.  Navigate to the **Hierarchy** tab in the entity record.

    2.  Add upstream or downstream entities for the selected record.

        You can add upstream or downstream entities to the entity record as shown in the example.

        ![Upstream or downstream entities.](../image/hierachy-tab-add-ups-downs-ent.png)

    3.  To save the upstream or downstream relationships, select **Save**.

9.  To view dependencies of the selected business service, select the **Open dependency view**.

    You can view the dependencies in the desired map view such as the vertical, horizontal, radial, force, group, or details view.

10. To navigate to the 360º view and monitor upstream and downstream relationships, entity class, entity types of the business service, select the **360º view**.


