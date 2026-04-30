---
title: Transfer order line asset tracking
description: As transfer order line actions are triggered, the stock information and states of any affected assets are updated. Consumables and non-consumables are tracked differently.When transfer order line stages change for non-consumables, it affects asset substates.When a consumable is added to a transfer order line, the stock for the consumable is split into two records and the transfer order links to the newly created stock line.
locale: en-US
release: xanadu
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 9
breadcrumb: [Using Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Transfer order line asset tracking

As transfer order line actions are triggered, the stock information and states of any affected assets are updated. Consumables and non-consumables are tracked differently.

When an asset is included in a transfer order line, the following takes place:

-   A substate field on the asset form changes to reflect the transfer order line states
-   The Active TO option on the asset form is automatically selected to show that the asset is part of a transfer order and cannot be added to multiple transfer orders
-   The asset is removed from the pool of available assets and changed to a state of In Stock Pending Transfer

**Parent Topic:**[Using Hardware Asset Management](../../hardware-asset-management/concept/using-ham-classic.md)

**Related topics**  


[Work with hardware normalization](../../hardware-asset-management/concept/Work-with-hardware-normalization.md)

[Work with Asset and CI](../../hardware-asset-management/concept/work-with-asset-ci.md)

[Consumables life cycle](../concept/c_FollowLifeCycleConsumbl.md)

[Manage asset bundles from your inventory](../../hardware-asset-management/task/create-bundled-assets.md)

[Manage various assets through asset classes](../concept/c_AssetClasses.md)

[Manage your inventory through pallet assets](../../hardware-asset-management/concept/pallets-for-inventory-management.md)

[Create fixed assets](../concept/c_CreatingFixedAssets.md#)

[Manage pre-allocated assets](../../hardware-asset-management/concept/manage-preallocated-asset.md)

[Manage loaner assets](../../hardware-asset-management/task/manage-loaner-asset.md)

[Donate assets to charity organizations](../../hardware-asset-management/concept/donate-asset-to-charity-organizations.md)

[Exclude assets](../../hardware-asset-management/task/exclude-assets.md)

[Use Advanced Shipment Notification](../../hardware-asset-management/task/advanced-shipment-notification.md)

[Use Organization Management](org-mgmt.md#)

[Manage RMA requests](../../hardware-asset-management/concept/manage-rma-req.md)

[Create an inventory stock order request](../../hardware-asset-management/task/create-inventory-stock-order.md)

[Transfer orders for Asset Management](../concept/transfer-orders-for-am.md#)

[Create a transfer order for Asset Management](../task/t_CreateATransferOrder.md#)

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

[Delete a transfer order](../concept/transfer-orders-for-am.md#)

[Delete a transfer order line](../concept/transfer-orders-for-am.md#)

[Return items received in a transfer order](../concept/transfer-orders-for-am.md#)

## Transfer order line asset tracking of non-consumables

When transfer order line stages change for non-consumables, it affects asset substates.

|Transfer order line stage|Affect on asset substate|
|-------------------------|------------------------|
|Draft|Asset moves to **In Stock** &gt; **Pending Transfer** \(from the current stockroom\). If the asset is a consumable, the quantity can be edited.|
|Requested|Asset stays in **In Stock** &gt; **Pending Transfer**.|
|Shipment Preparation|Asset stays in **In Stock** &gt; **Pending transfer**.|
|In Transit|Asset moves to **In Transit** &gt; **Reserved**.|
|Received|Asset moves to **In Stock** &gt; **Available** \(in the destination stockroom\).|
|Delivered|Asset moves to **In Stock** &gt; **Reserved**.|

**Related topics**  


[Delete a transfer order](../concept/transfer-orders-for-am.md#)

[Delete a transfer order line](../concept/transfer-orders-for-am.md#)

[Return items received in a transfer order](../concept/transfer-orders-for-am.md#)

## Transfer order line asset tracking consumables

When a consumable is added to a transfer order line, the stock for the consumable is split into two records and the transfer order links to the newly created stock line.

For example:

1.  Stockroom A has ten keyboards in stock.
2.  A transfer order line named TOL1 transfers three keyboards from stockroom A to stockroom B.
3.  The stock of ten keyboards in A is split into two records: seven shown as **In stock** &gt; **Available** and three shown as **In Stock** &gt; **Pending Transfer**.
4.  Another transfer order is created with a transfer order line named TOL2 that transfers two keyboards from stockroom A to stockroom B.
5.  The seven remaining keyboards are split into another two lines: five **In stock** &gt; **Available** and two **In stock** &gt; **Pending Transfer**.

    **Note:** The three **In Stock** &gt; **Pending Transfer** and the two **In Stock** &gt; **Pending Transfer** are not merged together because they are not part of the same transfer order line and not necessarily from the same person.

6.  As TOL2 for two keyboards moves from Draft to Requested to Shipment Preparation, TOL1 for the three keyboards remains **In Stock** &gt; **Pending Transfer**.
7.  When TOL1 for the three keyboards moves to the In Transit stage, the three keyboards are changed to the **In Transit** &gt; **Reserved** stage. The same happens for TOL2 with two keyboards.
8.  When TOL1 is Received, the three keyboards move to **In stock** &gt; **Available** in stockroom B.
9.  When TOL2 is received in stockroom B, the two keyboards move to **In stock** &gt; **Available** and are merged with the three keyboards that are also **In Stock** &gt; **Available** in B.
10. At the end, stockroom B shows five keyboards are **In Stock** &gt; **Available**.

**Related topics**  


[Delete a transfer order](../concept/transfer-orders-for-am.md#)

[Delete a transfer order line](../concept/transfer-orders-for-am.md#)

[Return items received in a transfer order](../concept/transfer-orders-for-am.md#)

