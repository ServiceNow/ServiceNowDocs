---
title: Components installed with Enterprise Asset Management for Providers
description: Several types of components are installed with activation of the com.sn\_eam\_provider plugin, including user roles, applications, and tables.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/it-asset-management/enterprise-asset-management/installed-with-eam-providers.html
release: yokohama
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: reference
last_updated: "2025-10-16"
reading_time_minutes: 3
breadcrumb: [Enterprise Asset Management reference, Enterprise Asset Management, IT Asset Management]
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
</table>**Parent Topic:**[Enterprise Asset Management reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-asset-management/enterprise-asset-management/reference-enterprise-asset-management.md)

**Related topics**  


[Domain separation and Enterprise Asset Management]()

[Enterprise Asset Management roles]()

[OT Asset Workspace roles]()

[Asset fields for enterprise assets]()

[Asset audit fields for enterprise assets]()

[Audit results]()

[Enterprise model categories and corresponding classes]()

[Mandatory fields in the bulk import spreadsheets]()

[Normalization status for enterprise models]()

[Model fields for Enterprise Asset Management]()

[Contract fields for Enterprise Asset Management]()

[Maintenance plan fields for Enterprise Asset Management]()

[Maintenance schedule fields for Enterprise Asset Management]()

[Work plan fields for Enterprise Asset Management]()

[Work plan schedule fields for Enterprise Asset Management]()

[Expense line fields for Enterprise Asset Management]()

[Fields inherited from a parent asset group to a sub group]()

[Enterprise asset disposal order stages]()

[Terminology for linear assets]()

[Installed with Enterprise Asset Management for Healthcare]()

[Installed with OT Asset Management]()

[Components installed with Enterprise Asset Management for Data Center and Network Asset Management \(DCNAM\)]()

[Scheduled jobs and tables installed with normalization of firmware models]()

[Asset put away task fields]()

