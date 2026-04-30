---
title: Components installed with Hardware Asset Management for DaaS
description: Several types of components are installed with activation of the Hardware Asset Management for DaaS \(com.sn\_daas\_ham\) plugin, including tables and user roles.
locale: en-US
release: zurich
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [DaaS reference, Device as a Service, Hardware Asset Management, IT Asset Management]
---

# Components installed with Hardware Asset Management for DaaS

Several types of components are installed with activation of the Hardware Asset Management for DaaS \(com.sn\_daas\_ham\) plugin, including tables and user roles.

## Roles installed

<table id="table_hgy_lmh_cbc"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

DaaS Manager \[sn\_daas\_ham.daas\_asset\_manager\]

</td><td>

-   Manages all aspects of DaaS, including access and execution of important actions, reports, and requests such as inbound asset orders and Return Merchandise Authorization \(RMA\) orders.
-   Marks assets as DaaS assets.

</td><td>

Asset Manager \[asset\]

</td></tr></tbody>
</table>## Tables installed

|Table|Description|
|-----|-----------|
|RMA response \[sn\_daas\_common\_rma\_response\_order\]|Information about the Return Merchandise Authorization \(RMA\) request with multiple order lines, including details, such as the originating account and the delivery address.|
|RMA response order line \[sn\_daas\_common\_rma\_response\_orderline\]|Model and asset information associated with the RMA creation.|
|Inbound asset order \[sn\_itam\_common\_inbound\_asset\_order\]|Information about the asset request with multiple order lines, such as the originating account and the delivery address.|
|Inbound asset order line \[sn\_itam\_common\_inbound\_asset\_orderline\]|Information about the model for which the asset is requested.|

