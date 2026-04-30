---
title: Review the domain order related items associated with a domain order
description: Review the domain order related line items that were generated for a customer order line item so that you can confirm all the related details are correct and complete.OM revamp project - Check the validity of this topic with dev.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Order decomposition, Order Management, Use, Sales Customer Relationship Management]
---

# Review the domain order related items associated with a domain order

Review the domain order related line items that were generated for a customer order line item so that you can confirm all the related details are correct and complete.

## Before you begin

Role required: sn\_ind\_tmt\_orm.order\_fulfillment\_manager

## About this task

Each product order contains the domain order related items that are created when a customer order is approved and then decomposed. You should review each domain order related item to make sure that they’re correct and complete. You can update them as needed.

Review if compatibility rules or horizontal relationships are configured for domain order specs.

## Procedure

1.  To view the domain order related items that are associated with a customer line item and product order, select the customer order line item and product order.

2.  Select an associated domain order related item to review or add a new domain order related item.

    For change, the new column **Existing related inventory** displays **True** for the domain order related items that are created using existing valid product inventory relationships and **False** for the domain order related items that are newly created.

<table id="choicetable_u3t_rjd_54b"><thead><tr><th align="left" id="d98562e88">

Task

</th><th align="left" id="d98562e91">

Action

</th></tr></thead><tbody><tr><td id="d98562e97">

**Review an existing domain order related item**

</td><td>

1.  Select the **Domain Order Related Items \(n\)** tab \(where \(n\) is the number of domain order related items that are associated with the selected domain order\) to access the Domain Order Related Items form.
2.  In the **Number** field, select an existing or new domain order related item to review.
 -   To refresh the form, select the refresh icon ![](../image/form-refresh.png).
-   To filter the existing domain order related items, select the filter icon ![](../image/form-filter.png).


</td></tr><tr><td id="d98562e140">

**Create a new domain order related item**

</td><td>

Select **New**.

</td></tr></tbody>
</table>3.  On the form, add a domain order related item or review the selected domain order related item details and update as needed.

    |Field|Description|
    |-----|-----------|
    |Number|Domain order related item number.|
    |Domain Order|Domain order number.|
    |Domain Order Specification|Domain order specification \(that has the Composed of relationship\) that is associated with the customer order with the selected domain order related item.|
    |Related Domain Order|Domain order number that the selected domain order related item is associated with.|
    |Related Inventory|Product inventory that the selected domain order line item is associated with.|
    |Existing related inventory|Default value is **False** that indicates the new inventory is going to be added.|

4.  For inflight change order requests, when you update any order line items and approve the order, the updates to the related order line items are displayed in the **Related Domain Order** column.

5.  When you finish reviewing and updating the domain order related items, do one of the following actions.

    |Action|Description|
    |------|-----------|
    |**Save the updated domain order related item**|Select **Update**.|
    |**Delete the domain order related item**|Select **Delete**.|


