---
title: Configure an input form screen
description: Configure an input parameter so that your users can see a list of records from their mobile app. To access a record from the list, a user just has to tap the record name.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 9
breadcrumb: [Input form screen, Mobile screen types, Mobile screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Configure an input form screen

Configure an input parameter so that your users can see a list of records from their mobile app. To access a record from the list, a user just has to tap the record name.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile App Builder**.

    The Mobile App Builder opens in a new browser tab and displays the application scope selection screen.

2.  Search for the application scope you are working in and then select the name of the application scope.

    The Mobile App Builder categories home screen displays.

3.  Select the **Screens** category, and then select **New**.

4.  Select the **Input form** option in the Create a screen page, and then select **Continue**.

5.  Complete the following fields as needed.

<table id="table_sk5_jmq_pnb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Properties

</td></tr><tr><td>

Name

</td><td>

The name of your screen. This name appears as a tile in the mobile application.

</td></tr><tr><td>

Description

</td><td>

Additional information about the screen.

</td></tr><tr><td>

Active

</td><td>

Option to set the input form screen as active. Inactive screens do not appear in your mobile apps.

</td></tr><tr><td class="sub-head" colspan="2">

Settings

</td></tr><tr><td>

Available offline

</td><td>

Option to make the input form screen is available in offline mode. For details on offline mode, see [Offline mode](../concept/mobile-offline-mode.md).

</td></tr><tr><td>

Resume from local device after canceling

</td><td>

Option to enable the resume on cancel option. When enabled, data entered on the screen is saved in memory when a user clicks **Cancel**. The data is loaded when the user returns to the screen later.

</td></tr><tr><td>

Reset after submit

</td><td>

Option to reset the input form screen to its default state after an action is submitted. The **Reset after Submit** setting enables users to submit multiple actions that must be saved to the ServiceNow instance without having to reopen the input form screen.To configure this setting, do the following:

1.  Select **Save** to save the input form screen.
2.  Select the options menu icon \(![Option menu icon.](../image/mab-option-menu.png)\) in the upper right corner of the form in Mobile App Builder and select **Open in platform**.
3.  Select the **Settings** tab.
4.  Select the **Reset after Submit** check box.
5.  Select **Update** to save the setting.
6.  Navigate back to Mobile App Builder by selecting that browser tab.


</td></tr><tr><td>

Track timestamps for input updates

</td><td>

Option to add timestamps for inputted data. For example, use this option to track inputs from various users within an input form screen. The timestamp data is extracted using scripted code of the action item type “script”. For an example script to demonstrate how to extract timestamp data, see [Using timestamps to track user changes in an input form](../reference/track-timestamp-script.md).

</td></tr><tr><td>

Fetch Type

</td><td>

Fetch type settings determine when data is loaded in screens. Change your fetch type to optimize load time performance for your screens. Select from **Background**, **Dynamic prefetch**, **On-demand**, or **Prefetch** as required for your setup. For more information about these options, see [Mobile fetch types](../reference/applet-fetch-types.md).

</td></tr><tr><td>

Header Only on First Page

</td><td>

Option to make the header visible only on the first page of the input form screen.

</td></tr><tr><td>

Presentation style

</td><td>

Determine the display of the input form screen in your app. The following choices are available:-   **Modal**: This is the standard presentation style and is primarily used for completing and uploading a form. Descriptive elements are available in this mode. Navigation tabs are not available, so that the user remains focused on the form.

Select this option, for example, where you want to create a basic input form with about ten fields that need to be worked on by an individual.

-   **Screen**: The screen presentation contains all the features of modal, as well as the ability to add additional configuration. For example, input actions and the ability to save the changes as users progress through the input form, as well as descriptive elements. You are also able to navigate to other tabs while working on an input form.

When you select the Screen option other fields in this form are available, as indicated in this table.

</td></tr><tr><td>

Header Card

</td><td>

An optional mobile view to display at the top of your input form screen. There can only be one header card for each input form screen. Select **Choose** to add an existing header card, or select **New** to configure one. For more information on view configuration, see [Understanding mobile cards and legacy cards](../reference/mcb-itemvew-v-viewconfig.md).**Note:** The header card supports buttons for navigation purposes only. Buttons can be used to navigate to another screen. Any other button functionality is not supported within the header card.

</td></tr><tr><td class="sub-head" colspan="2">

Buttons

</td></tr><tr><td>

Cancel label

</td><td>

Label for the button used to cancel the input form screen.

</td></tr><tr><td>

Next label

</td><td>

Label for the button used to advance to the next page of the input form screen.

</td></tr><tr><td>

Previous label

</td><td>

Label for the button used to return to the previous page of the input form screen.

</td></tr><tr><td>

Submit label

</td><td>

Label for the button used to submit the input form screen.

</td></tr><tr><td>

Unsaved changes messages

</td><td>

**Note:** This field displays when you select **Screen** in the **Presentation** style field.

 Select this option to determine the messages shown when a user attempts to close an input form screen with unsaved changes. The following actions trigger the display of a confirmation message while the input form is open:

-   Tapping the back button.
-   Tapping the same navigation tab the input form is currently opened on.
-   Using the pull-to-refresh options in any navigation tab.
**Note:** When the field **Resume from local device after canceling** is enabled, tapping the back button does not trigger the message and your changes are saved locally.

 The following fields need to be defined within the **Unsaved changes messages** area:

-   Confirmation message title
-   Confirmation message body
-   Confirmation button label
-   Cancel button label
![Unsaved changes confirmation message within an input form screen.](../image/unsaved-changes.png)

</td></tr><tr><td>

Input form page display

</td><td>

The way that information is displayed on your input form screen. Select one of the following options, as required for your setup:-   **Individual page for each input**: Choose this option to place each input field on its own page in your mobile app. Select this option for complex input types.
-   **Custom page and section setup**: Choose this option when you have multiple input fields that must appear on the same page in your mobile app. If you choose this option, more configuration options appear at the bottom of the form where you can configure **Pages** and **Section mappings**.


</td></tr><tr><td>

Inputs

</td><td>

Input fields that you want to appear on your input form screen. Select **New** to add a new input field. For more information about configuring input fields, see [Configure input form screen inputs](param-screen-config-inputs.md).

</td></tr><tr><td>

Variables

</td><td>

Variables that are to be used in your input form screen. Variables define what information is collected from the user automatically or the default information for an input. Select **New** to add a new variable. For more information about configuring variables, see [Configure attributes for input form screen variables](param-screen-config-variables.md).

</td></tr><tr><td>

Actions

</td><td>

Actions that you want to appear on an Input field to trigger a UI rule. Created actions will be shown on the keyboard when the user selects the specified input. For more information about configuring actions, see [Configure input sources in an input form screen](param-screen-config-actions.md).

</td></tr><tr><td>

UI rules

</td><td>

Define what elements of the mobile interface displays and which fields update when certain conditions are met. For more information, see [Mobile UI Rules](../concept/mobile-ui-rules.md).

</td></tr><tr><td>

Pages

</td><td>

**Note:** This field displays when you select **Custom page and section setup** in the **Input form page display** area.

The sections or inputs that appear on your input form screen when there are multiple pages. Select **New** to define a new page. For more information about configuring pages, see [Configure input form pages](parameter-screen-page-config.md).

</td></tr><tr><td>

Section mappings

</td><td>

**Note:** This field displays when you select **Custom page and section setup** in the **Input form page display** area.

The way that sections are displayed on your input form screen. You can configure how each section displays and the order of sections. Select **New** to define a new section mapping. For more information about configuring section mappings, see [Configure input form sections](parameter-screen-sections-create.md).

</td></tr><tr><td>

Top icon function instances

</td><td>

Define an input form screen action to display as an icon in the top menu section of your mobile app.Tapping on this input form screen action activates a writeback action, for example, allows users to save the progress of data entered in an input form screen before the final version is uploaded. Following the writeback action, a refresh takes place and the input form screen updates to display any recent changes from other users.

**Note:** This field displays when you select `Screen` in the **Presentation style** field.

There can only be one function instance per input form screen, either as a top menu icon or within the top menu function.

 For more information, see [Configure input form screen actions](input-form-screen-actions-config.md).

</td></tr><tr><td>

Top menu function instances

</td><td>

Define an input form screen action to display within the more menu \(![More menu.](../image/IconAppMenuAndroid.png)\) the top menu section of your mobile app.Tapping on this input form screen action activates a writeback action, for example, allows users to save the progress of data entered in an input form screen before the final version is uploaded. Following the writeback action, a refresh takes place and the input form screen updates to display any recent changes from other users.

**Note:** This field displays when you select `Screen` in the **Presentation style** field.

There can only be one function instance per input form screen, either as a top menu icon or within the top menu function.

 For more information, see [Configure input form screen actions](input-form-screen-actions-config.md).

</td></tr></tbody>
</table>6.  Select **Save**.


