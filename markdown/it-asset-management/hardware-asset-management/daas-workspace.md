---
title: DaaS provider view
description: The DaaS provider view in the Hardware Asset Workspace is an intuitive interface of the Device as a Service application to manage the assets of the customers of DaaS providers.
locale: en-US
release: xanadu
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Hardware Asset Workspace, Exploring Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# DaaS provider view

The DaaS provider view in the Hardware Asset Workspace is an intuitive interface of the Device as a Service application to manage the assets of the customers of DaaS providers.

**Note:** You must activate the following plugins to access the DaaS provider view:

-   Hardware Asset Management application \(sn\_hamp\)
-   Hardware Asset Workspace \(sn\_itam\_workspace\)
-   Hardware Asset Management for Device as a Service \(com.sn\_daas\_ham\)

For more information about the DaaS feature, see [Device as a Service](exploring-daas.md).

Use the DaaS provider view to perform the following:

-   Act on discrepancies such as assets missing serial number, stockroom, or DaaS accounts.
-   Select a DaaS account for which you want to view the records such as open or unassigned tasks, shipment status, and the number of assets that are eligible for refresh.
-   Create and manage [inbound asset orders](manage-inbound-orders.md), [RMA response orders](manage-rma-orders.md), and [repair order lines](../../hardware-asset-management/concept/requesting-hardware-asset-repair.md) for the DaaS assets of your customers.

Select any widget or chart to view detailed information and take appropriate actions on the assets that are marked as DaaS assets or dedicated to accounts.

![DaaS provider view in Hardware Asset Workspace.](../image/daas-workspace.jpg)

<table id="table_yjs_p21_cbc"><thead><tr><th>

Widget/Chart

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Important Actions

</td></tr><tr><td>

Fill in missing asset tag

</td><td>

Action to be performed on the assets that have missing asset tag.

</td></tr><tr><td>

Fill in missing serial number

</td><td>

Action to be performed on the assets that have missing serial number.

</td></tr><tr><td>

Fill in missing DaaS account

</td><td>

Action to be performed on the assets that have missing DaaS accounts.

</td></tr><tr><td>

Fill in missing stockroom

</td><td>

Action to be performed on the assets that have missing stockroom information.

</td></tr><tr><td colspan="2">

 

</td></tr><tr><td>

DaaS account

</td><td>

Customer of the DaaS provider whose data is being referenced.

</td></tr><tr><td>

Inbound order tasks

</td><td>

-   Open tasks: Number of open tasks in each stage of the Inbound asset order flow.
-   Unassigned tasks: Number of unassigned tasks in each stage of the Inbound asset order flow.

 The Inbound order flow includes the following stages:

-   Select
-   Pick
-   Prepare
-   Ship
-   Receive confirmation

For more information, see [Managing inbound asset orders for DaaS assets](manage-inbound-orders.md).

</td></tr><tr><td>

RMA response tasks

</td><td>

-   Open tasks: Number of open tasks in each stage of the RMA response order flow.
-   Unassigned tasks: Number of unassigned tasks in each stage of the RMA response order flow.

 The RMA response order flow includes the following stages:

-   Evaluate asset
-   Schedule shipment
-   Receive confirmation
-   Repair asset
-   Schedule refresh

For more information, see [Managing RMA response orders for DaaS assets](manage-rma-orders.md).

</td></tr><tr><td>

Repair order tasks

</td><td>

-   Open tasks: Number of open tasks in each stage of the repair order flow.
-   Unassigned tasks: Number of unassigned tasks in each stage of the repair order flow.

 The repair order flow includes the following stages:

</td></tr><tr><td>

Shipment assets

</td><td>

Open shipment tasks in RMA response order or Inbound asset order flow.

</td></tr><tr><td>

Assets eligible for refresh

</td><td>

Number of assets that are eligible for refresh, which have surpassed the refresh date.

</td></tr></tbody>
</table>