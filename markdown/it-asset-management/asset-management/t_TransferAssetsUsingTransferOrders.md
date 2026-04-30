---
title: Transfer assets using transfer orders
description: Transfer assets from one location to the other by moving the assets through the transfer order process. Transfer order lines specify the exact items that comprise a transfer order.
locale: en-US
release: yokohama
product: Asset Management
classification: asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Transfer orders for Asset Management, Manage transfer order, Using Asset Management, Asset Management, IT Asset Management]
---

# Transfer assets using transfer orders

Transfer assets from one location to the other by moving the assets through the transfer order process. Transfer order lines specify the exact items that comprise a transfer order.

## Before you begin

Role required: inventory\_user

The inventory\_user, asset, or procurement\_user role can only access the Transfer Order \[alm\_transfer\_order\] reports. You must activate the Procurement \(com.snc.procurement\) plugin for the inventory\_user, asset, and procurement\_user roles.

## About this task

You create a transfer order and move it from its initial **Draft** status to the final **Received** status. A transfer order can contain one or more transfer order lines. Under a single transfer order, all transfer order lines have the same From location and To location. Each line contains an asset to transfer and the quantity to transfer. The item to transfer is identified by asset name and model name. A transfer order line can involve one quantity of a non-consumable asset or multiple quantities of a consumable asset. A bundled model can be transferred.

## Procedure

1.  Complete the following steps to create a transfer order.

    1.  Navigate to **All** &gt; **Inventory** &gt; **Transfer Orders** &gt; **Create Transfer Order**.

    2.  In the **From Stockroom** list, select a stockroom from which you want to ship the items.

    3.  In the **To Stockroom** list, select a stockroom where you want to ship the items.

        **Note:** If you select the same stockroom in both the From Stockroom and To Stockroom fields, the transfer order automatically moves from **Draft** to **Received** when a transfer order line is added.

    4.  Select a date and time for the delivery from the **Delivery by date** date picker.

    5.  Select **Submit**.

    Transfer order record is created.

2.  Complete the following steps to create a transfer order line under the transfer order.

    1.  Navigate to **All** &gt; **Inventory** &gt; **Transfer Orders** and open the transfer order.

    2.  Next to **Transfer Order Lines**, select **New**.

    3.  On the Create transfer order line form, fill in the fields.

        For a description of the field values, see [Transfer order line fields](../reference/transfer-order-line-fields.md).

    4.  If the model is a consumable, specify a quantity in **Quantity Requested**.

    5.  Select **Submit**.

        After creating transfer order lines, the transfer order and all the transfer order lines are in the draft stage. While a transfer order or a transfer order line is in the draft stage, it can be deleted.

        **Note:** When an asset is part of a transfer order set to **Draft**, the asset record updates to show the asset as reserved. You can't request or transfer the asset while it’s reserved.

        A transfer order line is created along with a transfer order line task.

3.  Open the transfer order line task and select **Close Task**.

    The transfer order line task is completed and a new transfer order line task is opened.


## What to do next

Keep closing each task until you reach the last stage \(**Received**\). After you close the task for the Received stage, the transfer order line is completed and closed. All transfer order lines and the transfer order are marked **Delivered**.

**Parent Topic:**[Transfer orders for Asset Management](../concept/transfer-orders-for-am.md)

**Related topics**  


[Summary of transfer order line tasks](../reference/r_SummaryOfTransferOrderStages.md)

[Transfer order line fields](../reference/transfer-order-line-fields.md)

