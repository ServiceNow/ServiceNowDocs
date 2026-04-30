---
title: Manage asset bundles from your inventory
description: Create asset bundles from existing assets in your inventory to track, reserve, or deploy a group of assets as a single entity.
locale: en-US
release: xanadu
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 9
breadcrumb: [Using Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Manage asset bundles from your inventory

Create asset bundles from existing assets in your inventory to track, reserve, or deploy a group of assets as a single entity.

## Before you begin

An asset bundle is a grouping of assets and comprises of consumable and hardware assets. Only assets that are in the **In stock** status and **available** substatus are added to an asset bundle. Assets that are part of an asset bundle aren’t available as individual assets.

**Note:** For information on asset bundles, see [Asset bundles](../concept/asset-bundles-concept.md).

Role required: asset

## Procedure

1.  Navigate to **All** &gt; **Asset** &gt; **Bundled Assets**.

2.  Select **New**.

    The model category defaults to **Bundle** and the state defaults to **Build**. The build state is associated to only the **Bundle** model category. The build state is not valid for assets.

3.  In the Bundle form layout, select a product model from the **Model** list.

4.  In the **Stockroom** field, select a stockroom from where the assets are sourced for the bundle.

5.  Automatically add assets to your bundle by selecting **Auto-allocate assets** or add specific assets by selecting **Select assets**:

    -   **Auto-select assets**: Automatically adds assets to the asset bundle. The assets are added from the stockroom specified in the asset bundle.

        **Note:** Assets are allocated only when all the assets that are part of the bundle are available. Excluded assets aren't considered for auto-selection. For more information about asset exclusion, see [Hardware Asset Management license exclusion](../concept/ham-license-exclusion.md).

    -   **Select assets**: Select the assets that you want in your asset bundle and select **Add Assets**.

        **Note:**

        You can't select an excluded asset. For more information about asset exclusion, see [Hardware Asset Management license exclusion](../concept/ham-license-exclusion.md). Assets displayed are confined to the stockroom specified in the asset bundle.

    Once the assets are allocated to the bundle, the assets appear in the Assets related list and **Auto-allocate assets** and **Select assets** no longer appear in the Bundle form layout.

    **Note:** You must include all the assets to the asset bundle that are associated with the bundled model as a model component. If any asset isn’t included, the bundle asset is considered incomplete, and the **State** field value of the bundle asset can’t be changed.

6.  Select **Save**.

    The asset bundle is created. The cost of the bundled model is stamped on the asset bundle and on the expense line of the asset bundle. The cost isn’t the cumulative cost of all the model components of the bundled model.

7.  You can swap assets from an asset bundle by selecting **Replace assets**.

    Assets belonging to an asset bundle can be swapped when the state of the bundle is **In maintenance** or **In stock** \(substate **Pending repair**\).

    1.  In the Replace assets dialog box, select the assets you want to swap.

    2.  Select the asset that you want to swap the current asset with.

    3.  Select **Replace**.

        The asset that was swapped is returned to the stockroom.

8.  You can delete an asset bundle by selecting **Delete**.

    You must disassociate assets from an asset bundle to delete the bundle. Once all the assets are released from the bundle, you can delete the bundle.

    1.  In the **State** field, select **Retired**.

    2.  Select **Save**.

    3.  Select the **Release Assets** related link

    4.  In the confirmation dialog box, select **Release assets**.

        All the assets are disassociated from the asset bundle and are moved to a stockroom.

    5.  Select **Delete**.

        The asset bundle is deleted.


**Parent Topic:**[Using Hardware Asset Management](../concept/using-ham-classic.md)

**Related topics**  


[Work with hardware normalization](../concept/Work-with-hardware-normalization.md)

[Work with Asset and CI](../concept/work-with-asset-ci.md)

[Consumables life cycle](../../asset-management/concept/c_FollowLifeCycleConsumbl.md)

[Manage various assets through asset classes](../../asset-management/concept/c_AssetClasses.md)

[Manage your inventory through pallet assets](../concept/pallets-for-inventory-management.md)

[Create fixed assets](../../asset-management/concept/c_CreatingFixedAssets.md#)

[Manage pre-allocated assets](../concept/manage-preallocated-asset.md)

[Manage loaner assets](manage-loaner-asset.md)

[Donate assets to charity organizations](../concept/donate-asset-to-charity-organizations.md)

[Exclude assets](exclude-assets.md)

[Use Advanced Shipment Notification](advanced-shipment-notification.md)

[Use Organization Management](../../asset-management/reference/org-mgmt.md#)

[Manage RMA requests](../concept/manage-rma-req.md)

[Create an inventory stock order request](create-inventory-stock-order.md)

[Transfer orders for Asset Management](../../asset-management/concept/transfer-orders-for-am.md#)

[Create a transfer order for Asset Management](../../asset-management/task/t_CreateATransferOrder.md#)

[Transfer order line asset tracking](../../asset-management/reference/r_TransferOrderLineAssetTracking.md#)

[Create a disposal order](create-disposal-order.md)

[Use a hardware asset request flow](hardware-request-flow.md)

[Audit your inventory](audit-your-inventory.md)

[Request a Hardware Asset Refresh](hardware-asset-refresh.md#)

[Manage your expiring contracts for leased hardware assets](manage-your-leased-hw-asts-expiring-contract.md)

[Reclaim hardware assets](../concept/manage-asset-reclaim.md)

[View RFID information of assets](view-rfid-info.md)

[Manage the lifecycle of hardware models with calculated lifecycle templates](../concept/manage-ham-lifecycle-temp.md)

[Receive asset warranty details from Lenovo](../concept/receive-warranty-details-lenovo.md)

[Manage stockrooms](../concept/manage-your-stockrooms.md)

[Track shipments using the integration framework](../concept/tracking-shipments-using-integration-framework.md)

[Track asset location using indoor maps](track-asset-location-using-indoor-maps.md)

[Assess performance of Hardware Asset Management](../concept/suc-goal-act-hw.md)

[Manage refresh of assets using Zero Touch Refresh](../concept/refresh-hardware-uisng-ztr.md)

[Configure the Total Cost of Ownership of assets](../concept/configure-ham-tco.md)

[Manage and monitor hardware asset performance](../concept/manage-and-monitor-hardware-asset-performance.md)

[Manage Hardware Asset Management subscriptions](../concept/managing-ham-subscriptions.md)

[Manage repair of defective assets in your stockroom in the Hardware Asset Workspace](../concept/manage-repair-of-defective-ham-assets.md)

[Manage picking hardware assets within your stockroom for Hardware Asset Management workflows](../concept/manage-asset-picking-stockroom-ham-ws.md)

[Manage asset put away using the Hardware Asset Workspace](../concept/manage-asset-putaway-stockroom-hardware-asset-workspace.md)

[Manage hardware asset tasks using the Mobile Agent application](../concept/manage-hardware-asset-tasks-mobile-agent.md)

[Acknowledge receipt of assets on the Employee Center portal](receive-assets-employee-center.md)

[Update associated Decision tables for HAM flows](trigger-flow-ham.md)

