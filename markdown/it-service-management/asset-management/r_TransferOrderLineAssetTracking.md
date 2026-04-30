---
title: Transfer order line asset tracking
description: As transfer order line actions are triggered, the stock information and states of any affected assets are updated. Consumables and non-consumables are tracked differently.When transfer order line stages change for non-consumables, it affects asset substates.When a consumable is added to a transfer order line, the stock for the consumable is split into two records and the transfer order links to the newly created stock line.
locale: en-US
release: xanadu
product: Asset Management
classification: asset-management
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Asset Management, IT Service Management]
---

# Transfer order line asset tracking

As transfer order line actions are triggered, the stock information and states of any affected assets are updated. Consumables and non-consumables are tracked differently.

When an asset is included in a transfer order line, the following takes place:

-   A substate field on the asset form changes to reflect the transfer order line states
-   The Active TO option on the asset form is automatically selected to show that the asset is part of a transfer order and cannot be added to multiple transfer orders
-   The asset is removed from the pool of available assets and changed to a state of In Stock Pending Transfer

**Parent Topic:**[Asset Management](../concept/c_AssetManagement.md)

**Related topics**  


[Delete a transfer order](../concept/transfer-orders-asset.md#)

[Delete a transfer order line](../concept/transfer-orders-asset.md#)

[Return items received in a transfer order](../concept/transfer-orders-asset.md#)

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


[Delete a transfer order](../concept/transfer-orders-asset.md#)

[Delete a transfer order line](../concept/transfer-orders-asset.md#)

[Return items received in a transfer order](../concept/transfer-orders-asset.md#)

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


[Delete a transfer order](../concept/transfer-orders-asset.md#)

[Delete a transfer order line](../concept/transfer-orders-asset.md#)

[Return items received in a transfer order](../concept/transfer-orders-asset.md#)

