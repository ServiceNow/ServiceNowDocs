---
title: Switch the date/time fields between device time zone and UTC
description: Use the ShowDateTimeInUTC mobile property to determine whether the date/time field values in the Now Mobile app are displayed in the time zone of the user's device \(default\) or are converted to UTC.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Mobile properties, Considerations before implementation, ServiceNow Mobile Platform configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Switch the date/time fields between device time zone and UTC

Use the **ShowDateTimeInUTC** mobile property to determine whether the date/time field values in the Now Mobile app are displayed in the time zone of the user's device \(default\) or are converted to UTC.

## Before you begin

Role required: admin

## About this task

The **ShowDateTimeInUTC** mobile property value is **false** and not defined by default. When set to **false** or not defined, the Now Mobile app displays the time and date according to the time zone of a user’s device. Instead, set **ShowDateTimeInUTC** to **true** to display the time and date according to Coordinated Universal Time \(UTC\).

Both [Mobile Card Builder](../concept/mobile-card-builder.md) and the following mobile screens support the **ShowDateTimeInUTC** property:

-   [Input form screen](../concept/parameter-input-screen.md)
-   [Record screen](../concept/form-screen.md)

Mobile properties are configured as records in the sys\_sg\_properties table on the ServiceNow® Platform server. The ServiceNow instance sends the mobile property to mobile apps after authentication. Then the property turns on or turns off a feature on the mobile app.

## Procedure

1.  Navigate to **All** &gt; **sys\_sg\_properties.list**.

2.  In the Mobile Properties list, select **New**.

3.  On the form, fill in the fields.

<table id="table_vqz_l1n_vrb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the mobile property record. Enter `ShowDateTimeInUTC` to make this feature configurable. This feature is turned off by default and you must create it on your instance to configure it. It isn't visible on the instance until you create it. **Note:** The record name is case-sensitive and must be entered as `ShowDateTimeInUTC`.

</td></tr><tr><td>

Application

</td><td>

Application scope where the mobile property is applied. To select a different application scope, select the globe icon \(![Globe icon.](../image/globe-icon.png)\) on the instance banner. Then select **Application scope:_application\_scope_**. For information about how mobile properties are affected by application scope, see [Mobile properties](../concept/mobile-properties.md).

</td></tr><tr><td>

Description

</td><td>

Description of the mobile property. Enter a description of the property. For example, `Determines whether users see date/time according to UTC or according to their device's time zone.`

</td></tr><tr><td>

Type

</td><td>

Data type of the mobile property record. Select **True/False** for the **ShowDateTimeInUTC** mobile property.

</td></tr><tr><td>

Value

</td><td>

The following values can be entered:

-   To show the users date/time according to UTC, enter `True`
-   To show the users date/time according to the time zone of their device, enter `False`.


</td></tr><tr><td>

Active

</td><td>

Option to activate the mobile property. If the check box is cleared, the mobile property isn't activated for use.

</td></tr><tr><td>

Is Public

</td><td>

Determines whether the **pre\_auth** property is included in the API response.

 By default, this option is not selected. If you want this property included in the **/pre\_auth** API response, select this checkbox. For more information, see [Adaptive Authentication Events](https://www.servicenow.com/docs/access?context=adaptive-authentication-events&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

 Mobile properties with this checkbox enabled are excluded from the **/user\_client** API response.

</td></tr><tr><td>

Mobile App Config

</td><td>

Mobile app configuration that you want to use the mobile property for. This setting limits the mobile property behavior to users who have access to this mobile app configuration. Other users don't have access to this mobile property and instead experience default behavior.To enter a value, either start typing the configuration name or select the search icon \(![Search icon.](../image/search-icon.png)\). The search dialog box lists the configurations from which you can choose. Select a configuration for **Mobile App Config**.

</td></tr><tr><td>

Mobile Application

</td><td>

Mobile application that you want to send the mobile property to. This setting limits the mobile property behavior to users who have access to this mobile app. Other users don't have access to this mobile property and instead experience default behavior.To enter a value, either start typing the application name or select the search icon \(![Search icon.](../image/search-icon.png)\). The search dialog box lists the applications from which you can choose. Select an application for **Mobile Application**.

</td></tr></tbody>
</table>4.  Select **Submit**.


## What to do next

After updating this property, the end user must refresh the data from the instance to get the latest feature configurations.

**Parent Topic:**[Mobile properties](../concept/mobile-properties.md)

