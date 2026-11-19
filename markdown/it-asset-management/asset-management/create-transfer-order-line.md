---
title: Create a transfer order line
description: Create a transfer order line to specify the exact items that comprise a transfer order.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-asset-management/asset-management/create-transfer-order-line.html
release: zurich
product: Asset Management
classification: asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Transfer order tasks, Manage transfer order, Use, Asset Management, IT Asset Management]
---

# Create a transfer order line

Create a transfer order line to specify the exact items that comprise a transfer order.

## Before you begin

Role required: inventory\_user

## About this task

A transfer order can contain one or more transfer order lines. Under a single transfer order, all transfer order lines have the same From location and To location. Each line contains an asset to transfer and the quantity to transfer. The item to transfer is identified by asset name and model name. A transfer order line can involve one quantity of a non-consumable asset or multiple quantities of a consumable asset. A bundled model can be transferred.

## Procedure

1.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Number|Unique number identifying the transfer order line.|
    |Stage|Current stage of the transfer order. Transfer order lines can only be created when a transfer order is in Draft stage.|
    |Transfer order|The transfer order to which the transfer order line belongs.|
    |Request line|Requested item to associate with the transfer order line.|
    |Model|Model of the items requested by the transfer order line. For example, a printer. If the Asset field is filled out first, the Model field is automatically filled in with the model corresponding to the asset.|
    |Asset|Asset requested by the transfer order line. For example, a specific printer. The asset can filter on stockrooms.|
    |Quantity requested|Number of items requested by the transfer order line. For example, 3 computers are requested to be transferred.|
    |Quantity remaining|Number of items yet to be received. For example, 3 keyboards had been requested, 2 are received, 1 is remaining.|
    |Quantity received|Number of items already received. For example, 3 keyboards are transferred, 2 are received.|
    |Quantity returned|Number of items that already needed to be returned.|

2.  Select **Save**.


**Parent Topic:**[Transfer order tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/asset-management/work-with-transfer-orders.md)

