---
title: Complete a single scan enterprise asset inventory audit using the ServiceNow Agent app
description: Scan your inventory assets by using the ServiceNow Agent app for single scan audit records.
locale: en-US
release: zurich
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Manage enterprise asset inventory audit using the ServiceNow Agent app, Manage enterprise assets and tasks using Mobile Agent application, Enterprise Asset Management, IT Asset Management]
---

# Complete a single scan enterprise asset inventory audit using the ServiceNow Agent app

Scan your inventory assets by using the ServiceNow Agent app for single scan audit records.

## Before you begin

Role required: sn\_eam.enterprise\_admin, sn\_eam.enterprise\_asset\_manager, sn\_eam.asset\_technician, sn\_itam\_common.asset\_audit\_user, or sn\_itam\_common.asset\_audit\_admin

## About this task

**Important:** This feature is available with Enterprise Asset Management version 10.0.0 onwards.

## Procedure

1.  From your mobile device, launch the ServiceNow Agent application.

2.  On the navigation bar at the bottom of the screen, tap the **Enterprise Asset** tab.

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

    **Note:** When the scanned asset record doesn't exist in your ServiceNow instance, the List of assets and models screen is empty. You can create an asset record for the new asset in the inventory. For more information, see [Create an enterprise asset from the inventory audit screen](inventory-audit-create-asset-eam.md).

10. On the List of assets and models screen, slide the scanned asset record to the left side.

    The Audit option is displayed on the screen.

    ![Audit option for single scan method](../../hardware-asset-management/image/single-scan-audit-option.png)

11. Tap **Audit**.

    The **Details** tab screen is displayed. The audit result field values are automatically updated when you scan the stockroom assets.

12. After you’re finished scanning assets, mark the audit as complete.

    1.  Tap the three dots icon in the navigation bar.

    2.  Tap **Complete**.

        A confirmation message appears on the audits page.

        **Note:** You can start a new scan as many times as you need while the audit is in progress. After you mark the audit as **Complete**, you can't scan any more assets.


## Result

The audit result field values are updated on the **Details** tab screen. For a detailed field description, see [Audit results](../reference/audit-results-eam.md).

## What to do next

-   Review the inventory audit result.
-   Tap the audit result field values to view the detailed list of the assets.

**Related topics**  


[Audit results](../reference/audit-results-eam.md)

[Create an enterprise asset from the inventory audit screen](inventory-audit-create-asset-eam.md)

