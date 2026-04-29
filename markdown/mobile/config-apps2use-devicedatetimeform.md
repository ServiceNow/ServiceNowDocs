---
title: Configure mobile apps to use the date/time format of mobile devices
description: Set the useDeviceSettingsForDateTimeFormats mobile property to True to configure the date/time fields in mobile apps to use the date/time format that is used on the mobile device.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Mobile properties, Before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Configure mobile apps to use the date/time format of mobile devices

Set the **useDeviceSettingsForDateTimeFormats** mobile property to `True` to configure the date/time fields in mobile apps to use the date/time format that is used on the mobile device.

## Before you begin

Role required: admin

## About this task

The useDeviceSettingsForDateTimeFormats mobile property is available in ServiceNow® mobile app versions 18.2 and later. For more information about ServiceNow mobile app versions, see [Mobile app version history for iOS and Android](https://servicenow.com/docs/bundle/mobile-rn/page/release-notes/mobile-apps/mobile-apps.html).

## Procedure

1.  Navigate to **All** &gt; **sys\_sg\_properties.list**.

    The Mobile Properties list appears.

2.  In the Mobile Properties list, select **New**.

3.  On the form, fill in the fields.

<table id="table_wbl_dlf_rcc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the mobile property record. Enter `useDeviceSettingsForDateTimeFormats` to make this feature configurable.

 The **useDeviceSettingsForDateTimeFormats** property is turned off by default and you must create it on your instance to configure it. It isn't visible on the instance until you create it.

 **Note:** The record name is case-sensitive and must be entered as `useDeviceSettingsForDateTimeFormats`.

</td></tr><tr><td>

Application

</td><td>

Application scope where the mobile property is applied. To select a different application scope, select the globe icon \(![Globe image](../image/globe-icon.png)\) on the instance banner. Then select **Application scope:_application\_scope_**. For information about how mobile properties are affected by application scope, see [Mobile properties](../concept/mobile-properties.md).

</td></tr><tr><td>

Description

</td><td>

Description of the mobile property. Enter a description of the property. For example, `Configures mobile apps to use the date/time format of the mobile device where the app runs`.

</td></tr><tr><td>

Type

</td><td>

Data type of the mobile property record. Select **True/False** for the **useDeviceSettingsForDateTimeFormats** mobile property.

</td></tr><tr><td>

Value

</td><td>

Enter one of the following options:

-   To configure mobile apps to use the date/time format of the mobile device where the app runs, enter `True`.
-   To use the date/time format of the mobile app and ignore the device format, enter `False`.


</td></tr><tr><td>

Active

</td><td>

Whether the mobile property is activated. If the check box is cleared, the mobile property isn't activated for use.

</td></tr><tr><td>

Is Public

</td><td>

Determines whether the **pre\_auth** property is included in the API response.

 By default, this option is not selected. If you want this property included in the **/pre\_auth** API response, select this checkbox. For more information, see [Adaptive authentication events](https://www.servicenow.com/docs/access?context=adaptive-authentication-events&version=australia&pubname=australia-platform-security&ft:locale=en-US).

 Mobile properties with this checkbox enabled are excluded from the **/user\_client** API response.

</td></tr><tr><td>

Mobile App Config

</td><td>

Mobile app configuration that you want to use the mobile property for. This setting limits the mobile property behavior to users who have access to this mobile app configuration. Other users don't have access to this mobile property and instead experience default behavior.

 To enter a value, either start typing the configuration name or select the search icon \(![Magnifying glass image](../image/search-icon.png)\). The search dialog box lists the configurations from which you can choose. Select a configuration for **Mobile App Config**.

</td></tr><tr><td>

Mobile Application

</td><td>

Mobile application that you want to send the mobile property to. This setting limits the mobile property behavior to users who have access to this mobile app. Other users don't have access to this mobile property and instead experience default behavior.

 To enter a value, either start typing the application name or select the search icon \(![Magnifying glass image](../image/search-icon.png)\). The search dialog box lists the applications from which you can choose. Select an application for **Mobile Application**.

</td></tr></tbody>
</table>4.  Select **Submit**.


## What to do next

After updating this property, the end user must refresh the app to get the latest feature configurations.

**Parent Topic:**[Mobile properties](../concept/mobile-properties.md)

