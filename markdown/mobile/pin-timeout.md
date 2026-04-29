---
title: PIN timeout
description: Configure the PINIdleTimeout property to define the PIN timeout for different ServiceNow mobile apps. You can use this property to enhance security by controlling how long users are allowed to remain inactive before being required to reenter their PIN.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Mobile properties, Before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# PIN timeout

Configure the PINIdleTimeout property to define the PIN timeout for different ServiceNow mobile apps. You can use this property to enhance security by controlling how long users are allowed to remain inactive before being required to reenter their PIN.

## Before you begin

Role required: admin

## About this task

The PINIdleTimeout property lets you set different inactivity timeouts according to mobile app type. The property provides the option that higher-security apps like the Mobile Agent app can lock sooner, while lower-risk apps, like the Now Mobile app, can give users more time before reprompting to log in.

**Note:** If this property isn't defined, the default PIN timeout is 300 seconds.

## Procedure

1.  Navigate to **All** &gt; **sys\_sg\_properties.list**.

    The Mobile Properties list appears.

2.  In the Mobile Properties list, select **New**.

    The Mobile Properties form appears.

3.  On the form, fill in the fields as required.

<table id="table_abx_zjt_l3c"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the mobile property record. Enter `PINIdleTimeout` to make this feature configurable.The PINIdleTimeout property is turned off by default and you must create it on your instance to configure it. It isn't visible on the instance until you create it

</td></tr><tr><td>

Application

</td><td>

Application scope where the mobile property is applied. To select a different application scope, select the globe icon \(![globe image](../image/globe-icon.png)\) on the instance banner. Then select **Application scope: _application\_scope_**.

 For information about how mobile properties are affected by application scope, see [Mobile properties](../concept/mobile-properties.md).

</td></tr><tr><td>

Description

</td><td>

Description of the mobile property. Enter a description of the property. For example, `Configure length of time mobile app is opened before login is required`.

</td></tr><tr><td>

Type

</td><td>

Data type of the mobile property record. For this property, select **Integer**.

</td></tr><tr><td>

Value

</td><td>

Enter the value in seconds for how long the mobile app remains open before the app times out and login is required again. Consider the following:-   Default value is 300 seconds
-   The value range is from 30 through 900 seconds
-   If the entered value is below 30 or above 900 seconds, the system uses the default value of 300 seconds.
-   The timeout mechanism keeps counting even when the app is minimized or closed.


</td></tr><tr><td>

Active

</td><td>

Whether the mobile property is activated. If the check box is cleared, the mobile property isn't activated for use.

</td></tr><tr><td>

Is Public

</td><td>

Determines whether the **pre\_auth** property is included in the API response.

 By default, this option isn't selected. If you want this property included in the **/pre\_auth** API response, select this check box. For more information, see [Adaptive authentication events](https://www.servicenow.com/docs/access?context=adaptive-authentication-events&version=australia&pubname=australia-platform-security&ft:locale=en-US).

 Mobile properties with this check box enabled are excluded from the **/user\_client** API response.

</td></tr><tr><td>

Mobile App Config

</td><td>

Mobile app configuration for which you want to use the mobile property. This setting limits the mobile property behavior to users who have access to this mobile app configuration. Other users don't have access to this mobile property and instead experience default behavior.

 To enter a value, either start entering the application name or select the search icon \(![magnifying glass image](../image/search-icon.png)\). The search dialog box lists the configurations from which you can choose.

</td></tr><tr><td>

Mobile Application

</td><td>

Mobile application to which you want to send the mobile property. This setting limits the mobile property behavior to users who have access to this mobile app. Other users don't have access to this mobile property and instead experience default behavior.

 To enter a value, either start to type the application name or select the search icon \(![magnifying glass image](../image/search-icon.png)\). The search dialog box lists the applications from which you can choose.

</td></tr></tbody>
</table>4.  Enter `PINIdleTimeout` in the **Name** field.

5.  Select **Integer** in the **Type** field.

6.  In the **Value** field, select between 30-900 seconds to define the length of time the app remains open before the user is required to log in again.

7.  Select **Submit**.


## What to do next

After updating this property, the end user must refresh the app to get the latest feature configurations.

**Parent Topic:**[Mobile properties](../concept/mobile-properties.md)

