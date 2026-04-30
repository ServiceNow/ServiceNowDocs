---
title: Transfer order line asset tracking
description: As transfer order line actions are triggered, the stock information and states of any affected assets are updated. Consumables and non-consumables are tracked differently.
locale: en-US
release: zurich
product: Asset Management
classification: asset-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Manage transfer order, Use, Asset Management, IT Asset Management]
---

# Transfer order line asset tracking

As transfer order line actions are triggered, the stock information and states of any affected assets are updated. Consumables and non-consumables are tracked differently.

When an asset is included in a transfer order line, the following takes place:

-   A substate field on the asset form changes to reflect the transfer order line states
-   The Active TO option on the asset form is automatically selected to show that the asset is part of a transfer order and cannot be added to multiple transfer orders
-   The asset is removed from the pool of available assets and changed to a state of In Stock Pending Transfer

-   **[Transfer order line asset tracking of non-consumables](r_TrsferOrderLneAssetTrackNonConsum.md)**  
When transfer order line stages change for non-consumables, it affects asset substates.
-   **[Transfer order line asset tracking consumables](r_TrsferOrderLneAssetTrackConsum.md)**  
When a consumable is added to a transfer order line, the stock for the consumable is split into two records and the transfer order links to the newly created stock line.

**Parent Topic:**[Manage transfer order](../../hardware-asset-management/concept/manage-transfer-orders.md)

**Related topics**  


[Transfer order flow](../concept/transfer-order-flows.md)

[Transfer orders for Asset Management](../concept/transfer-orders-for-am.md)

[Create a transfer order for Asset Management](../task/t_CreateATransferOrder.md)

[Perform bulk updates for transfer order lines](../task/create-bulk-transfer.md)

[Delete a transfer order](../task/t_DeleteATransferOrder.md)

[Delete a transfer order line](../task/t_DeleteATransferOrderLine.md)

[Return items received in a transfer order](../task/t_ReturnItemsRecInXferOrder.md)

