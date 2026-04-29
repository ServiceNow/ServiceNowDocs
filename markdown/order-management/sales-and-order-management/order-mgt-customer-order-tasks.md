---
title: Review and close fulfillment tasks
description: Review and update the fulfillment tasks that are associated with an order, or order orchestration plan, so that you can make sure that all tasks are properly completed.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Order fulfillment, Order Management, Use, Sales and Order Management]
---

# Review and close fulfillment tasks

Review and update the fulfillment tasks that are associated with an order, or order orchestration plan, so that you can make sure that all tasks are properly completed.

## Before you begin

Role required: order\_approver, order\_viewer, sn\_ind\_tmt\_orm.order\_fulfillment\_manager, or sn\_ind\_tmt\_orm.service\_order\_manager \(for service orders\)

## About this task

If you encounter issues with resolving or completing an order task, you can create fallout records. Fallout records enable you to identify, investigate, and resolve order processing issues so that orders can continue processing through to completion.

When you create a manual fallout record, or an automated one is generated, the following occurs in the related order task:

-   Its **State** field changes to On hold, with a comment on which logged-in user caused it to change.
-   In the Activity section, a work order note indicates that the order task state has changed from its former state, usually In Progress, to On hold. A work order note with the message `A fallout record FOnnnn has been created` also appears.

If you create a manual fallout record or an automated one is generated for the order tasks, you can easily review and track all fallout records for a specific order. Use the **Fallouts \(n\)** tab \(where n is the number of fallouts\) that appears when you view the related customer or service order in the Customer Order form.

To learn more about order fallout, see [Managing order fallout](../concept/fallout-management-overview.md).

## Procedure

1.  Navigate to  **Workspaces** &gt; **CSM/FSM Configurable Workspace** .

2.  Select the List icon ![](../../../reuse/icons/product-icons/list-outline-24.svg).

3.  Navigate to **Order tasks**.

    -   To view all open order tasks, select **All**.
    -   To view only the tasks that are assigned to you, select **My order tasks**.
4.  Select the order task that you want to work on.

    You can also directly access the task records for an order from the order orchestration UI. To learn more about accessing the UI, see [Order fulfillment](../concept/reviewing-orchestration-plans-order-fulfillment.md).

5.  For each order task, set the status by selecting an option from the **State** drop-down menu and update the work notes, as required.

6.  On the Order Task form, review the order task details and update as needed.

    For information about the field descriptions, see [Order Tasks form](../reference/field-descriptions-order-task-form.md).

7.  When you finish reviewing and updating the order task or encounter issues that are preventing its closure, perform one of the actions from the following table.

    |Action|Description|
    |------|-----------|
    |**Save the updated order task**|Select **Save**.|
    |**Delete the order task**|Select **Delete** from the more options icon ![](../image/icon-three-dot-menu.png).|
    |**Create a fallout record**|Select **Create Fallout** from the more options icon ![](../image/icon-three-dot-menu.png). To learn more, see [Create a manual fallout record](create-manual-order-fallout-record.md).|


## Result

After your agents complete all fulfillment tasks for the entire customer order, the following actions occur:

-   The **State** field for the customer order is automatically set to **Completed**.
-   The **State** field for each of the individual customer order line items is set to **Completed**.
-   Corresponding sold products or product inventory records are created depending on the configuration.

## What to do next

Create MACD orders directly from the sold products. For more information, see [Request post-sale change orders](create-macd-orders.md).

**Parent Topic:**[Order fulfillment](../concept/reviewing-orchestration-plans-order-fulfillment.md)

