---
title: Using pallet assets for managing inventory
description: You can add a pallet with the assets contained in it to transfer orders and disposal orders to manage your inventory effectively.
locale: en-US
release: australia
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Manage your inventory through pallet assets, Using Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Using pallet assets for managing inventory

You can add a pallet with the assets contained in it to transfer orders and disposal orders to manage your inventory effectively.

## Moving pallets from one stockroom to another

Move an in-stock pallet along with the assets contained in it from one stockroom to another by using transfer orders. When you move only the assets contained in a pallet, the assets are removed from the pallet after the Ready for fulfillment task is closed. You can also use a transfer order to move an empty pallet.

Updates that you perform on the pallet as part of the transfer order workflow are applicable to the assets contained in it.

If there's a problem with all or some of the assets you receive as part of a transfer order, you can return the pallet along with its assets. You can't return individual assets contained in the pallet.

For more information, see [Transfer assets using transfer orders](../../asset-management/task/t_TransferAssetsUsingTransferOrders.md).

## Disposing of pallets

Dispose of a pallet with its assets that are reaching the end of the life cycle or that aren’t functional by using a disposal order. When you add a pallet to a disposal order, the assets and child assets in the pallet are also added. However, any asset bundles in the pallet are not included.

The disposal order workflow when disposing of a pallet or its assets is as follows:

-   Disposing of the pallet with the assets contained it: The verified pallet and its assets are disposed.
-   Disposing of only the assets and retaining the pallet: The assets are removed from the pallet after they're verified.
-   Disposing of the pallet with only some of its assets and retaining the remaining assets: The assets that weren't verified or disposed of are removed from the pallet automatically.

For more information, see [Create a disposal order](../task/create-disposal-order.md).

## Consuming assets from a pallet

**Note:** When an asset from the pallet is consumed as part of any workflow, the asset is automatically removed from the pallet.

Assets contained in a pallet can also be consumed as part of the following workflows:

-   [Return Merchandise Autorization \(RMA\)](return-merchandise-authorization.md): When an asset from a pallet is added to RMA, the asset is immediately removed from the pallet.

    **Note:** In an RMA request with an off-site replacement or repair, the assets that are in the pallet aren't shown in the Replacement asset field on the Receive task form.

-   [Asset Local Stock](https://www.servicenow.com/docs/access?context=consume-local-asset-stock&version=australia&pubname=australia-it-service-management&ft:locale=en-US): When an asset from the pallet is consumed as part of the local stock, the asset is removed from the pallet after the Confirm assigned asset task is closed.
-   [Loaner](loaner-asset.md#): When an asset from a pallet is consumed as a Loaner asset, the asset is removed from the pallet after the Prepare task of the loaner order is closed.
-   [Return leased assets](../task/return-your-leased-hardware-asset.md): When a leased asset from a pallet is returned, the asset is removed from the pallet after the Shipment task is closed.
-   Swap and deploy tasks from ITSM: When deploy asset action is triggered from ITSM, the asset that must be deployed is removed from the pallet. When swap action is triggered from ITSM, the asset in the pallet that is a replacement for a faulty asset is removed from the pallet.

**Parent Topic:**[Manage your inventory through pallet assets](pallets-for-inventory-management.md)

**Related topics**  


[Create pallet assets](../task/create-pallet-assets.md)

[Add assets to a pallet](../task/add-assets-to-pallet.md)

[Remove assets from a pallet](../task/remove-assets-from-pallet.md)

[Delete pallet assets](../task/delete-pallet-assets.md)

