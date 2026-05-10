---
title: Perform asset audit for personal stockrooms
description: Verify and reconcile assets between a physical location such as the technician's stockroom and the system.
locale: en-US
release: australia
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Inventory, ServiceNow Agent mobile app, Completing work on mobile, Use, Field Service Management]
---

# Perform asset audit for personal stockrooms

Verify and reconcile assets between a physical location such as the technician's stockroom and the system.

## Before you begin

Ensure that you have the following setup:

-   The sn\_itam\_common and sn\_itam\_asset\_audits store applications are installed.
-   The sn\_itam\_common\_personal\_stockroom\_audit\_user and sn\_itam\_common\_personal\_stockroom\_audit\_admin roles are enabled. These roles must be added with wm\_agent and enable you to edit personal stockrooms only when Enterprise Asset Management is not installed.
-   The com.snc\_fsm\_mobile, com.sn\_itam\_common and com.sn\_asset\_audits plugins must be installed.

Role required: wm\_agent

## About this task

-   Without Enterprise Asset Management installed:
    -   Users can audit their personal stockrooms only.
    -   Stockroom selection is restricted to field agent stockrooms only.
-   With Enterprise Asset Management installed:
    -   Users with the wm\_agent role can only audit personal stockrooms.
    -   Users with the asset\_audit\_user or asset\_audit\_admin role can audit all stockrooms.
    -   Space fields are displayed.
    -   Users can select any stockroom.

For more information, see [Stockroom audit access by role](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/enterprise-asset-management/stockroom-audit-access-eam.md).

## Procedure

1.  Open the ServiceNow Agent mobile application.

2.  Tap **Inventory**.

3.  Tap **Stockroom audits**.

4.  Tap the More ![](../image/perform-asset-audit.png) icon and select **New stockroom audit**.

5.  Select **Scan** as the method.

6.  Add the stockroom by tapping **Submit**.

7.  Scan the personal stockroom assets by selecting the stockroom and tapping **Scan**.

8.  Match the asset between the technician's stockroom and the system by swiping the asset and tapping **Audit**.

    **Note:**

    -   Once all the assets are scanned, all the stockroom details such as **Expected**, **Missing**, and **New** are updated. The **Expected** count displays the number of assets present in both the technician's stockroom and the system that can be reconciled. The **Missing** count displays assets that are yet to be scanned from the technician's stockroom and the discrepancy between the technician's stockroom and the system.
    -   There is no quantity check for hardware assets and they are set to 1 by default.
9.  If you scan an asset that is present in the technician's stockroom but not in the system, update it by tapping the **Create asset** option.

    1.  Provide details of the asset such as the model, asset tag, and number.

    2.  Select the technician's personal stockroom as the **Stockroom**.

10. Complete the audit by tapping the More ![](../image/perform-asset-audit.png) icon and tapping **Complete**.


## Result

The asset audit is complete, ensuring that the assets in the technician's personal stockroom and the system are in sync.

