---
title: Consumables life cycle
description: Consumables are assets that are not tracked individually, but as a group of the same model.
locale: en-US
release: australia
product: Asset Management
classification: asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using Asset Management, Asset Management, IT Asset Management]
---

# Consumables life cycle

Consumables are assets that are not tracked individually, but as a group of the same model.

The group of consumables has one or more of the following traits.

-   Same location
-   Same state
-   Consumed by the same asset, typically as accessories or parts

Some common consumable assets include mouse devices, computer keyboards, and pencils. The base ServiceNow system includes the **Consumable** model category. The first step in working with models is to create a model within the model category for an individual consumable asset. Items such as monitors, keyboards, and mouse devices are often tracked as consumables. Consumables cannot be pre-allocated.

Consumable assets are stored in the Consumable \[alm\_consumable\] table. Consumables follow a slightly different life cycle from other assets.

## Stages of consumables

The consumable lifecycle stages are as follows.

-   On order
-   In stock
-   In transit
-   Consumed
-   In maintenance
-   Retired
-   Missing

-   **[View consumable assets](../task/t_ViewingConsumableAssets.md)**  
Consumables are tracked as a group of the same model, but you can view individual consumables in the consumable model record.
-   **[Create consumable assets](../task/t_CreatingConsumableAssets.md)**  
Create a consumable to track an asset as a group of the same model.
-   **[Consume consumable assets](../task/t_ConsumingConsumableAssets.md)**  
To consume consumable assets, they must have a state of **In Stock** and a substate of **Available**.
-   **[Return consumable assets to stockrooms](../../hardware-asset-management/task/return-consumables.md)**  
Move a consumable asset that is in a consumed state and has completed its life cycle back to an in-stock status.
-   **[Dispose of consumable assets](../../hardware-asset-management/task/dispose-consumables.md)**  
Dispose of those consumable assets that are no longer required in your stockrooms.

**Parent Topic:**[Using Asset Management](using-asset-management.md)

**Related topics**  


[Mobile app for Hardware Asset Management](../../../administer/mobile-my-asset/concept/mobile-my-asset.md)

[Work with Asset and CI](../../hardware-asset-management/concept/work-with-asset-ci.md)

[Manage various assets through asset classes](c_AssetClasses.md)

[Create fixed assets](c_CreatingFixedAssets.md#)

[Stockrooms](c_Stockrooms.md)

[Manage pre-allocated assets](../../hardware-asset-management/concept/manage-preallocated-asset.md)

[Manage transfer order](manage-transfer-orders.md)

[Example Asset Management process](../task/t_AssetManagementProcess.md)

[Use Organization Management](../reference/org-mgmt.md#)

