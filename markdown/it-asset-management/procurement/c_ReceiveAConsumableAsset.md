---
title: Consumable assets
description: A consumable asset is one that is purchased in quantity and distributed. It is assigned to the consumable model category, and the asset record tracks the quantity that is available and total cost. When consumable assets are received, they are merged into an existing consumable record, if available.
locale: en-US
release: australia
product: Procurement
classification: procurement
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Receive assets, Procurement, IT Asset Management]
---

# Consumable assets

A consumable asset is one that is purchased in quantity and distributed. It is assigned to the consumable model category, and the asset record tracks the quantity that is available and total cost. When consumable assets are received, they are merged into an existing consumable record, if available.

For the records to merge, the consumable cannot be listed on an active transfer order and the **Model**, **Location**, **Model Category**, **Stockroom**, **Status**, and **Substatus** fields on the asset record must match.

If consumables are merged into an existing consumable record, the cost of the additional consumables received is added to that of the existing consumables in the record. For example, if 50 computer keyboards arrive and 20 keyboards of the same model exists in the receiving stockroom, the two records are merged showing 70 keyboards in the stockroom with a combined total cost.

If no matching consumable record exists in the receiving stockroom, a record is created. After the consumables are received, the quantity is updated, but individual consumables are no longer tracked within the Procurement application and are not displayed on receiving slip lines.

**Note:** The related list of a purchase order doesn't display consumable asset details. This means that you can't track consumables through a purchase order.

For more details on creating consumable assets, see [Create consumable assets](../../asset-management/task/t_CreatingConsumableAssets.md).

**Parent Topic:**[Receive assets](c_ReceiveAssets.md)

**Related topics**  


[Receive an asset](../task/t_ReceiveAnAsset.md)

[Create a receiving slip](../task/t_CreateAReceivingSlip.md)

[Create a receiving slip line](../task/t_CreateAReceivingSlipLine.md)

