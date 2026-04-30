---
title: Cancel a purchase order line item
description: You can cancel a purchase order line items with a status of Requested, Ordered, or Pending Delivery.
locale: en-US
release: xanadu
product: Procurement
classification: procurement
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Create a purchase order, Procurement purchase order management for assets, Procurement, IT Asset Management]
---

# Cancel a purchase order line item

You can cancel a purchase order line items with a status of **Requested**, **Ordered**, or **Pending Delivery**.

## Before you begin

Role required: procurement\_admin or procurement\_user

## About this task

Keep the following in mind when you cancel a purchase order line item.

-   When a purchase order line item is canceled, if all other line items are also canceled, the purchase order is canceled.
-   After a purchase order line item is canceled, it can be reordered if the associated purchase order has not been canceled or received.
-   If you cancel a purchase order line item for which assets were created, the assets are deleted from the system and removed from the purchase order.
-   If you reorder the same purchase order line item, the assets are recreated for that line if the line has a status of **Pending Delivery**.

## Procedure

1.  Navigate to **All** &gt; **Procurement** &gt; **Orders** &gt; **Purchase Orders**.

2.  Open a purchase order.

3.  In the **Purchase order line items** related list, select a line item to cancel.

4.  Click **Cancel**.


**Parent Topic:**[Create a purchase order](t_CreateAPurchaseOrder.md)

