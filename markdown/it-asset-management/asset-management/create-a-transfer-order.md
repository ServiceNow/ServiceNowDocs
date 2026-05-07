---
title: Create a transfer order
description: Create a transfer order to move one or more assets from a source stockroom to a destination stockroom.
locale: en-US
release: australia
product: Asset Management
classification: asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Transfer order tasks, Manage transfer order, Using Asset Management, Asset Management, IT Asset Management]
---

# Create a transfer order

Create a transfer order to move one or more assets from a source stockroom to a destination stockroom.

## Before you begin

Role required: inventory\_user

The inventory\_user, asset, or procurement\_user role can only access the Transfer Order \[alm\_transfer\_order\] reports. You must activate the Procurement \(com.snc.procurement\) plugin for the inventory\_user, asset, and procurement\_user roles.

## Procedure

1.  Navigate to **All** &gt; **Inventory** &gt; **Transfer Orders** &gt; **Create Transfer Order**.

2.  In the **From Stockroom** list, select a stockroom from which you want to ship the items.

3.  In the **To Stockroom** list, select a stockroom where you want to ship the items.

    **Note:** If you select the same stockroom in both the **From Stockroom** and **To Stockroom** fields, the transfer order automatically moves from **Draft** to **Received** when a transfer order line is added.

4.  Select a date and time for the delivery from the **Delivery by date** date picker.

5.  Select **Submit**.


## Result

Transfer order record is created.

## What to do next

Create transfer order lines to specify the items that the transfer order comprises of.

**Parent Topic:**[Transfer order tasks](../concept/work-with-transfer-orders.md)

**Related topics**  


[Create transfer order line](create-transfer-order-line.md)

