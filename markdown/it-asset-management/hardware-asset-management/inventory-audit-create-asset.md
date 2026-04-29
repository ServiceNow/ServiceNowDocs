---
title: Create an asset from the inventory audit screen
description: Create an asset record for the scanned asset that doesn't exist in your ServiceNow instance and that is detected when auditing inventory.
locale: en-US
release: australia
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [create an asset, create new asset inventory audit screen]
breadcrumb: [Audit hardware asset inventory, Using Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Create an asset from the inventory audit screen

Create an asset record for the scanned asset that doesn't exist in your ServiceNow instance and that is detected when auditing inventory.

## Before you begin

Role required: asset, and sn\_itam\_common.asset\_audit\_admin, or sn\_itam\_common.asset\_audit\_user

## About this task

When scanning an asset in the inventory, if a new asset is detected that doesn’t exist in your ServiceNow® instance, you can create a record for it. You can add the asset directly from the audit screen in the ServiceNow Agent app.

**Note:** This procedure applies when you scan assets for a single scan audit record.

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

    The List of assets and models screen is displayed.

10. Tap the three dots icon ![](../image/list-of-assets-and-models-three-dot-icon.png).

11. Tap **Create new asset**.

    ![Create new asset](../image/list-of-assets-and-models-screen.png)

    The Create asset from audit screen is displayed.

12. On the form, fill in the following fields.

    | | |
    |---|---|
    |Model|The product model of the asset.|
    |Stockroom|The stockroom where the asset is available.|
    |State|The **State** field value is automatically set to **In stock**. Change this value as needed.|
    |Substate|The **Substate** field value is automatically set to **Available**. Change this value as needed.|
    |Asset Tag|Alphanumeric information assigned by your organization to help track the asset.|
    |Serial Number|Serial number of this asset.|
    |MAC address|MAC address of the mobile device|

    **Note:** Depending on the IRE rule configured for the selected **Model** field value, either **Asset Tag**, **Serial Number**, or **MAC address** field value is required to save the audit record.

    For more details on these field descriptions, see [Asset record fields](../../asset-management/reference/asset-record-fields.md).

13. Tap **Submit**.

    A confirmation message is displayed on the screen, and the asset record is created.


## Result

In the audit results, the **New** field value is incremented for each new asset scanned in the inventory.

**Parent Topic:**[Audit hardware asset inventory](../concept/ham-inventory-audit.md)

