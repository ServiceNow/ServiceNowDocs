---
title: Review and submit a product or service order in Order Management
description: Review all the order line items as the next step in the process to create a product order. Edit the order details as needed before submitting it for fulfillment approval.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Creating orders, Order Management, Use, Sales Customer Relationship Management]
---

# Review and submit a product or service order in Order Management

Review all the order line items as the next step in the process to create a product order. Edit the order details as needed before submitting it for fulfillment approval.

## Before you begin

Role required: sn\_ind\_tmt\_orm.order\_agent, order\_approver

## Procedure

1.  Navigate to  **Workspaces** &gt; **CSM/FSM Configurable Workspace.** .

2.  Select the List icon ![](../../../reuse/icons/product-icons/list-outline-24.svg).

3.  Navigate to **Customer Orders** &gt; **All**.

4.  Select the order that you want to submit for approval.

5.  Select **Review &amp; Submit**.

6.  Review the order line items details and configurations.

<table id="table_hll_tf4_tqb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Order Line

</td><td>

Unique system-assigned number of the order line item with a prefix ORDL.

</td></tr><tr><td>

Product Offering

</td><td>

Product offering that the customer is ordering for fulfillment.

</td></tr><tr><td>

Product Specification

</td><td>

Product specification that is associated with the order line item.

</td></tr><tr><td>

Qty

</td><td>

Product quantity.

</td></tr><tr><td>

Unit list price

</td><td>

Price of a product or service as defined in the Price List Line.

</td></tr><tr><td>

Cumulative monthly price

</td><td>

Total monthly recurring charges for this order line item. An example is a monthly line charge.

</td></tr><tr><td>

Cumulative annual price

</td><td>

Total yearly recurring charges for this order line item.

</td></tr><tr><td>

Cumulative one time price

</td><td>

Total non-recurring charges for this order line item. An example is a one-time installation fee.

</td></tr><tr><td>

Cumulative net price

</td><td>

Total price for this order line item.

</td></tr><tr><td>

Total monthly recurring price

</td><td>

Aggregated monthly cost of all recurring charges associated with an order line item or subscription contract.

</td></tr><tr><td>

Total one time price

</td><td>

Aggregate cost of all non-recurring charges associated with an order line item. These are typically setup fees, installation charges, or product costs that are billed once rather than on a recurring basis.

</td></tr><tr><td>

Total amount

</td><td>

Aggregate cost of all charges, both, one-time and recurring, associated with the entire order. It is a calculated field that reflects the final payable amount after applying quantity, pricing, and adjustments.

</td></tr></tbody>
</table>    **Note:** You can't manually adjust the amounts that appear in the pricing fields. They only change if you change the characteristic values for the order line items.

7.  To update the configuration or quantity for an order line item, select the Edit icon ![](../../../reuse/icons/product-icons/pencil-outline-24.svg).

    You're redirected to the configurator UI for making updates.

8.  To delete an order line item, select the Delete icon ![](../image/trash-icon.png).

9.  Save any changes or updates and select the **Reprice** to reset the total pricing.

10. After reviewing the order, select **Submit**.

    The state of the order changes from Draft to New. The order progresses to the next step of the order life cycle.


## What to do next

For complex orders, capture technical details. For more information, see [Capture order enrichment details for complex fulfillment](capture-order-enrichment-details.md).

If order enrichment tasks don't apply, move to order approval. For more information, see [Approving or rejecting orders](../concept/approving-rejecting-orders-som.md).

