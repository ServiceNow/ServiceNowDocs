---
title: Create a purchase order from a request
description: You can create a purchase order directly from a request. This enables procurement managers to obtain items and fulfill requests from the Service Catalog. You can create multiple purchase orders from a request.
locale: en-US
release: xanadu
product: Procurement
classification: procurement
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Sourcing items in a service catalog request, Procurement, Asset Management, IT Service Management]
---

# Create a purchase order from a request

You can create a purchase order directly from a request. This enables procurement managers to obtain items and fulfill requests from the Service Catalog. You can create multiple purchase orders from a request.

## Before you begin

Role required: procurement\_admin or procurement\_user

## Procedure

1.  Navigate to **All** &gt; **Procurement** &gt; **Requests** &gt; **Requests**.

2.  Select the **Number** of a request that has been approved but not sourced.

    Look in the **Request State** and **Sourced** columns.

3.  In the **Catalog Tasks** related list, select a Source Request Items number.

4.  Select **Source Request**.

    The Source Request screen is displayed with a list of all the requested items.

5.  Select **Purchase** in the requested item section.

6.  In the **Vendor** list, select the vendor from which the requested item or items should be delivered.

7.  Verify if the **Out of Stock** field is set to **false**.

    If the vendor doesn't have stock, the field value will be **true**.

8.  In the **Quantity** field, specify the quantity you want to order.

9.  In the **Destination Stockroom** list, select the destination to which the requested item or items should be delivered.

10. Select the **Consolidate PO** check box to combine the listed items with existing purchase orders.

    When you check Consolidate Purchase Orders, all items sourced from the same vendor on the same request are placed on the same purchase order. When you select a vendor, the system automatically searches for purchase orders that have been created for the same request, have the same **Vendor** selected, and have the **Requested** status. If the system finds a match, all items are placed on the same purchase order and can be ordered together. If the system does not find a match, a new purchase order is created.

    For example, if you are purchasing 25 phones from Apple and an open purchase order already exists for Apple, the 25 phones are added to the open purchase order. If there are no open purchase orders for the selected vendors, new purchase orders are created. Items ordered from the same vendor are grouped together. Different items are shown on separate lines on the purchase order.

11. Select **Submit**.


## Result

-   Purchase order is created.
-   On the request, the **Sourced** check box is selected

**Parent Topic:**[Sourcing items in a service catalog request](../concept/c_SourcingRequestItems.md)

**Related topics**  


[Create a transfer order from a request](t_CreatingTransferOrderFromReq.md)

[Source requests from local stockrooms](consume-local-asset-stock.md)

[Add an assignment from a request](t_AddingAssignmentsFromReq.md)

