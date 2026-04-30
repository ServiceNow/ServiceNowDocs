---
title: Hardware Asset Management license exclusion
description: Pay only for the assets using licensed Hardware Asset Management features and exclude an asset for which you don't want to use the licensed features.
locale: en-US
release: xanadu
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Exploring Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Hardware Asset Management license exclusion

Pay only for the assets using licensed Hardware Asset Management features and exclude an asset for which you don't want to use the licensed features.

Hardware asset features are restricted to hardware and consumable asset records. Use the asset level exclusion when you want to use Hardware Asset Management licensed features but want to exclude a few assets. For more information about excluding an asset, see [Exclude assets](../task/exclude-assets.md).

Hardware assets belonging to a category that you don't opt in are excluded by default. For example, if you don't opt in for the End User Computer category, all End user computers would be excluded. For more information, see [Opt-in or opt-out of HAM license resource categories](../task/optin-optout-ham-license-resource-categories.md).

You can't select and use the excluded assets in the following HAM flows and tasks:

-   [Loaner](loaner-asset.md#)
-   [Disposal](../task/create-disposal-order.md)
-   [Refresh](../task/hardware-asset-refresh.md#)
-   [Lease](../task/manage-your-leased-hw-asts-expiring-contract.md)
-   [Bundle](asset-bundles-concept.md)
-   [Return Merchandise Authorization \(RMA\)](../task/submit-rma-request.md)
-   [Audit](../task/audit-your-inventory.md)
-   [RFID](integrating-rfid.md)
-   [Asset lifecycle automation](asset-lifecycle-automation.md)
-   [Pallets](pallet-assets.md)
-   [Donation](asset-donation.md)

**Note:** Any workflow once started on an asset is allowed to complete even if the asset is marked excluded midway through.

