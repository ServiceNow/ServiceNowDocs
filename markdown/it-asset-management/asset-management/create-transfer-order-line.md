---
title: Create transfer order line
description: Add a transfer order a line to a transfer order for each asset or consumable model you want to move.
locale: en-US
release: australia
product: Asset Management
classification: asset-management
topic_type: task
last_updated: "2026-04-06"
reading_time_minutes: 1
breadcrumb: [Transfer order tasks, Manage transfer order, Using Asset Management, Asset Management, IT Asset Management]
---

# Create transfer order line

Add a transfer order a line to a transfer order for each asset or consumable model you want to move.

## Before you begin

Role required: inventory\_user

The inventory\_user, asset, or procurement\_user role can only access the Transfer Order \[alm\_transfer\_order\] reports. You must activate the Procurement \(com.snc.procurement\) plugin for the inventory\_user, asset, and procurement\_user roles.

## About this task

A transfer order can contain one or more transfer order lines. Under a single transfer order, all transfer order lines have the same **From location** and **To location**. Each line contains an asset to transfer and the quantity to transfer. The item to transfer is identified by asset name and model name. A transfer order line can involve one quantity of a non-consumable asset or multiple quantities of a consumable asset. A bundled model can be transferred.

## Procedure

1.  Navigate to **All** &gt; **Inventory** &gt; **Transfer Orders** and open the transfer order.

2.  Next to **Transfer Order Lines**, select **New**.

3.  On the Create transfer order line form, fill in the fields.

    For a description of the field values, see [Transfer order line fields](../reference/create-transfer-order-line-fields.md).

4.  If the model is a consumable, specify a quantity in **Quantity Requested**.

5.  Select **Submit**.

    After creating transfer order lines, the transfer order and all the transfer order lines are in the draft stage. While a transfer order or a transfer order line is in the draft stage, it can be deleted.

    **Note:** When an asset is part of a transfer order set to **Draft**, the asset record updates to show the asset as reserved. You can't request or transfer the asset while it’s reserved.


## Result

A transfer order line is created along with a transfer order line task.

## What to do next

Close the transfer order line task to complete the task.

**Parent Topic:**[Transfer order tasks](../concept/work-with-transfer-orders.md)

**Related topics**  


[Create a transfer order](create-a-transfer-order.md)

[Close transfer order line task](move-transfer-order-line-through-stages.md)

