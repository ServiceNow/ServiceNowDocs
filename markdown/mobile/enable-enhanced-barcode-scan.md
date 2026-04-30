---
title: Enable enhanced barcode scanning
description: Add the EnableCameraFocusEnhancement and the EnableMaxCameraResolution mobile properties to enhance barcode scanning for Android devices.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Mobile properties, Considerations before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Enable enhanced barcode scanning

Add the **EnableCameraFocusEnhancement** and the **EnableMaxCameraResolution** mobile properties to enhance barcode scanning for Android devices.

## Before you begin

Role required: admin

## About this task

**Important:**

To scan barcodes as accurately as possible, make sure that you:

-   Scan in a well-lit environment. Both Android and iOS mobile devices have flashlight apps that you can use to make sure your device's camera has adequate light to scan barcodes accurately.
-   Keep the device camera in a steady position while scanning. If the camera is shaking, barcode scans will become blurred and inaccurate.

You can enable enhanced barcode scanning on your instance for Android devices by adding the following mobile properties:

<table id="table_v5b_byq_tzb"><thead><tr><th>

Mobile property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**EnableCameraFocusEnhancement**

</td><td>

Enables auto-zooming, which improves accuracy. This only applies to hardware that supports auto-zooming.

</td></tr><tr><td>

**EnableMaxCameraResolution**

</td><td>

Enables the highest possible resolution that the hardware can support. Use this for frame rendering.**Note:** Newer, more powerful hardware can best take advantage of this mobile property.

</td></tr></tbody>
</table>**Important:** These mobile properties are only supported on Android devices.

## Procedure

1.  Navigate to **All** &gt; **sys\_sg\_properties.list**.

    The Mobile Properties list appears.

2.  In the Mobile Properties list, select **New**.

    The Mobile Properties form appears.

3.  On the form, fill in the fields for the **EnableCameraFocusEnhancement** mobile property.

<table id="table_pqg_xyq_tzb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for the mobile property record. Enter `EnableCameraFocusEnhancement` to enable auto-zooming for hardware that supports this feature.**Note:** The record name is case-sensitive and must be entered as `EnableCameraFocusEnhancement`.

</td></tr><tr><td>

Application

</td><td>

Application scope where the mobile property is applied. To select a different application scope, select the globe icon \(![Globe icon](../image/globe-icon.png)\) on the instance banner. Then select **Application scope:_application\_scope_**.

 For information about how mobile properties are affected by application scope, see [Mobile properties](../concept/mobile-properties.md).

</td></tr><tr><td>

Description

</td><td>

Description of the mobile property. Enter a description of the property. For example, `Enables auto-zooming for barcode scanning`.

</td></tr><tr><td>

Type

</td><td>

Data type of the mobile property record. You must select **True/False** for the **EnableCameraFocusEnhancement** mobile property.

</td></tr><tr><td>

Value

</td><td>

Enter one of the following options:-   To enable auto-zooming for barcode scanning, enter `True`.
-   To turn off auto-zooming for barcode scanning, enter `False`.


</td></tr><tr><td>

Active

</td><td>

Whether the mobile property is activated. If the check box is cleared, the mobile property isn't activated for use.

</td></tr><tr><td>

Is Public

</td><td>

Determines whether the **pre\_auth** property is included in the API response.

 By default, this option is not selected. If you want this property included in the **/pre\_auth** API response, select this checkbox. For more information, see [Adaptive Authentication Events](https://www.servicenow.com/docs/access?context=adaptive-authentication-events&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

 Mobile properties with this checkbox enabled are excluded from the **/user\_client** API response.

</td></tr><tr><td>

Mobile App Config

</td><td>

Mobile app configuration for which you want to use the mobile property. This setting limits the mobile property behavior to users who have access to this mobile app configuration. Other users don't have access to this mobile property and instead experience default behavior.

 Select one of the following mobile app configs:

-   **Mobile Agent**
-   **Now Mobile**


</td></tr><tr><td>

Mobile Application

</td><td>

Mobile application to which you want to send the mobile property. This setting limits the mobile property behavior to users who have access to this mobile app. Other users don't have access to this mobile property and instead experience default behavior.

 Select one of the following mobile applications:

-   If you selected **Mobile Agent** for the **Mobile App Config**, select **Agent**.
-   If you selected **Now Mobile** for the **Mobile App Config**, select **Request**.


</td></tr></tbody>
</table>4.  Select **Submit**.

    The Mobile Properties list appears.

5.  In the Mobile Properties list, select **New**.

    The Mobile Properties form appears.

6.  On the form, fill in the fields for the **EnableMaxCameraResolution** mobile property.

    Refer to Step 3 for information about how to complete the fields.

    **Important:** The Name field is case-sensitive and must be entered as **EnableMaxCameraResolution**.

7.  When you have completed the Mobile Properties form for the **EnableMaxCameraResolution** mobile property, select **Submit**.


## What to do next

-   To confirm that the properties have been added, make sure they appear in the Mobile Properties list after you select **Submit**.
-   End users must pull to refresh and get the latest feature configurations.

**Parent Topic:**[Mobile properties](../concept/mobile-properties.md)

