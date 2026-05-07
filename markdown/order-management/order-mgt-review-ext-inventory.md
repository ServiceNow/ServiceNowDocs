---
title: Review the external product inventory details for a customer order
description: Review the external inventory details of the customer orders that you’ve received from the external Configure, Price, and Quote \(CPQ\) system during the order capture process.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [External product inventory ID, Managing service orders, Order Management, Use, Sales Customer Relationship Management]
---

# Review the external product inventory details for a customer order

Review the external inventory details of the customer orders that you’ve received from the external Configure, Price, and Quote \(CPQ\) system during the order capture process.

## Before you begin

Role required: order\_approver, order\_viewer, sn\_ind\_tmt\_orm.order\_fulfillment\_manager

## Procedure

1.  Navigate to  **Workspaces** &gt; **CSM/FSM Configurable Workspace** .

2.  Select the List icon ![](../../../reuse/icons/product-icons/list-outline-24.svg).

3.  Navigate to **Customer Orders** &gt; **All**.

4.  Select an order you want to view.

5.  View the external product inventories that are currently associated with an order line item by selecting the customer order line item.

6.  Select the **External product inventories** tab.

7.  On the form, review the fields values.

    **Note:** To create a new external product inventory table, select **New**. On the Create New External product inventory form, fill in the fields.

<table id="table_ydt_sc5_cyb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Unique system-assigned number of the external inventory ID.

</td></tr><tr><td>

External product inventory ID

</td><td>

External product inventory ID from the CPQ system.

</td></tr><tr><td>

Order line item

</td><td>

Order line item number against which the external inventory ID is captured.

</td></tr><tr><td>

State

</td><td>

State of the external product inventory ID:-   **Valid**

When the order was closed, the state of the external product inventory ID was updated to Valid.

-   **Invalid**

During the inflight order changes, the state of the external product inventory ID was updated to Invalid.

**Note:** The state of the external inventory ID is updated after the order fulfillment is complete \(the order state is Closed Complete\).

</td></tr></tbody>
</table>8.  Save or delete the product inventory details.

    |Action|Description|
    |------|-----------|
    |**Save the external product inventory details**|Select **Save**.|
    |**Delete the external product inventory details**|Select the options icon ![](../image/more-options.png) next to the **Save** button, and then select **Delete**.|


**Parent Topic:**[External product inventory ID](../concept/ext-inventory-id.md)

