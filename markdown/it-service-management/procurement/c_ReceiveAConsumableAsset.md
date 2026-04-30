---
title: Consumable assets
description: A consumable asset is one that is purchased in quantity and distributed. It is assigned to the consumable model category, and the asset record tracks the quantity that is available and total cost. When consumable assets are received, they are merged into an existing consumable record, if available.
locale: en-US
release: xanadu
product: Procurement
classification: procurement
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Procurement purchase order management for assets, Procurement, Asset Management, IT Service Management]
---

# Consumable assets

A consumable asset is one that is purchased in quantity and distributed. It is assigned to the consumable model category, and the asset record tracks the quantity that is available and total cost. When consumable assets are received, they are merged into an existing consumable record, if available.

For the records to merge, the consumable cannot be listed on an active transfer order and the **Model**, **Location**, **Model Category**, **Stockroom**, **Status**, and **Substatus** fields on the asset record must match.

If consumables are merged into an existing consumable record, the cost of the additional consumables received is added to that of the existing consumables in the record. For example, if 50 computer keyboards arrive and 20 keyboards of the same model exists in the receiving stockroom, the two records are merged showing 70 keyboards in the stockroom with a combined total cost.

If no matching consumable record exists in the receiving stockroom, a record is created. After the consumables are received, the quantity is updated, but individual consumables are no longer tracked within the Procurement application and are not displayed on receiving slip lines.

**Note:** The related list of a purchase order doesn't display consumable asset details. This means that you can't track consumables through a purchase order.

For more details on creating consumable assets, see [Create consumable assets](../../asset-management/concept/c_FollowLifeCycleConsumbl.md#).

**Parent Topic:**[Procurement purchase order management for assets](c_UseProcurement.md)

**Related topics**  


[Track a request from the service catalog](../task/t_TrackReqFromServiceCatalog.md)

[Cancel a request from the service catalog](../task/t_CancelReqFromServCatalog.md)

[View and edit a catalog task](../task/t_ViewAndEditACatalogTask.md)

[Create a purchase order](../task/t_CreateAPurchaseOrder.md)

[Create an asset and reserve it for the requester](../task/t_CreateAssetReserveForRequester.md)

