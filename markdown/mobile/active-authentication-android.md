---
title: Keep native apps active during authentication on Android devices
description: Use the preventAppKillOnAuth property on your ServiceNow instance to help prevent Android devices from killing the mobile app when put to background during login. Use this configuration to allow for a smoother authentication experience by keeping the app active until users complete or cancel the login process.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-12-08"
reading_time_minutes: 3
breadcrumb: [Mobile properties, Considerations before implementation, ServiceNow Mobile Platform configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Keep native apps active during authentication on Android devices

Use the **preventAppKillOnAuth** property on your ServiceNow instance to help prevent Android devices from killing the mobile app when put to background during login. Use this configuration to allow for a smoother authentication experience by keeping the app active until users complete or cancel the login process.

## Before you begin

Role required: admin

## About this task

**Note:** The **preventAppKillOnAuth** may need to be set only if you're experiencing login issues, where the app restarts after being put in the background and then is resumed. After such restarts, the app can fail to redirect to the native mobile interface after login. This issue was found to occur on OEM devices like Redmi, POCO, and Oppo.

The **preventAppKillOnAuth** property is a pre-authenticated mobile setting that when set to true signals to the system that an important task is in progress. This setting maintains that the mobile app remains alive during the authentication process even when moved to the background.

Mobile properties are configured as records in the sys\_sg\_properties table on the  ServiceNow Mobile Platform server.

**Note:**  The **preventAppKillOnAuth** property is supported from the 20.6.0 mobile client release.

-   **Example**

    When you open an authenticator app to retrieve code or approve a login request, the ServiceNow mobile app moves to the background. In such a situation the Android OS may terminate the app in the following circumstances:

    -   If the device is running low on memory.
    -   If the battery saver mode enabled.
    -   If the system settings has a limit to the number of background apps enabled to run simultaneously.

## Procedure

1.  Navigate to **All** &gt; **sys\_sg\_properties.list**.

    The Mobile Properties list displays.

2.  In the Mobile Properties list, select **New**.

    The Mobile Properties form displays.

3.  On the form, fill in the fields as required.

<table id="table_pqg_xyq_tzb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for the mobile property record. Enter `preventAppKillOnAuth` to make this feature configurable. The  `preventAppKillOnAuth` property is turned off by default and you must create it on your instance to configure it.

</td></tr><tr><td>

Application

</td><td>

Application scope where the mobile property is applied. To select a different application scope, select the globe icon \(![Globe icon](../image/globe-icon.png)\) on the instance banner. Then select **Application scope:_application\_scope_**.

 For information about how mobile properties are affected by application scope, see [Mobile properties](../concept/mobile-properties.md).

</td></tr><tr><td>

Description

</td><td>

Description of the mobile property. Enter a description of the property. For example, `Determines whether app remains alive during auth process`.

</td></tr><tr><td>

Type

</td><td>

Data type of the mobile property record. You must select **True/False** for the **preventAppKillOnAuth** mobile property.

</td></tr><tr><td>

Value

</td><td>

Enter one of the following options:-   To request Android OS, to keep app alive all through authentication process, enter `True`.
-   To enable Android OS to manage the app using standard background processes during authentication, enter `False`. This is the default value.


</td></tr><tr><td>

Active

</td><td>

Determine whether the mobile property is activated. If the check box is cleared, the mobile property isn't activated for use.

</td></tr><tr><td>

Is Public

</td><td>

Determines whether this property is publicly available in the **pre\_auth** API to mobile devices, even before logging in to the instance.

 Select this check box to enable the property functionality.

</td></tr><tr><td>

Mobile App Config

</td><td>

Not relevant for this configuration. When the **Is Public** field is selected, this field isn't available

</td></tr><tr><td>

Mobile Application

</td><td>

Enter either `Agent`, `Request`, or the name of a custom app type created by users of Mobile Publishing. Alternatively, leave the field empty to apply this property for all supported app types or variants.

 To enter a value, either start entering the application name or select the search icon. The search dialog box lists the applications from which you can choose. Select an application in the Mobile Applications dialog box.

</td></tr></tbody>
</table>4.  Enter the property name `preventAppKillOnAuth`, in the **Name** field.

5.  Select **True/False** in the **Type** field.

6.  Enter `true` in the **Value** field.

7.  Select **Is Public**.

8.  Select **Submit**.


**Parent Topic:**[Mobile properties](../concept/mobile-properties.md)

