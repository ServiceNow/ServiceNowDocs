---
title: Add assets to a pallet
description: Add base, hardware, bundle, consumable, and other pallet assets to an in-stock pallet to track and manage the assets in a stockroom as a group.
locale: en-US
release: yokohama
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Manage your inventory through pallet assets, Using Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Add assets to a pallet

Add base, hardware, bundle, consumable, and other pallet assets to an in-stock pallet to track and manage the assets in a stockroom as a group.

## Before you begin

Role required: asset

## About this task

You can add assets to a pallet only under the following conditions:

-   The asset belongs to the same stockroom as the pallet or has no value set in the **Stockroom** field.

-   The pallet **State** field value is In stock.

-   The asset **State** field value is one of the following:

    -   On order
    -   In stock
    -   In transit
    -   Retired
-   The asset isn’t associated to another parent asset.

    Either remove the existing parent-child association and then add the asset to the pallet or directly add the pallet as parent to the asset.


When an asset that is a parent to other assets is added to a pallet, all its child assets are also added. However, the parent field of the child assets isn’t replaced with details of the pallet.

## Procedure

1.  Navigate to **All** &gt; **Hardware Asset Workspace** &gt; **Asset estate**.

2.  Select the **Pallets** tab.

3.  Select the pallet to which you want to add assets.

4.  Select the **Assets** tab.

5.  Add base, hardware, and bundle assets to the pallet.

    1.  Select **Add assets**.

    2.  In the Add assets dialog box, select the assets that you want to add.

        You can use the filter to narrow the list of available assets.

    3.  Select **Add**.

    The assets that you added to the pallet are added to the list shown in the Assets tab. The state, substate, location, stockroom, aisle, and space details of the assets are synced with the pallet.

    **Note:** Only the substate of pre-allocated assets isn't synced with the pallet. For more information, see [Create pre-allocated assets](../../asset-management/task/t_CreatingPreAllocatedAssets.md#).

6.  Add consumable assets to the pallet.

    1.  Select **Add consumables**.

    2.  In the Add consumable to pallet dialog box, select the consumable from the list of available consumables or search for it.

    3.  In the **Quantity** field, either accept the default field value of the maximum available quantity of the selected consumable or modify the value to the number of consumables you want to add.

    4.  Select **Add**.

    The consumable asset that you added to the pallet is added to the list shown in the Assets tab.


**Parent Topic:**[Manage your inventory through pallet assets](../concept/pallets-for-inventory-management.md)

**Related topics**  


[Create pallet assets](create-pallet-assets.md)

[Remove assets from a pallet](remove-assets-from-pallet.md)

[Delete pallet assets](delete-pallet-assets.md)

[Using pallet assets for managing inventory](../concept/using-pallet-assets-for-inventory-mgmt.md)

