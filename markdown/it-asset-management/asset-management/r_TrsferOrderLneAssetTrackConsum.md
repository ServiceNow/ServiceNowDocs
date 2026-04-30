---
title: Transfer order line asset tracking consumables
description: When a consumable is added to a transfer order line, the stock for the consumable is split into two records and the transfer order links to the newly created stock line.
locale: en-US
release: yokohama
product: Asset Management
classification: asset-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Transfer order line asset tracking, Manage transfer order, Using Asset Management, Asset Management, IT Asset Management]
---

# Transfer order line asset tracking consumables

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

**Parent Topic:**[Transfer order line asset tracking](r_TransferOrderLineAssetTracking.md)

**Related topics**  


[Delete a transfer order](../task/t_DeleteATransferOrder.md)

[Delete a transfer order line](../task/t_DeleteATransferOrderLine.md)

[Return items received in a transfer order](../task/t_ReturnItemsRecInXferOrder.md)

