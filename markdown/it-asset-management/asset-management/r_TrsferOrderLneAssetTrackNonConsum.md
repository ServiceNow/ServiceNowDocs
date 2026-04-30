---
title: Transfer order line asset tracking of non-consumables
description: When transfer order line stages change for non-consumables, it affects asset substates.
locale: en-US
release: zurich
product: Asset Management
classification: asset-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Transfer order line asset tracking, Manage transfer order, Use, Asset Management, IT Asset Management]
---

# Transfer order line asset tracking of non-consumables

When transfer order line stages change for non-consumables, it affects asset substates.

|Transfer order line stage|Affect on asset substate|
|-------------------------|------------------------|
|Draft|Asset moves to **In Stock** &gt; **Pending Transfer** \(from the current stockroom\). If the asset is a consumable, the quantity can be edited.|
|Requested|Asset stays in **In Stock** &gt; **Pending Transfer**.|
|Shipment Preparation|Asset stays in **In Stock** &gt; **Pending transfer**.|
|In Transit|Asset moves to **In Transit** &gt; **Reserved**.|
|Received|Asset moves to **In Stock** &gt; **Available** \(in the destination stockroom\).|
|Delivered|Asset moves to **In Stock** &gt; **Reserved**.|

**Parent Topic:**[Transfer order line asset tracking](r_TransferOrderLineAssetTracking.md)

**Related topics**  


[Delete a transfer order](../task/t_DeleteATransferOrder.md)

[Delete a transfer order line](../task/t_DeleteATransferOrderLine.md)

[Return items received in a transfer order](../task/t_ReturnItemsRecInXferOrder.md)

