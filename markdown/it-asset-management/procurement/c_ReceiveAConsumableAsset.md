---
title: Consumable assets
description: A consumable asset is one that is purchased in quantity and distributed. It is assigned to the consumable model category, and the asset record tracks the quantity that is available and total cost. When consumable assets are received, they are merged into an existing consumable record, if available.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/it-asset-management/procurement/c\_ReceiveAConsumableAsset.html
release: yokohama
product: Procurement
classification: procurement
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Receive assets, Procurement, IT Asset Management]
---

# Consumable assets

A consumable asset is one that is purchased in quantity and distributed. It is assigned to the consumable model category, and the asset record tracks the quantity that is available and total cost. When consumable assets are received, they are merged into an existing consumable record, if available.

For records to merge, the consumable can't be listed on an active transfer order. When a record is eligible for merge, the merge process identifies an existing consumable record that matches on all of the following base fields:

-   Model
-   Location
-   Model category
-   Stockroom
-   Install status
-   Substatus
-   Parent
-   Asset function
-   Assigned to
-   Domain \(for multi-domain instances\)
-   Active-to \(matched as true, or as false-or-empty\)
-   Planned-for-disposal \(matched as false or empty\)

If consumables are merged into an existing consumable record, the cost of the additional consumables received is added to that of the existing consumables in the record. For example, if 50 computer keyboards arrive and 20 keyboards of the same model exists in the receiving stockroom, the two records are merged showing 70 keyboards in the stockroom with a combined total cost.

If no matching consumable record exists in the receiving stockroom, a record is created. After the consumables are received, the quantity is updated, but individual consumables are no longer tracked within the Procurement application and are not displayed on receiving slip lines.

**Note:** The related list of a purchase order doesn't display consumable asset details. This means that you can't track consumables through a purchase order.

For more details on creating consumable assets, see [Create consumable assets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-asset-management/asset-management/t_CreatingConsumableAssets.md).

**Parent Topic:**[Receive assets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-asset-management/procurement/c_ReceiveAssets.md)

**Related topics**  


[Receive an asset]()

[Create a receiving slip]()

[Create a receiving slip line]()

