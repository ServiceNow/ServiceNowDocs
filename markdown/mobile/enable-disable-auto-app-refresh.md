---
title: Turn on or turn off automatic app refresh
description: Use the clientRefresh mobile property on your ServiceNow instance to turn on or turn off automatically refreshing your mobile apps. You can also use the clientRefresh property to adjust the scope of refresh on your mobile app.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Mobile properties, Before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Turn on or turn off automatic app refresh

Use the **clientRefresh** mobile property on your ServiceNow instance to turn on or turn off automatically refreshing your mobile apps. You can also use the **clientRefresh** property to adjust the scope of refresh on your mobile app.

## Before you begin

Role required: admin

## About this task

The **clientRefresh** mobile property is enabled by default on the ServiceNow platform server. Mobile apps that are managed by San Diego and later versions of the server instance automatically refresh after an end user runs action items that change data in records. The data change is immediately visible to the user. Users don't need to refresh their mobile apps. The New Update image no longer appears to prompt an app refresh when this feature is enabled. This feature causes no impact on mobile app performance. Mobile apps only refresh screens that have been previously visited. If you want to turn off this behavior, use the steps described in this task.

Mobile properties are configured as records in the sys\_sg\_properties table on the ServiceNow Platform server. The ServiceNow instance sends the mobile property to mobile apps after authentication. Then the property turns on or turns off a feature on the mobile app. The **clientRefresh** mobile property is configured using JSON scripts.

The **clientRefresh** property is a JSON object with two keys: `isEnabled` and `refreshScope`, which are described in the Mobile properties new record form.

**Important:** Starting with the San Diego release of the ServiceNow server, to turn off refreshing behavior, you must create a new clientRefresh JSON object and set the `isEnabled` key to `false` in the mobile property definition.

## Procedure

1.  Navigate to **All** &gt; **sys\_sg\_properties.list**.

    The Mobile Properties list appears.

2.  In the Mobile Properties list, select **New**.

    The Mobile Properties form appears.

3.  On the form, fill in the fields.

<table id="table_vqz_l1n_vrb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for the mobile property record. Enter `clientRefresh` to make the automatic app refresh feature configurable. Although this feature is turned on by default, you must create it to configure it. It isn't visible on the instance until you create it. **Note:** The record name is case-sensitive and must be entered as `clientRefresh`.

</td></tr><tr><td>

Application

</td><td>

Application scope where the mobile property is applied. To select a different application scope, select the globe icon \(![Globe icon.](../image/globe-icon.png)\) on the instance banner. Then select **Application scope:_application\_scope_**. For information about how mobile properties are affected by application scope, see [Mobile properties](../concept/mobile-properties.md).

</td></tr><tr><td>

Description

</td><td>

Description of the mobile property. Enter a description of the property. For example, `Turns on or turns off automatic refresh of instance data for mobile apps.`

</td></tr><tr><td>

Type

</td><td>

Data type of the mobile property record. You must select **JSON** for the **clientRefresh** mobile property.

</td></tr><tr><td>

Value

</td><td>

The JSON code that configures this feature.-   To disable the feature, enter the following:

    ```
{"isEnabled":false,"refreshScope":"all_tabs"}
    ```

-   To enable the feature, enter the following:

    ```
{"isEnabled":true,"refreshScope":"all_tabs"}
    ```

-   To increase the scope of data that is refreshed, enter the following:

    ```
{"isEnabled":true,"refreshScope":"all_tabs"}
    ```

Using `"all_tabs"` refreshes all screens across all navigation bar tabs after an action is run in the mobile app that changes data in a record.

-   To limit the scope of data that is refreshed, enter the following:

    ```
{"isEnabled":true,"refreshScope":"current_tab"}
    ```

Using `"current_tab"` refreshes just the current navigation bar tab after an action is run in the mobile app.

 **Note:** Use a JSON formatter/validator to make sure that there are no syntax issues.

</td></tr><tr><td>

Active

</td><td>

Option to activate the mobile property. If the check box is cleared, then the mobile property isn't activated for use.

</td></tr><tr><td>

Is Public

</td><td>

Determines whether the **pre\_auth** property is included in the API response.

 By default, this option is not selected. If you want this property included in the **/pre\_auth** API response, select this checkbox. For more information, see Adaptive authentication events.

 Mobile properties with this checkbox enabled are excluded from the **/user\_client** API response.

</td></tr><tr><td>

Mobile App Config

</td><td>

Mobile app configuration for which you want to use the mobile property. This setting limits the mobile property behavior to users who have access to this mobile app configuration. Other users don't have access to this mobile property and instead experience default behavior.To enter a value, either start typing the configuration name or select the search icon. The search dialog box lists the configurations from which you can choose. Select a configuration in the Mobile app configs dialog box.

</td></tr><tr><td>

Mobile Application

</td><td>

Mobile application to which you want to send the mobile property. This setting limits the mobile property behavior to users who have access to this mobile app. Other users don't have access to this mobile property and instead experience default behavior.To enter a value, either start typing the application name or select the search icon. The search dialog box lists the applications from which you can choose. Select an application in the Mobile Applications dialog box.

</td></tr></tbody>
</table>4.  Select **Submit**.


## What to do next

After updating this property, the end user must pull to refresh and get the latest feature configurations.

**Parent Topic:**[Mobile properties](../concept/mobile-properties.md)

