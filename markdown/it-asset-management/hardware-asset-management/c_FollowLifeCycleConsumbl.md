---
title: Consumables life cycle
description: Consumables are assets that are not tracked individually, but as a group of the same model.
locale: en-US
release: xanadu
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 7
breadcrumb: [Using Hardware Asset Management, Hardware Asset Management, IT Asset Management]
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
-   **[Plan disposal of consumable assets](../../hardware-asset-management/task/dispose-consumables.md)**  
Make the consumable assets that are no longer required in your stockrooms ready for disposal.

**Parent Topic:**[Using Hardware Asset Management](../../hardware-asset-management/concept/using-ham-classic.md)

**Related topics**  


[Work with hardware normalization](../../hardware-asset-management/concept/Work-with-hardware-normalization.md)

[Work with Asset and CI](../../hardware-asset-management/concept/work-with-asset-ci.md)

[Manage asset bundles from your inventory](../../hardware-asset-management/task/create-bundled-assets.md)

[Manage various assets through asset classes](c_AssetClasses.md)

[Manage your inventory through pallet assets](../../hardware-asset-management/concept/pallets-for-inventory-management.md)

[Create fixed assets](c_CreatingFixedAssets.md#)

[Manage pre-allocated assets](../../hardware-asset-management/concept/manage-preallocated-asset.md)

[Manage loaner assets](../../hardware-asset-management/task/manage-loaner-asset.md)

[Donate assets to charity organizations](../../hardware-asset-management/concept/donate-asset-to-charity-organizations.md)

[Exclude assets](../../hardware-asset-management/task/exclude-assets.md)

[Use Advanced Shipment Notification](../../hardware-asset-management/task/advanced-shipment-notification.md)

[Use Organization Management](../reference/org-mgmt.md#)

[Manage RMA requests](../../hardware-asset-management/concept/manage-rma-req.md)

[Create an inventory stock order request](../../hardware-asset-management/task/create-inventory-stock-order.md)

[Transfer orders for Asset Management](transfer-orders-for-am.md#)

[Create a transfer order for Asset Management](../task/t_CreateATransferOrder.md#)

[Transfer order line asset tracking](../reference/r_TransferOrderLineAssetTracking.md#)

[Create a disposal order](../../hardware-asset-management/task/create-disposal-order.md)

[Use a hardware asset request flow](../../hardware-asset-management/task/hardware-request-flow.md)

[Audit your inventory](../../hardware-asset-management/task/audit-your-inventory.md)

[Request a Hardware Asset Refresh](../../hardware-asset-management/task/hardware-asset-refresh.md#)

[Manage your expiring contracts for leased hardware assets](../../hardware-asset-management/task/manage-your-leased-hw-asts-expiring-contract.md)

[Reclaim hardware assets](../../hardware-asset-management/concept/manage-asset-reclaim.md)

[View RFID information of assets](../../hardware-asset-management/task/view-rfid-info.md)

[Manage the lifecycle of hardware models with calculated lifecycle templates](../../hardware-asset-management/concept/manage-ham-lifecycle-temp.md)

[Receive asset warranty details from Lenovo](../../hardware-asset-management/concept/receive-warranty-details-lenovo.md)

[Manage stockrooms](../../hardware-asset-management/concept/manage-your-stockrooms.md)

[Track shipments using the integration framework](../../hardware-asset-management/concept/tracking-shipments-using-integration-framework.md)

[Track asset location using indoor maps](../../hardware-asset-management/task/track-asset-location-using-indoor-maps.md)

[Assess performance of Hardware Asset Management](../../hardware-asset-management/concept/suc-goal-act-hw.md)

[Manage refresh of assets using Zero Touch Refresh](../../hardware-asset-management/concept/refresh-hardware-uisng-ztr.md)

[Configure the Total Cost of Ownership of assets](../../hardware-asset-management/concept/configure-ham-tco.md)

[Manage and monitor hardware asset performance](../../hardware-asset-management/concept/manage-and-monitor-hardware-asset-performance.md)

[Manage Hardware Asset Management subscriptions](../../hardware-asset-management/concept/managing-ham-subscriptions.md)

[Manage repair of defective assets in your stockroom in the Hardware Asset Workspace](../../hardware-asset-management/concept/manage-repair-of-defective-ham-assets.md)

[Manage picking hardware assets within your stockroom for Hardware Asset Management workflows](../../hardware-asset-management/concept/manage-asset-picking-stockroom-ham-ws.md)

[Manage asset put away using the Hardware Asset Workspace](../../hardware-asset-management/concept/manage-asset-putaway-stockroom-hardware-asset-workspace.md)

[Manage hardware asset tasks using the Mobile Agent application](../../hardware-asset-management/concept/manage-hardware-asset-tasks-mobile-agent.md)

[Acknowledge receipt of assets on the Employee Center portal](../../hardware-asset-management/task/receive-assets-employee-center.md)

[Update associated Decision tables for HAM flows](../../hardware-asset-management/task/trigger-flow-ham.md)

