---
title: Create a transfer order line
description: Transfer order lines specify the exact items that comprise a transfer order.
locale: en-US
release: zurich
product: Asset Management
classification: asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Create a transfer order for Asset Management, Manage transfer order, Use, Asset Management, IT Asset Management]
---

# Create a transfer order line

Transfer order lines specify the exact items that comprise a transfer order.

## Before you begin

Role required: inventory\_user

## About this task

A transfer order can contain one or more transfer order lines. Under a single transfer order, all transfer order lines will have the same From location and To location. Each line contains an asset to transfer and the quantity to transfer. The item to transfer is identified by asset name and model name. A transfer order line can involve one quantity of a non-consumable asset or multiple quantities of a consumable asset. A bundled model can be transferred.

## Procedure

-   After creating a transfer order, click **New** in the **Transfer Order Lines** related list and fill in the fields as appropriate.

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


-   **[Create a customized template task](create-customized-template-task.md)**  
Create customized template tasks to configure your specific task workflow for transfer order lines. Default template tasks are available with the Asset Management application. You can’t modify or delete a default template task.
-   **[Create a template subtask](create-template-subtask.md)**  
Create template subtasks to add granularity to the transfer order line tasks. For example, before preparing for shipment, for a computer, you may want to create sub tasks for imaging the computer or adding additional software.

**Parent Topic:**[Create a transfer order for Asset Management](t_CreateATransferOrder.md)

