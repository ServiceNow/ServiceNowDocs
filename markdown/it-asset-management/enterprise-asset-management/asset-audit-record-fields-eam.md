---
title: Asset audit fields for enterprise assets
description: Create New Asset Audits form and related fields description.
locale: en-US
release: zurich
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: reference
last_updated: "2026-01-19"
reading_time_minutes: 6
keywords: [asset audit, inventory audit, audit record fields]
breadcrumb: [References, Enterprise Asset Management, IT Asset Management]
---

# Asset audit fields for enterprise assets

Create New Asset Audits form and related fields description.

## Create New Asset Audits form

<table id="table_pd5_p51_rsb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Audit number

</td><td>

Audit reference number.

</td></tr><tr><td>

Assignment group

</td><td>

Group to which you want to assign the audit.

</td></tr><tr><td>

Assigned to

</td><td>

Person responsible for the audit.

</td></tr><tr><td>

Type

</td><td>

Type of the audit. The available values are-   Location
-   Stockroom

</td></tr><tr><td>

Status

</td><td>

Current status of the audit.

</td></tr><tr><td>

Location**Note:** This field appears only if you set the **Type** field to **Location**.

</td><td>

Location in which you want to perform the audit.

</td></tr><tr><td>

Include child locations**Note:** This field appears only if you set the **Type** field to **Location**.

</td><td>

Option to include child locations in the audit.

</td></tr><tr><td>

Stockroom**Note:** This field appears only if you set the **Type** field to **Stockroom**.

</td><td>

Stockroom in which you want to perform the audit.

</td></tr><tr><td>

Model category

</td><td>

Model category that you want to audit.

</td></tr><tr><td>

Aisle and space**Note:** This field appears only if you set the **Type** field to **Stockroom**.

</td><td>

Aisle and space within the stockroom where you want to perform the audit.

</td></tr><tr><td>

Scheduled date

</td><td>

Date on which you want to perform the audit.

</td></tr><tr><td>

Scan date

</td><td>

Date on which you want to scan the assets.

</td></tr><tr><td>

Include consumables

</td><td>

Option to include consumable assets in the stockroom audit. The available options are:-   Yes: When this field is set to **Yes**, consumable assets are included in the inventory audit.
-   No: When this field is set to **No**, consumable assets aren't included in the inventory audit.

**Note:** You can include consumable assets only for stockroom audit. When the **Type** field is set to **Stockroom**, this field is activated. When the **Type** field is set to **Location**, this field is automatically set to **No** and inactive.

 The default populated value for this field is derived using the **sn\_itam\_common.set\_default\_include\_consumables** system property. -   When this system property value is set to **yes**, the default value for the **Include consumables** field is set to **Yes**.
-   When this system property value is set to **no**, the default value for the **Include consumables** field is set to **No**.

 **Important:** This field is available with Enterprise Asset Management version 10.0.0 onwards.

</td></tr><tr><td>

Scan method

</td><td>

Type of scan method for scanning the assets. The available options are:-   Single scan
-   Multi scan

Depending on the value of the **Include consumables** field, the default selection for the scan method is automatically determined.

-   When the **Include consumables** field is set to **Yes**, the **Scan method** field value is automatically set to **Single Scan** and can’t be edited.
-   When the **Include consumables** field is set to **No**, the Scan method field becomes editable, enabling you to select the desired scan type.

Depending on the selected scan method for the audit record, you can scan the assets in the inventory using the ServiceNow Agent app.

-   To complete asset scanning for the single scan audit record, see [Complete a single scan enterprise asset inventory audit using the ServiceNow Agent app](../task/scan-assets-agent-app-eam.md).
-   To complete asset scanning for multi scan audit records, see [Complete multi scan enterprise asset inventory audit using the ServiceNow Agent app](../task/complete-multi-scan-inventory-audit-using-mobile-app-eam.md).

**Important:** This field is available with Enterprise Asset Management version 10.0.0 onwards.

</td></tr></tbody>
</table>**Note:** The audit result fields such as **Expected**, **Not expected and location corrected**, **Missing**, **New**, and **Excluded from licensing** can't be edited. When the asset is scanned in the inventory using the ServiceNow Agent app, values are automatically updated in these fields. For more information about scanning assets, see [Complete a single scan enterprise asset inventory audit using the ServiceNow Agent app](../task/scan-assets-agent-app-eam.md) and [Complete multi scan enterprise asset inventory audit using the ServiceNow Agent app](../task/complete-multi-scan-inventory-audit-using-mobile-app-eam.md).

**Parent Topic:**[Enterprise Asset Management reference](../concept/reference-enterprise-asset-management.md)

**Related topics**  


[Domain separation and Enterprise Asset Management](../concept/domain-separation-eam.md)

[Enterprise Asset Management roles](eam-roles.md)

[OT Asset Workspace roles](ot-workspace-roles.md)

[Asset fields for enterprise assets](asset-fields-eam.md)

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

[Components installed with Enterprise Asset Management for Providers](installed-with-eam-providers.md)

[Scheduled jobs and tables installed with normalization of firmware models](firmware-tables-jobs-ot.md)

[Asset put away task fields](put-away-task-form-eam.md)

[Audit results](audit-results-eam.md)

[Complete a single scan enterprise asset inventory audit using the ServiceNow Agent app](../task/scan-assets-agent-app-eam.md)

[Complete multi scan enterprise asset inventory audit using the ServiceNow Agent app](../task/complete-multi-scan-inventory-audit-using-mobile-app-eam.md)

