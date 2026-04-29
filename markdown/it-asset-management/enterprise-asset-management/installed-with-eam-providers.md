---
title: Components installed with Enterprise Asset Management for Providers
description: Several types of components are installed with activation of the com.sn\_eam\_provider plugin, including user roles, applications, and tables.
locale: en-US
release: australia
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Enterprise Asset Management for Providers, Industry-specific EAM solutions, Enterprise Asset Management, IT Asset Management]
---

# Components installed with Enterprise Asset Management for Providers

Several types of components are installed with activation of the com.sn\_eam\_provider plugin, including user roles, applications, and tables.

## Roles installed

<table id="table_t5p_2y4_zgc"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Provider asset manager

 \[sn\_eam\_provider.provider\_asset\_manager\]

</td><td>

Manages all DaaS-related activities, including the fulfillment of Return Merchandise Authorization \(RMA\) requests.

</td><td>

-   sn\_eam.asset\_manager
-   sn\_eam\_provider.provider\_asset\_technician

</td></tr><tr><td>

Provider asset technician

 \[sn\_eam\_provider.provider\_asset\_technician\]

</td><td>

Performs tasks related to DaaS assets.

</td><td>

sn\_eam.asset\_technician

</td></tr></tbody>
</table>## Applications installed

|Name|Description|
|----|-----------|
|ITAM Common forDaaS \(sn\_daas\_common\)|Provides asset management services to DaaS providers, vendors, and manufacturers to support their DaaS offerings.|

## Tables installed

<table id="table_x5p_2y4_zgc"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

RMA response

 \[sn\_daas\_common\_rma\_response\_order\]

</td><td>

Information about your RMA response orders, including the originating account and the delivery address.

</td></tr><tr><td>

RMA response order line

 \[sn\_daas\_common\_rma\_response\_orderline\]

</td><td>

Information about each asset that is associated with your RMA response orders, including the model of the asset.

</td></tr><tr><td>

Inbound asset order

 \[sn\_itam\_common\_inbound\_asset\_order\]

</td><td>

Information about your inbound asset orders, including the originating account and the delivery address.

</td></tr><tr><td>

Inbound asset order line

 \[sn\_itam\_common\_inbound\_asset\_orderline\]

</td><td>

Information about each asset that is associated with your inbound asset orders, including the model of the asset.

</td></tr></tbody>
</table>**Parent Topic:**[Enterprise Asset Management for Providers](../concept/eam-providers.md)

