---
title: Complete a single scan inventory audit using the ServiceNow Agent app
description: Scan your inventory assets by using the ServiceNow Agent app for single scan audit records.
locale: en-US
release: australia
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Audit hardware asset inventory, Using Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Complete a single scan inventory audit using the ServiceNow Agent app

Scan your inventory assets by using the ServiceNow Agent app for single scan audit records.

## Before you begin

The **sn\_hamp\_migrate\_hamaudit** system property is set to **true** to enable the audit enhancements introduced in the Hardware Asset Management version 15.0.0.

Role required: asset, sn\_itam\_common.asset\_audit\_admin or sn\_itam\_common.asset\_audit\_user

## Procedure

1.  From your mobile device, launch the ServiceNow Agent application.

2.  Tap **Asset**.

3.  Select the stockroom or location audit record.

4.  Tap **Start audit**.

    **Note:** This button appears only for the location audit.

5.  Select **Scan**.

    The Asset scan page is displayed.

6.  In the **Asset tag/Serial number/Model barcode** field, enter or scan the asset tag, serial number, or model barcode of the asset.

7.  Tap **Next**.

8.  Select an **Aisle and space**.

9.  Select **Submit**.

    The List of assets and models screen is displayed, showing the scanned asset record.

    **Note:** When the scanned asset record doesn't exist in your ServiceNow instance, the List of assets and models screen is empty. You can create an asset record for the new asset in the inventory. For more information, see [Create an asset from the inventory audit screen](inventory-audit-create-asset.md).

10. On the List of assets and models screen, slide the scanned asset record to the left side.

    The Audit option is displayed on the screen.

    ![Audit option for single scan method](../image/single-scan-audit-option.png)

11. Tap **Audit**.

    The **Details** tab screen is displayed. The audit result field values are automatically updated when you scan the stockroom assets.

12. After you’re finished scanning assets, mark the audit as complete.

    1.  Tap the three dots icon in the navigation bar.

    2.  Tap **Complete**.

        A confirmation message appears on the audits page.

        **Note:** You can start a new scan as many times as you need while the audit is in progress. After you mark the audit as **Complete**, you can't scan any more assets.


## Result

The audit result field values are updated on the **Details** tab screen. For a detailed field description, see [Audit results](../reference/audit-results.md).

## What to do next

-   Review the inventory audit result.
-   Tap the audit result field values to view the detailed list of the assets.

**Parent Topic:**[Audit hardware asset inventory](../concept/ham-inventory-audit.md)

**Related topics**  


[View audit results](view-audit-results.md)

[Create an asset from the inventory audit screen](inventory-audit-create-asset.md)

