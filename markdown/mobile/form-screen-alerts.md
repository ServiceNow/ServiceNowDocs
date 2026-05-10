---
title: Configure a mobile alert for a record screen
description: Configure a mobile alert overlay for a record screen to inform users of an important message and to redirect them to a specific screen. Only one mobile alert is available per instance.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Record screen, Mobile screen types, Mobile screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Configure a mobile alert for a record screen

Configure a mobile alert overlay for a record screen to inform users of an important message and to redirect them to a specific screen. Only one mobile alert is available per instance.

## Before you begin

When configuring an alert for a record screen, you must have a record screen to display the alert. See, [Record screen](../concept/form-screen.md).

Role required: admin

## Procedure

1.  Configure a navigation function button for use within a mobile alert.

    1.  In the web-based UI, enter `sys_sg_button.list` in the filter navigator.

    2.  Select the button to use with the mobile alert.

    3.  On the Function, make sure to fill the following fields:

        1.  **Name**: Title for the button
        2.  **Type**: Select the `Navigation` option.
        3.  **Context**: Select the `Record` option.
        4.  **Destination type**: Select the `Screen` option.
    4.  Select the **Condition** tab and define the conditions that apply for the display and the hiding of the mobile alert. For more information, see [Configure a navigation to a screen](sg-config-navigation-function.md).

    5.  Select the **Action Completion** tab.

    6.  In the **Destination screen** field, select the reference lookup icon \(![Reference lookup icon](../image/reference-lookup-icon.png)\) and select a screen where the instance redirects the user to.

    7.  Select **Submit**.

2.  Configure the mobile alert content displayed to the user.

    1.  Enter `sys_sg_alert.list` in the filter navigator.

    2.  On the Mobile Alerts form, click **New**.

    3.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Name|Name of the alert.|
        |Title|Title of the alert message displayed to the user.|
        |Message|Body of the message displayed to the user.|

    4.  Select the **Dismiss Button** tab and enter a text that displays to the user in the **Dismiss button label** field. Examples are "Close" and "Dismiss".

        These texts are translated field types associated with the Translated Name / Fields \[sys\_translated\] table, see [Translated Name / Field table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/system-localization/r_TranslatedNameFieldTable.md).

    5.  Select the **Primary Button** tab.

        1.  Enter a text in the **Primary button label** field that redirects the user to a screen. Examples are "View" and "Display".

            These texts are translated field types associated with the Translated Name / Fields \[sys\_translated\] table, see [Translated Name / Field table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/system-localization/r_TranslatedNameFieldTable.md).

        2.  In the Primary button field, select the reference lookup icon and select the navigation function button you defined earlier.
    6.  Select **Submit**.

3.  Enable the mobile alert in a record screen by adding a reference to the mobile alert.

    1.  Enter `sys_sg_form_screen.list` in the filter navigator.

    2.  Select a record screen that displays the mobile alert.

    3.  In the **Alert** field of the Record screen form, select the reference lookup icon and select the record screen where the alert displays.

    4.  Select **Submit**.


## Result

The mobile alert overlay displays over a list screen. The alert contains a message, the navigation function button, and the option to close the alert. There is also an alert icon \(![Alert icon with a red spot to show call to action is required.](../image/alert-form-screen-icon.png)\) in the screen header. The user can tap on the icon at any time, to review the mobile alert. The red spot indicates to the user that they have not performed the call to action.

![Mobile alert overlay](../image/alert-form-screen.png)

