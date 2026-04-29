---
title: Create an audit record in the Hardware Asset Management application
description: Create an audit record to audit your inventory to determine the accuracy of your hardware and consumable assets and to optimize the inventory.
locale: en-US
release: australia
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Audit hardware asset inventory, Using Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Create an audit record in the Hardware Asset Management application

Create an audit record to audit your inventory to determine the accuracy of your hardware and consumable assets and to optimize the inventory.

## Before you begin

Role required: asset

The asset or inventory\_user role can only access the Asset Audits \[sn\_hamp\_asset\_audit\] reports.

**Note:**

-   When the **sn\_hamp\_migrate\_hamaudit** system property is set to **true**, you're required to have the asset role, along with either the sn\_itam\_common.asset\_audit\_admin or sn\_itam\_common.asset\_audit\_user role.
-   When the **sn\_hamp\_migrate\_hamaudit** system property is set to **false**, only the asset role is required.

## Procedure

1.  Create an audit.

<table id="choicetable_upl_qst_ywb"><thead><tr><th align="left" id="d146028e87">

Interface

</th><th align="left" id="d146028e90">

Action

</th></tr></thead><tbody><tr><td id="d146028e96">

**Core UI**

</td><td>

1.  Navigate to **Asset Audits** &gt; **Asset Audits** form.
2.  Select **New**.
 **Important:** If you have set the **sn\_hamp\_migrate\_hamaudit** system property value to **true**, to enable audit enhancements in your ServiceNow® instance, you can't create an asset audit record from the core UI.

</td></tr><tr><td id="d146028e139">

**Hardware Asset Workspace**

</td><td>

1.  Navigate to **All** &gt; **Hardware Asset Workspace** &gt; **Inventory view**.
2.  Select the **Asset audit** tab.

The **Asset audit** tab displays a list of existing asset audits.

3.  Select **New**.


</td></tr></tbody>
</table>2.  On the Create New Asset Audits form, fill in the fields.

    For a description of the field values, see [Asset audit fields](../reference/asset-audit-record-fields.md).

    **Note:** The audit result fields, such as **Expected**, and **New**, can't be edited. When the asset is scanned in the inventory using the ServiceNow Agent app, values are automatically updated in these fields. For a detailed description of the audit result field values, see [Audit results](../reference/audit-results.md).

3.  Select **Save**.


## Result

-   The asset audit inventory record is created and appears with the **Expected Assets** and **Scanned Assets** tabs.
-   The audit record is saved in the Asset Audits \[sn\_itam\_common\_asset\_audit\] table when the **sn\_hamp\_migrate\_hamaudit** system property is set to **true**.
-   The audit record is saved in the Asset Audits \[sn\_hamp\_asset\_audit\] table when the **sn\_hamp\_migrate\_hamaudit** system property is set to **false**.

## What to do next

Scan the assets in the inventory using the ServiceNow Agent app.

**Parent Topic:**[Audit hardware asset inventory](../concept/ham-inventory-audit.md)

**Related topics**  


[Complete a single scan inventory audit using the ServiceNow Agent app](scan-assets-agent-app.md)

[Complete multi scan inventory audit using the ServiceNow Agent app](complete-multi-scan-inventory-audit-using-mobile-app.md)

[View audit results](view-audit-results.md)

