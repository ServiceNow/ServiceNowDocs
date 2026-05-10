---
title: Turn off the Zero Trust Access banner on mobile apps
description: Learn how to turn off the banner on mobile app screens where Zero Trust Access \(ZTA\) is enabled.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Mobile properties, Before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Turn off the Zero Trust Access banner on mobile apps

Learn how to turn off the banner on mobile app screens where Zero Trust Access \(ZTA\) is enabled.

## Before you begin

Role required: Security admin

## About this task

When ZTA is enabled on your ServiceNow instance, end users see a banner at the top of their mobile app screen each time the network connection state changes. For example, when the end user logs in or when the mobile access token expires, and the instance requests a refreshed token. This can occur several times due to internal app management and end users see this banner every time. While this informs the user when their network connection changes, it can make it difficult to use the mobile app.

To enhance usability of the mobile app, admins can set the **disableZTABanner** mobile property to on the instance. When this property is set to `True`, display of the banner is suppressed on mobile app screens.

**Important:** By default, this mobile property isn’t set and produces the same behavior as setting the property to `False` where the ZTA banner displays for all connection`True` state changes.

## Procedure

1.  Navigate to **All** &gt; **sys\_sg\_properties.list**.

    The Mobile Properties list appears.

2.  In the Mobile Properties list, select **New**.

    The Mobile Properties form appears.

3.  On the form, fill in the fields.

<table id="table_jgf_5sv_s2c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for the mobile property record. Enter `disableZTABanner` to suppress the ZTA banner on mobile apps when connection state changes.

**Note:** The record name is case-sensitive and must be entered as `disableZTABanner`.

</td></tr><tr><td>

Application

</td><td>

Application scope where the mobile property is applied. To select a different application scope, select the globe icon \(![globe image](../image/globe-icon.png)\) on the instance banner. Then select **Application scope: _application\_scope_**.

 For information about how mobile properties are affected by application scope, see [Mobile properties](../concept/mobile-properties.md).

</td></tr><tr><td>

Description

</td><td>

Description of the mobile property. Enter a description of the property. For example, `Turns off the ZTA banner on mobile app screens`.

</td></tr><tr><td>

Type

</td><td>

Data type of the mobile property record. Select **True/False** for the **disableZTABanner** property.

</td></tr><tr><td>

Value

</td><td>

The following values can be entered:

-   To suppress the ZTA banner on mobile apps when connection states change, enter `True`.
-   To enable the ZTA banner on mobile apps when connection states change, enter `False`.
**Important:** By default, this mobile property isn’t set and produces the same behavior as setting the property to `False` where the ZTA banner displays for all connection state changes.

</td></tr><tr><td>

Active

</td><td>

Option to activate the mobile property. If the check box is cleared, the mobile property isn't activated for use.

</td></tr><tr><td>

Is Public

</td><td>

Determines whether the **pre\_auth** property is included in the API response.

 By default, this option is not selected. If you want this property included in the **/pre\_auth** API response, select this checkbox. For more information, see [Adaptive authentication events](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/authentication/adaptive-authentication-events.md).

 Mobile properties with this checkbox enabled are excluded from the **/user\_client** API response.

</td></tr><tr><td>

Mobile App Config

</td><td>

Mobile app configuration for which you want to use the mobile property. This setting limits the mobile property behavior to users who have access to this mobile app configuration. Other users don't have access to this mobile property and instead experience default behavior.

 To enter a value, either start entering the application name or select the search icon \(![magnifying glass image](../image/search-icon.png)\). The search dialog box lists the configurations from which you can choose.

 Select one of the following mobile app configs:

-   **Mobile Agent**
-   **Now Mobile**


</td></tr><tr><td>

Mobile Application

</td><td>

Mobile application to which you want to send the mobile property. This setting limits the mobile property behavior to users who have access to this mobile app. Other users don't have access to this mobile property and instead experience default behavior.

 To enter a value, either start to type the application name or select the search icon \(![magnifying glass image](../image/search-icon.png)\). The search dialog box lists the applications from which you can choose.

 Select one of the following mobile applications:

-   If you selected **Mobile Agent** for the **Mobile App Config**, select **Agent**.
-   If you selected **Now Mobile** for the **Mobile App Config**, select **Request**.


</td></tr></tbody>
</table>4.  Select **Submit**.


## What to do next

After updating this property, the end user must pull to refresh and get the latest feature configurations.

**Parent Topic:**[Mobile properties](../concept/mobile-properties.md)

