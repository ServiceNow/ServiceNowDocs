---
title: Create transfer order lines in Enterprise Asset Workspace
description: Create transfer order lines in Enterprise Asset Management to specify the items that comprise a transfer order.
locale: en-US
release: yokohama
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Create a transfer order in Enterprise Asset Workspace, Create and manage enterprise asset inventory, Managing enterprise asset inventory and contracts, Enterprise Asset Management, IT Asset Management]
---

# Create transfer order lines in Enterprise Asset Workspace

Create transfer order lines in Enterprise Asset Management to specify the items that comprise a transfer order.

## Before you begin

Role required: sn\_eam.enterprise\_admin or sn\_eam.enterptrise\_asset\_manager

## About this task

A transfer order can contain one or more transfer order lines. Under a single transfer order, all transfer order lines have the same **From location** and **To location**. Each line contains an asset to transfer and the quantity to transfer. The item to transfer is identified by the asset name and the model name. A transfer order line can involve one quantity of a non-consumable asset or multiple quantities of a consumable asset.

## Procedure

1.  Navigate to the transfer order in the Enterprise Asset Workspace.

2.  In the transfer order, select the **Transfer Order Lines** tab

    The Transfer Order Lines page appears.

3.  Select **New**.

4.  On the form, fill in the details

    |Field|Description|
    |-----|-----------|
    |Number|Internal unique number identifying the transfer order line.|
    |Transfer Order|The transfer order to which the transfer order line belongs.|
    |Model|Model of the items requested by the transfer order line. For example, a printer. If the Asset field is filled out first, the Model field is automatically filled in with the model corresponding to the asset.|
    |Quantity requested|Number of items requested by the transfer order line. For example, 3 computers are requested to be transferred.|
    |Quantity received|Number of items already received. For example, 3 keyboards are transferred, 2 are received.|
    |Stage|Current stage of the transfer order. Transfer order lines can only be created when a transfer order is in **Draft** stage.|
    |Request line|Requested item to associate with the transfer order line.|
    |Asset|Asset requested by the transfer order line. For example, a specific printer. The asset can filter on stockrooms.|
    |Quantity remaining|Number of items yet to be received. For example, 3 keyboards had been requested, 2 are received, 1 is remaining.|
    |Quantity returned|Number of items that already needed to be returned.|

5.  Select **Save**.

    The Transfer Order Line is created and displays the **Transfer Order Line Tasks** tab. Transfer order line tasks are created to move transfer order lines from one stage to the other.


**Parent Topic:**[Create a transfer order in Enterprise Asset Workspace](create-eam-transferorder.md)

