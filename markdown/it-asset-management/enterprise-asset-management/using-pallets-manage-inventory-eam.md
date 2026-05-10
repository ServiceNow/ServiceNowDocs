---
title: Using pallet assets to manage your asset inventory in the Enterprise Asset Workspace
description: You can manage your asset inventory by using pallets and the assets contained within those pallets in your transfer orders, disposal orders, resale orders, and various consumption workflows.
locale: en-US
release: australia
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Create pallet assets in the Enterprise Asset Workspace, Create and manage enterprise assets, Managing enterprise models and assets, Enterprise Asset Management, IT Asset Management]
---

# Using pallet assets to manage your asset inventory in the Enterprise Asset Workspace

You can manage your asset inventory by using pallets and the assets contained within those pallets in your transfer orders, disposal orders, resale orders, and various consumption workflows.

## Moving pallets between stockrooms

You can use transfer orders to move in-stock pallets from one stockroom to another. If you’re moving a pallet that contains assets, those assets are also moved as part of the same transfer order. If you move only the assets that are contained within a pallet, those assets are automatically removed from the corresponding pallet asset record after the Ready for fulfillment task is closed.

For more information about transfer orders, see [Create a transfer order in Enterprise Asset Workspace](../task/create-eam-transferorder.md).

## Disposing of pallets

When a pallet is nearing the end of its life cycle or is no longer functional, you can dispose of it using a disposal order. If the pallet contains any assets, you can choose to dispose of the pallet and its assets using any of the following options:

**Note:** You can dispose of only the enterprise assets and enterprise-based consumable assets that are contained within your pallets. If a pallet contains any hardware, bundle, or hardware-based consumable assets, those assets are automatically updated with a State of Invalid and can’t be processed as part of a disposal order.

-   Dispose of both the pallet and all assets that are contained within that pallet.
-   Dispose of both the pallet and only certain assets that are contained within that pallet. Any assets that you choose to retain are automatically removed from the corresponding pallet asset record.
-   Dispose of the pallet but retain all assets that are contained within that pallet. If you select this option, all assets are automatically removed from the corresponding pallet asset record.
-   Retain the pallet but dispose of all assets that are contained within that pallet. If you select this option, all assets are automatically removed from the corresponding pallet asset record.
-   Retain the pallet but dispose of only certain assets that are contained within that pallet. Any assets that you dispose of are automatically removed from the corresponding pallet asset record.

For more information about disposal orders, see [Create a disposal order in the Enterprise Asset Workspace](../task/create-eamdisposal-order.md).

## Reselling pallets

To help reduce waste and save costs, you can use resale orders to resell any pallets that you’re no longer using. If a pallet contains any assets, you can choose to resell the pallet and its assets using any of the following options:

**Note:** You can’t resell any hardware assets, asset bundles, and non-enterprise consumable assets that are contained within your pallets.

-   Resell both the pallet and all assets that are contained within that pallet.
-   Resell both the pallet and only certain assets that are contained within that pallet. Any assets that you choose to retain are automatically removed from the corresponding pallet asset record.
-   Resell the pallet but retain all assets that are contained within that pallet. If you select this option, all assets are automatically removed from the corresponding pallet asset record.
-   Retain the pallet but resell all assets that are contained within that pallet. If you select this option, all assets are automatically removed from the corresponding pallet asset record.
-   Retain the pallet but resell only certain assets that are contained within that pallet. Any assets that you resell are automatically removed from the corresponding pallet asset record.

For more information on resale orders, see [Create an asset resale flow](../task/enterprise-asset-resale-flow.md).

## Consuming assets within a pallet

Assets that are contained within a pallet can be consumed through various asset workflows.

-   **Return Merchandise Authorization \(RMA\) flow**

    A Return Merchandise Authorization \(RMA\) is an agreement between a buyer and seller that allows the buyer to return, replace, or request the repair of a defective product within the specified warranty period. When an asset within a pallet becomes defective, you can initiate its replacement or repair by using an RMA order. Any assets that you include in an RMA order are automatically removed from the corresponding pallet asset record.

    For more information about RMA orders, see [Requesting a Return Merchandise Authorization \(RMA\) for defective enterprise assets](requesting-return-merchandise-authorization-enterprise-assets.md).

-   **Local Order subflow**

    You can source and fulfill asset requests using assets that are available in the requester's local stockroom. When an asset within a pallet is sourced and consumed locally as part of an asset request, it’s automatically removed from the corresponding pallet asset record after the Enterprise Confirm asset task is closed.

    For more information on sourcing assets from local stockrooms, see [Source requests from Enterprise Asset workspace](../task/source-requests-from-workspace.md).

-   **Loaner Request flow**

    If you need to use an asset for only a short period of time, you can request to loan that asset by using a loaner request. When an asset within a pallet is loaned out, it’s removed from the corresponding pallet asset record after the Prepare task for the loaner request is closed.

    For more information on loaning assets, see [Request a loaner asset in Enterprise Asset Workspace](../task/request-eam-assetloaner-request.md).

-   **Leased Asset Return flow**

    If a contract for a leased asset is nearing its expiration, you can return the leased asset to the asset vendor before incurring any penalty fees. When a leased asset within a pallet is returned to the asset vendor, it is automatically removed from the corresponding pallet asset record after the Shipment task for the asset is closed.

    For more information about returning leased assets, see [Return a leased enterprise asset](../task/return-leased-enterprise-asset.md).

-   **Swap tasks from the IT Service Management Asset Management application**

    The ServiceNow® Asset Management application enables you to track and manage your assets. If you use the application to swap an asset within a pallet, that asset is automatically removed from the corresponding pallet asset record after it’s swapped.

    For more information on the Asset Management application, see [Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/asset-management/c_AssetManagement.md).


**Parent Topic:**[Create pallet assets in the Enterprise Asset Workspace](../task/create-pallet-asset-eam.md)

