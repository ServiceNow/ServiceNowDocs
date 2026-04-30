---
title: Enable barcode scanning with an external scanner
description: Set the externalScanEnabled mobile property to True to enable barcode scanning with an external scanner while the device camera is available in other parts of the mobile app.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Mobile properties, Considerations before implementation, ServiceNow Mobile Platform configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Enable barcode scanning with an external scanner

Set the **externalScanEnabled** mobile property to `True` to enable barcode scanning with an external scanner while the device camera is available in other parts of the mobile app.

## Before you begin

Role required: admin

## About this task

When the **externalScanEnabled** mobile property is set to `True`, you can use an external scanner without denying access to the camera for the mobile app.

By default, the **externalScanEnabled** mobile property isn't configured, which turns off this feature.

In ServiceNow® mobile apps version 19.0 and later, when you configure the **externalScanEnabled** property on your ServiceNow instance, it enables a toggle switch on the barcode scan screen. This switch can be used to select the device camera or an external device.

**Important:**

External barcode scanning devices must be configured with a 'tab' character appended to the end of each barcode. Multi-scan and group scans use the tab suffix character to automatically advance to the next field.

Please refer to the user manual of your device to learn how to configure the tab suffix. For example:

-   For all Zebra scanners, see [Add a Tab Key after Scanning a Barcode](https://supportcommunity.zebra.com/s/article/Add-a-Tab-Key-After-Scanning-a-Bar-Code?language=en_US).
-   For Zebra DS2278 Bluetooth scanner, see [Tab Key](https://www.zebra.com/content/dam/support-dam/en/documentation/unrestricted/guide/product/ds2278-prg-en.pdf).
-   For Zebra TC52X, TC78x, and MC 900 \(phone with built-in scanner\), see [DataWedge: Append Send Enter or Tab Key after Scanning](https://supportcommunity.zebra.com/s/article/DataWedge-for-Android-Send-Enter-or-Tab-after-scanning?language=en_US).
-   For Honeywell CT40 \(phone with built-in scanner\), see [Article 000076406](https://sps-support.honeywell.com/s/article/How-to-add-remove-a-suffix-on-an-Android-device-running-CommonES-version-3-or-greater) in the Honeywell knowledge base.

For more information, see [Mobile barcode scanning](../concept/sg-mobile-scanning.md).

## Procedure

1.  Navigate to **All** &gt; **sys\_sg\_properties.list**.

    The Mobile Properties list appears.

2.  In the Mobile Properties list, select **New**.

    The Mobile Properties form appears.

3.  On the form, fill in the fields.

<table id="table_usp_f5m_bdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for the mobile property record.

 Enter `externalScanEnabled` to enable using an external scanner without turning off your mobile device camera.

 **Note:** The record name is case-sensitive and must be entered as `externalScanEnabled`.

</td></tr><tr><td>

Application

</td><td>

Application scope where the mobile property is applied.

 To select a different application scope, select the globe icon \(![Globe icon image](../image/globe-icon.png)\) on the instance banner. Then select **Application scope : _application\_scope_**.

 For information about how mobile properties are affected by application scope, see [Mobile properties](../concept/mobile-properties.md).

</td></tr><tr><td>

Description

</td><td>

Description of the mobile property. Enter a description of the property.

</td></tr><tr><td>

Type

</td><td>

Data type of the mobile property record. You must select **True/False** for the **externalScanEnabled** mobile property.

</td></tr><tr><td>

Value

</td><td>

Enter one of the following options:

 -   To enable barcode scanning with an external scanner without denying access to the camera for the mobile app, enter `True`.
-   To turn off the ability to scan barcodes with an external scanner and use the mobile device camera for barcode scanning, enter `False`.


</td></tr><tr><td>

Active

</td><td>

Indicates if the mobile property is activated. If the check box is cleared, the mobile property isn't activated for use.

</td></tr><tr><td>

Is Public

</td><td>

Determines whether the **pre\_auth** property is included in the API response.

 By default, this option is not selected. If you want this property included in the **/pre\_auth** API response, select this checkbox. For more information, see [Adaptive Authentication Events](https://www.servicenow.com/docs/access?context=adaptive-authentication-events&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

 Mobile properties with this checkbox enabled are excluded from the **/user\_client** API response.

</td></tr><tr><td>

Mobile App Config

</td><td>

Mobile app configuration for which you want to use the mobile property. This setting limits the mobile property behavior to users who have access to this mobile app configuration. Other users don't have access to this mobile property and instead experience default behavior.

 To enter a value, either start typing the application name or select the search icon \(![Search icon image](../image/search-icon.png) \). The search dialog box lists the configurations from which you can choose.

 Select one of the following mobile app configs:

-   **Mobile Agent**
-   **Now Mobile**


</td></tr><tr><td>

Mobile Application

</td><td>

Mobile application to which you want to send the mobile property. This setting limits the mobile property behavior to users who have access to this mobile app. Other users don't have access to this mobile property and instead experience default behavior.

 To enter a value, either start typing the application name or select the search icon \(![Search icon image](../image/search-icon.png) \). The search dialog boxt lists the application from which you can choose.

 Select one of the following mobile applications:

-   If you selected **Mobile Agent** for the **Mobile App Config**, select **Agent**.
-   If you selected **Now Mobile** for the **Mobile App Config**, select **Request**.


</td></tr></tbody>
</table>4.  Select **Submit**.


## What to do next

After updating this property, the end-user must pull to refresh and get the latest feature configurations.

**Parent Topic:**[Mobile properties](../concept/mobile-properties.md)

