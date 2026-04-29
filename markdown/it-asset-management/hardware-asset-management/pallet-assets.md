---
title: Pallet assets
description: Use the Pallet asset class to track and manage assets in your inventory as a group. You can easily move a group of assets between locations or dispose of them as a group.
locale: en-US
release: australia
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Exploring Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Pallet assets

Use the Pallet asset class to track and manage assets in your inventory as a group. You can easily move a group of assets between locations or dispose of them as a group.

A pallet is an asset with the model category Pallet. Pallets are the parent of the assets contained in them. The predefined pallet types are pallet, bin, box, and container.

**Note:** The Pallet asset class with its associated UI options are available only with the Hardware Asset Management Professional plugin \(com.sn\_hamp\).

You can create a pallet asset and add base, hardware, bundle, consumables, and other pallet assets to the pallet in the Asset Estate view.

Pallet assets aren't associated with any expense lines.

The Pallet \[alm\_pallet\] table stores information about pallet assets. The location of a pallet in the stockroom is indicated by the **Aisle** and **Space** columns of the Asset \[alm\_asset\] table.

Note the following when you plan to use pallet assets for inventory management:

-   You can't add software, enterprise, and excluded assets to a pallet.

    **Note:** For information on excluded assets, see [Hardware Asset Management license exclusion](ham-license-exclusion.md).

-   You can't add an asset that is already associated to a parent asset.
-   Pallet assets can't be a part of asset bundles.

For more details on pallet assets, see [Manage your inventory through pallet assets](pallets-for-inventory-management.md).

