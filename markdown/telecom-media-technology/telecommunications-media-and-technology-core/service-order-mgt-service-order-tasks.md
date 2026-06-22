---
title: Review and update the service order fulfillment tasks
description: Review and update the fulfillment tasks that are associated with a service order, or order orchestration plan, so that you can make sure that all tasks are properly completed.OM content revamp project - This is a redundant topic and has been removed from the SOM bundle on Oct 9, 2025. A common topic for customer and service orders \(order-mgt-customer-order-tasks.dita\) has been preserved with combined content.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-media-technology/telecommunications-media-and-technology-core/service-order-mgt-service-order-tasks.html
release: australia
product: Telecommunications, Media and Technology Core
classification: telecommunications-media-and-technology-core
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Approve and fulfill service orders, Use, Sales Customer Relationship Management for Telecommunications, Telecommunications, Media, and Technology \(TMT\)]
---

# Review and update the service order fulfillment tasks

Review and update the fulfillment tasks that are associated with a service order, or order orchestration plan, so that you can make sure that all tasks are properly completed.

## Before you begin

Role required: order\_approver, order\_viewer, sn\_ind\_tmt\_orm.service\_order\_manager

## About this task

If you encounter issues with resolving or completing an order task, you can create fallout records. Fallout records enable you to identify, investigate, and resolve order processing issues so that orders can continue processing through to completion.

When you create a manual fallout record, or an automated one is generated, the following occurs in the related order task:

-   Its **State** field changes to On hold, with a comment on which logged-in user caused it to change.
-   In the Activity section, a work order note indicates that the order task state has changed from its former state, usually In Progress, to On hold. A work order note with the message `A fallout record FOnnnn has been created` also appears.

If you create a manual fallout record or an automated one is generated for the order tasks, you can easily review and track all fallout records for a specific order. Use the **Fallouts \(n\)** tab \(where n is the number of fallouts\) that appears when you view the related customer or service order in the Customer Order form.

To learn more about order fallout, see [Managing order fallout](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/sales-and-order-management/fallout-management-overview.md).

## Procedure

1.  Navigate to **All** &gt; **Customer Order Management** &gt; **Workspace** &gt; **Configurable Workspace Home**.

2.  From the **Configurable Workspace Lists** tab \[Omitted image "list-outline-24.svg"\] Alt text:, select **Order Tasks**.

    1.  Do one the following options:
        -   To view all open order tasks, select **All**.
        -   To view only the tasks that are assigned to you, select **My Tasks**.
    2.  Select the order task that you want to work on.
    **Note:** You can also directly access the task records for an order from the Orchestration Plan UI. To learn more, see [Review an order orchestration plan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/sales-and-order-management/review-order-fulfillment-orchestration-plan.md).

3.  For each order task, set the status and update the work notes, as required.

4.  On the form, review the order task details and update as needed.

    For information about the field descriptions, see [Order Tasks form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/sales-and-order-management/field-descriptions-order-task-form.md).

5.  When you finish reviewing and updating the order task, or encounter issues preventing its closure, do one of the actions in the following table.

    |Action|Description|
    |------|-----------|
    |**Save the updated order task**|Select **Save**.|
    |**Delete the order task**|Select the options icon \[Omitted image "more-options.png"\] Alt text: next to the **Save** button, and then select **Delete**.|
    |**Create a fallout record**|Select the options icon \[Omitted image "more-options.png"\] Alt text: next to the **Save** button, and then select **Create Fallout**. To learn more, see [Create a manual fallout record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/sales-and-order-management/create-manual-order-fallout-record.md).|


## Result

After your agents complete all fulfillment tasks for the entire service order, the following actions occur:

-   The **State** field for the customer order is automatically set to **Completed**.
-   The **State** field for each of the individual customer order line items is set to **Completed**.

