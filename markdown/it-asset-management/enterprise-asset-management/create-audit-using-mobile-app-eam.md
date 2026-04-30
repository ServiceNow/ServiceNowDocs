---
title: Create an enterprise audit record using the ServiceNow Agent app
description: Create an inventory audit record using the ServiceNow Agent app.
locale: en-US
release: yokohama
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2026-01-05"
reading_time_minutes: 3
keywords: [create an audit record]
breadcrumb: [Manage enterprise asset inventory audit using the ServiceNow Agent app, Managing enterprise assets and tasks using the Mobile Agent application, Enterprise Asset Management, IT Asset Management]
---

# Create an enterprise audit record using the ServiceNow Agent app

Create an inventory audit record using the ServiceNow Agent app.

## Before you begin

Role required: sn\_eam.enterprise\_admin or sn\_eam.enterprise\_asset\_manager

## Procedure

1.  From your mobile device, launch the Mobile Agent application.

2.  On the navigation bar at the bottom of the screen, tap the **Enterprise Asset** tab.

3.  Select the audit that you want to perform.

<table id="choicetable_bpk_mvc_whc"><thead><tr><th align="left" id="d69571e78">

Audit type

</th><th align="left" id="d69571e81">

Action

</th></tr></thead><tbody><tr><td id="d69571e87">

**To perform stockroom audits**

</td><td>

1.  On the navigation bar, tap the Stockroom audits menu.
2.  Tap the more actions icon \(![](../../hardware-asset-management/image/more-actions-icon.png)\).
3.  Tap **New stockroom audit**.


</td></tr><tr><td id="d69571e116">

**To perform location audits**

</td><td>

1.  On the navigation bar, tap the Location audits menu.
2.  Tap the more actions icon \(![](../../hardware-asset-management/image/more-actions-icon.png)\).
3.  Tap **New location audit**.


</td></tr></tbody>
</table>4.  On the form, fill in the fields.

<table id="table_qnv_44d_whc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Stockroom**Note:** This field appears if you’re creating a stockroom audit.

</td><td>

Stockroom where you want to perform the audit.

</td></tr><tr><td>

Location**Note:** This field appears if you’re creating a location audit.

</td><td>

Location where you want to perform the audit.

</td></tr><tr><td>

Aisle and space**Note:** This field appears if you’re creating a stockroom audit.

</td><td>

Aisle and space for which you want to perform the audit.

</td></tr><tr><td>

Include child locations**Note:** This field appears if you’re creating a location audit.

</td><td>

Option to include child locations in the audit.

</td></tr><tr><td>

Model category

</td><td>

Model category for which you want to perform the audit.

</td></tr><tr><td>

Include consumables**Note:** This field appears if you’re creating a stockroom audit.

</td><td>

Option to include consumable assets in the inventory audit. The available options are:-   Yes
-   No
The default populated value for this field is derived using the **sn\_itam\_common.set\_default\_include\_consumables** system property.-   When this system property value is set to **yes**, the default value for the **Include consumables** field is set to **Yes**.
-   When this system property value is set to **no**, the default value for the **Include consumables** field is set to **No**.
**Important:** This field is available with Enterprise Asset Management version 10.0.0 onwards.

</td></tr><tr><td>

Scan method

</td><td>

Scan method to be used to scan the assets. The available options are:-   Single scan
-   Multi scan
-   When the **Include consumables** field is set to **Yes**, the **Scan method** field value is automatically set to **Single Scan** and can’t be edited.
-   When the **Include consumables** field is set to **No**, the **Scan method** field becomes editable, enabling you to select the scan type.
Depending on the selected scan method for the audit record, you can scan the assets in the inventory using the ServiceNow Agent app.

-   To complete asset scanning for the single scan audit record, see [Complete a single scan enterprise asset inventory audit using the ServiceNow Agent app](scan-assets-agent-app-eam.md).
-   To complete asset scanning for multi scan audit records, see [Complete multi scan enterprise asset inventory audit using the ServiceNow Agent app](complete-multi-scan-inventory-audit-using-mobile-app-eam.md).
**Important:** This field is available with Enterprise Asset Management version 10.0.0 onwards.

</td></tr></tbody>
</table>5.  Tap **Submit**.


## Result

-   An audit record is created and listed on the **Open** tab.
-   The audit result fields are displayed on the audit **Details** tab.

    For a detailed description of the audit result field values, see [Audit results](../../hardware-asset-management/reference/audit-results.md).


## What to do next

Scan the assets in the inventory using the ServiceNow Agent app.

**Related topics**  


[Complete a single scan enterprise asset inventory audit using the ServiceNow Agent app](scan-assets-agent-app-eam.md)

[Complete multi scan enterprise asset inventory audit using the ServiceNow Agent app](complete-multi-scan-inventory-audit-using-mobile-app-eam.md)

