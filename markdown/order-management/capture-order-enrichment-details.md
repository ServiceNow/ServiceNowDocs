---
title: Capture order enrichment details for complex fulfillment
description: Collect additional order details and technical information necessary for order decomposition and fulfillment, promoting accurate delivery and helping prevent delays or fallouts for complex products or services.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Enriching orders, Order Management, Use, Sales Customer Relationship Management]
---

# Capture order enrichment details for complex fulfillment

Collect additional order details and technical information necessary for order decomposition and fulfillment, promoting accurate delivery and helping prevent delays or fallouts for complex products or services.

## Before you begin

Role required: sn\_ind\_tmt\_orm.order\_fulfilment\_agent

## About this task

You can enrich order and order line items that meet the following conditions:

-   The Order Enrichment Flow Policy is configured for this product offering
-   The order has been captured, reviewed, and submitted by an order agent
-   The order and order line items are in the Enrichment in progress state

## Procedure

1.  Navigate to  **Workspaces** &gt; **CSM/FSM Configurable Workspace.** .

2.  Select the List icon ![](../../../reuse/icons/product-icons/list-outline-24.svg).

3.  Navigate to the order enrichment task using either of the following options.

<table id="choicetable_ctl_t4y_pgc"><thead><tr><th align="left" id="d68918e108">

Navigation option

</th><th align="left" id="d68918e111">

Steps

</th></tr></thead><tbody><tr><td id="d68918e117">

**From Customer Orders**

</td><td>

1.  Navigate to **Customer Orders** &gt; **All**.
2.  Select the order record that's ready for enrichment, which is indicated by the Enrichment in progress state.
3.  View the order enrichment tasks by selecting the **Order Tasks** tab.
4.  Select the order enrichment task to open the task record and view its details.


</td></tr><tr><td id="d68918e153">

**From Order Tasks**

</td><td>

1.  Navigate to **Order Tasks** &gt; **All**.
2.  Select the order record that's ready for enrichment.

This is indicated by the Enrichment in progress state.

3.  Select the order enrichment task to open the task record and view its details.


</td></tr></tbody>
</table>4.  Select **Configure**.

5.  Capture the additional information that you gathered from the customer in the configurator UI.

    Depending on the product configuration, you can choose from a value range, a drop-down menu, or enter text in the configurator UI.

6.  Adjust the quantity by entering a value in the **Quantity** field.

7.  Review the quantity and other details in the Current Selection pane before proceeding.

8.  Select **Update**.

    You're redirected back to the enrichment task Details page.

9.  To mark the task as complete, select the **Closed complete** option from the **State** drop-down menu and select **Save**.

    You're redirected back to the **Order Tasks** tab where you can see new set of tasks that are asynchronously created.

10. Complete all the enrichment tasks in a similar manner.

11. View the summary of your selections for each enrichment task by going to its **Order Task Characteristics Values** tab.

    The **Characteristic Options** tab displays all the available options for that product characteristic.


## Result

The order record is updated with all necessary fulfillment details. The order state changes to New. The fulfillment manager can now approve or reject the order.

## What to do next

[Approve orders in Order Management](som-om-approve-product-order.md)

