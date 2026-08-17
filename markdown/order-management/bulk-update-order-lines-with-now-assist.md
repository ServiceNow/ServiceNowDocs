---
title: Manage order updates with ServiceNow Otto
description: Use ServiceNow Otto for Order Management to manage order updates, such as applying bulk changes to order line items, removing order lines, or creating an order case, without navigating between individual records.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/order-management/bulk-update-order-lines-with-now-assist.html
release: zurich
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use, ServiceNow Otto for Order Management]
---

# Manage order updates with ServiceNow Otto

Use ServiceNow Otto for Order Management to manage order updates, such as applying bulk changes to order line items, removing order lines, or creating an order case, without navigating between individual records.

## Before you begin

Role required: sn\_ind\_tmt\_orm.order\_agent.

## About this task

The Order Assistant Agent is a context-aware assistant that works inside the order workspace and helps order agents perform order updates while working on a single order. In this task, you can use ServiceNow Otto for Order Management to:

-   Bulk apply a discount to all order lines.
-   Update the shipping address for all order lines.
-   Update quantity for order lines.
-   Delete order lines.
-   Create order case.

Some bulk update actions offer an undo option immediately after the change is applied. Undo is available only within the current ServiceNow Otto chat and only for supported actions, such as updating quantity or shipping address.

Bulk quantity updates apply to top-level \(parent\) order lines. Child order lines reflect the change through the parent relationship and aren’t updated directly.

The actions available in ServiceNow Otto depend on the current state of the order.

<table id="table_kfk_p2f_m3c"><thead><tr><th>

Order state

</th><th>

Actions available to the order agent

</th></tr></thead><tbody><tr><td>

Draft

</td><td>

-   Bulk update quantity
-   Update shipping address
-   Apply bulk discount
-   Delete an order line item

</td></tr><tr><td>

New

</td><td>

-   Bulk update quantity
-   Update shipping address
-   Apply bulk discount
-   Delete an order line item
-   Create case for order
-   Create a case for order lines

</td></tr><tr><td>

Acknowledged

</td><td>

-   Create case for order
-   Create case for order lines

</td></tr></tbody>
</table>**Note:** For best results, start a new ServiceNow Otto chat for each bulk action. Long conversations can reduce accuracy overtime.

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace**.

2.  Select the List \[Omitted image "list-outline-24.svg"\] Alt text: icon.

3.  Navigate to **Orders** &gt; **All**

4.  Select an order.

5.  Launch the ServiceNow Otto chat panel by selecting the ServiceNow Otto icon \[Omitted image "icon-otto-outline-24.svg"\] Alt text:.

6.  In the ServiceNow Otto panel, start Assistance for orders \(Order Assistant Agent\).

7.  If prompted, confirm the order number \(or enter a different order number\).

8.  Choose the order update that you want to perform.

<table id="choicetable_cyq_1s4_k3c"><thead><tr><th align="left" id="d83654e282">

Action

</th><th align="left" id="d83654e285">

What to do in ServiceNow Otto panel

</th></tr></thead><tbody><tr><td id="d83654e294">

**Bulk update quantity**

</td><td>

1.  Enter the new quantity value when prompted.
2.  Confirm the bulk update.


</td></tr><tr><td id="d83654e312">

**Bulk update shipping address**

</td><td>

1.  Provide the complete shipping address when prompted.
2.  Confirm the bulk update.


</td></tr><tr><td id="d83654e330">

**Apply bulk discount**

</td><td>

1.  Enter the discount percentage when prompted.
2.  Choose how to handle lines with manual adjustments \(if prompted\).
3.  Confirm the bulk update.


</td></tr><tr><td id="d83654e351">

**Delete order line**

</td><td>

Specify the top-level order line you want to remove when prompted, then confirm the deletion.

</td></tr><tr><td id="d83654e361">

**Create Order case**

</td><td>

Describe the issue with the order when prompted, review the generated summary, then confirm to create the order case.

</td></tr></tbody>
</table>9.  Review the order lines to verify the update was applied.


## What to do next

After updating quantity or shipping address, you can keep the changes or undo them when prompted.

**Parent Topic:**[Using ServiceNow Otto for Order Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/order-management/now-assist-order-management-using.md)

