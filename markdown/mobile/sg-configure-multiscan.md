---
title: Configure a grouped input for multiple scans
description: Enable your users to scan several barcodes sequentially. Users can scan barcodes without leaving the scanning interface when you configure a grouped input. You can configure grouped inputs on buttons to accept multiple barcode scans.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Mobile barcode scanning, Considerations before implementation, ServiceNow Mobile Platform configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Configure a grouped input for multiple scans

Enable your users to scan several barcodes sequentially. Users can scan barcodes without leaving the scanning interface when you configure a grouped input. You can configure grouped inputs on buttons to accept multiple barcode scans.

## Before you begin

Role required: admin

## Procedure

1.  In the application navigator, enter `sys_sg_button` to open a list of mobile functions.

2.  Open the record for the button where you want to include multi-scan functionality.

3.  Click the **Grouped Inputs** tab on the form to display the grouped inputs list.

4.  Click **New**.

5.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of your grouped input. Because this name is used in scripts, do not include spaces in names.|
    |Label|Label to describe your grouped input. You may use spaces in your label.|
    |Source|Source for the grouped input. Select **Button**.|
    |Button|Button used for the grouped input. The **Button** field appears after you select **Button** in the **Source** field.|
    |Order|Order value for your grouped input.|
    |Mandatory|Field that you enable to require that at least one value is entered for this input.|
    |Multiple entries|Ability to scan multiple entries.|
    |Max entries|Maximum number of entries for this input. Enter `0` for an unlimited number of entries. This field is visible only when the **Multiple entries** field is enabled.|


-   **[Create UI parameters for your grouped input](sg-configure-multiscan-2.md)**  
Create UI parameters to contain the values that your users scan in with your grouped input.
-   **[Configure your action item to use your grouped input UI parameters](sg-configure-multiscan-3.md)**  
Configure the action item on your button so that you can use the values that your users scan in.

**Parent Topic:**[Mobile barcode scanning](../concept/sg-mobile-scanning.md)

