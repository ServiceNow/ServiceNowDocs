---
title: Components installed with Enterprise Asset Management for Providers
description: Several types of components are installed with activation of the com.sn\_eam\_provider plugin, including user roles, applications, and tables.
locale: en-US
release: zurich
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: reference
last_updated: "2025-10-16"
reading_time_minutes: 3
breadcrumb: [References, Enterprise Asset Management, IT Asset Management]
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
</table>**Parent Topic:**[Enterprise Asset Management reference](../concept/reference-enterprise-asset-management.md)

**Related topics**  


[Domain separation and Enterprise Asset Management](../concept/domain-separation-eam.md)

[Enterprise Asset Management roles](eam-roles.md)

[OT Asset Workspace roles](ot-workspace-roles.md)

[Asset fields for enterprise assets](asset-fields-eam.md)

[Asset audit fields for enterprise assets](asset-audit-record-fields-eam.md)

[Audit results](audit-results-eam.md)

[Enterprise model categories and corresponding classes](enterprise-model-categories.md)

[Mandatory fields in the bulk import spreadsheets](mandatory-bulk-fields.md)

[Normalization status for enterprise models](norm-status-eam.md)

[Model fields for Enterprise Asset Management](eam-model-fields.md)

[Contract fields for Enterprise Asset Management](contract-fields-eam.md)

[Maintenance plan fields for Enterprise Asset Management](maintenance-plan-fields-eam.md)

[Maintenance schedule fields for Enterprise Asset Management](maintenance-schedule-fields-eam.md)

[Work plan fields for Enterprise Asset Management](wp-fields-eam.md)

[Work plan schedule fields for Enterprise Asset Management](work-plan-schedule-fields-eam.md)

[Expense line fields for Enterprise Asset Management](expense-line-fields-eam.md)

[Fields inherited from a parent asset group to a sub group](subgroups-parent-fields-eam.md)

[Enterprise asset disposal order stages](eamasset-disposalorder-stages.md)

[Terminology for linear assets](terms-eam.md)

[Installed with Enterprise Asset Management for Healthcare](installed-with-eam-healthcare.md)

[Installed with OT Asset Management](installed-with-otam.md)

[Components installed with Enterprise Asset Management for Data Center and Network Asset Management \(DCNAM\)](installed-with-eam-dcnam.md)

[Scheduled jobs and tables installed with normalization of firmware models](firmware-tables-jobs-ot.md)

[Asset put away task fields](put-away-task-form-eam.md)

