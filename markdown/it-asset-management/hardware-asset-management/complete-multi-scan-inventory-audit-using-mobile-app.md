---
title: Complete multi scan inventory audit using the ServiceNow Agent app
description: Scan your inventory assets by using the ServiceNow Agent app for the multi scan audit records.
locale: en-US
release: australia
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [scan assets, scan multiple assets, multi scan inventory audit]
breadcrumb: [Audit hardware asset inventory, Using Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Complete multi scan inventory audit using the ServiceNow Agent app

Scan your inventory assets by using the ServiceNow Agent app for the multi scan audit records.

## Before you begin

Role required: asset, sn\_itam\_common.asset\_audit\_admin, or sn\_itam\_common.asset\_audit\_user

**Note:**

-   When the **sn\_hamp\_migrate\_hamaudit** system property is set to **true**, you're required to have the asset role, along with either the sn\_itam\_common.asset\_audit\_admin or sn\_itam\_common.asset\_audit\_user role.
-   When the **sn\_hamp\_migrate\_hamaudit** system property is set to **false**, only the asset role is required.

## Procedure

1.  From your mobile device, launch the ServiceNow Agent application.

2.  Tap **Asset**.

3.  Select the stockroom or location audit record.

4.  Tap **Start audit**.

    **Note:** This button appears only for the location audit.

5.  Select **Scan**.

    The Asset scan screen is displayed.

6.  Scan or enter the asset tag in the **Asset Tag** field.

    You can scan or enter the asset tag for one or more assets.

7.  Select the **Review** tab to review the list of scanned assets.

    On the review screen, you can delete assets if needed. However, Hardware Asset Management automatically removes duplicates for assets that you accidentally scan twice.

8.  Tap **Next**.

9.  Select an Aisle and space.

10. Select **Submit**.

    The Stockroom audit **Details** tab screen is displayed.

    **Note:** If the scanned asset record doesn't exist in your ServiceNow instance, a new asset record is created using the provided Asset tag. The new asset record is created with an unknown product model and an unknown model category value. Additionally, an asset remediation task is also created to notify you that an asset record has been created with an unknown model category and an unknown product model. Open the asset remediation task from the Hardware Asset Workspace and update the **Model category** and **Model** fields value for the asset. For more information, see [Close an asset remediation task](close-an-asset-remediation-task.md).

11. After you’re finished scanning assets, mark the audit as complete.

    1.  Tap the three dots icon in the navigation bar.

    2.  Tap **Complete**.

        A confirmation message appears on the audits page.

        **Note:** You can start a new scan as many times as you need while the audit is in progress. After you mark the audit as **Complete**, you can't scan any more assets.


**Parent Topic:**[Audit hardware asset inventory](../concept/ham-inventory-audit.md)

**Related topics**  


[Close an asset remediation task](close-an-asset-remediation-task.md)

