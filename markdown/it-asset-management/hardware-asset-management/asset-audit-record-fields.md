---
title: Asset audit fields
description: Create New Asset Audits form and related fields description.
locale: en-US
release: zurich
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: reference
last_updated: "2026-01-19"
reading_time_minutes: 4
keywords: [asset audit, inventory audit, audit record fields]
breadcrumb: [Reference, Hardware Asset Management, IT Asset Management]
---

# Asset audit fields

Create New Asset Audits form and related fields description.

## Create New Asset Audits form

<table id="table_kt4_5lw_nrb"><thead><tr><th>

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

Assignment group to which you want to assign the inventory audit record.

</td></tr><tr><td>

Type

</td><td>

Type of the asset audit. The available values are:-   Location
-   Stockroom

</td></tr><tr><td>

Assigned to

</td><td>

Person responsible for the audit.

</td></tr><tr><td>

Location**Note:** This field appears only if you set the **Type** field to **Location**.

</td><td>

Location in which you want to perform the audit.

</td></tr><tr><td>

Include child locations**Note:** This field appears if you set the **Type** field to **Location**.

</td><td>

Option to include child locations in the audit.

</td></tr><tr><td>

Stockroom**Note:** This field appears only if you set the **Type** field to **Stockroom**.

</td><td>

Stockroom in which you want to perform the audit.

</td></tr><tr><td>

Status

</td><td>

Present status of the audit.

</td></tr><tr><td>

Model category

</td><td>

Model category for which you want to perform the audit.**Important:** This field is available with Hardware Asset Management version 15.0.0 onwards.

</td></tr><tr><td>

Scan date

</td><td>

Date when you want to scan the assets.

</td></tr><tr><td>

Aisle and space**Note:** This field appears only if you set the **Type** field to **Stockroom**.

</td><td>

Aisle and space for which you want to perform the audit.**Important:** This field is available with Hardware Asset Management version 15.0.0 onwards.

</td></tr><tr><td>

Include consumables

</td><td>

Option to include consumable assets in the stockroom audit. The available options are:-   Yes: When this field is set to **Yes**, consumable assets are included in the inventory audit.
-   No: When this field is set to **No**, consumable assets aren't included in the inventory audit.

**Note:** You can include consumable assets only for stockroom audit. When the **Type** field is set to **Stockroom**, this field is activated. When the **Type** field is set to **Location**, this field is automatically set to **No** and inactive.

 The default populated value for this field is derived using the **sn\_itam\_common.set\_default\_include\_consumables** system property. -   When this system property value is set to **yes**, the default value for the **Include consumables** field is set to **Yes**.
-   When this system property value is set to **no**, the default value for the **Include consumables** field is set to **No**.

 **Important:** This field is available with Hardware Asset Management version 15.0.0 onwards.

</td></tr><tr><td>

Scheduled date

</td><td>

Scheduled date when you want to perform the audit.

</td></tr><tr><td>

Scan method

</td><td>

Type of scan method for scanning the assets. The available options are:-   Single scan
-   Multi scan

Depending on the value of the **Include consumables** field, the default selection for the scan method is automatically determined.

-   When the **Include consumables** field is set to **Yes**, the **Scan method** field value is automatically set to **Single Scan** and can’t be edited.
-   When the **Include consumables** field is set to **No**, the Scan method field becomes editable, enabling you to select the desired scan type.

Depending on the selected scan method for the audit record, you can scan the assets in the inventory using the ServiceNow Agent app.

-   To complete asset scanning for the single scan audit record, see [Complete a single scan inventory audit using the ServiceNow Agent app](../task/scan-assets-agent-app.md).
-   To complete asset scanning for multi scan audit records, see [Complete multi scan inventory audit using the ServiceNow Agent app](../task/complete-multi-scan-inventory-audit-using-mobile-app.md).

**Important:** This field is available with Hardware Asset Management version 15.0.0 onwards.

</td></tr></tbody>
</table>**Note:** The audit result fields such as **Expected**, **Not expected and location corrected**, **Missing**, **New**, and **Excluded from licensing** can't be edited. When the asset is scanned in the inventory using the ServiceNow Agent app, values are automatically updated in these fields. For more information about scanning assets, see [Complete a single scan inventory audit using the ServiceNow Agent app](../task/scan-assets-agent-app.md) and [Complete multi scan inventory audit using the ServiceNow Agent app](../task/complete-multi-scan-inventory-audit-using-mobile-app.md).

**Parent Topic:**[Hardware Asset Management reference](../concept/reference-hardware-asset-management.md)

**Related topics**  


[Audit results](audit-results.md)

[Create an audit record in the Hardware Asset Management application](../task/audit-your-inventory.md)

[Complete a single scan inventory audit using the ServiceNow Agent app](../task/scan-assets-agent-app.md)

[Complete multi scan inventory audit using the ServiceNow Agent app](../task/complete-multi-scan-inventory-audit-using-mobile-app.md)

