---
title: Configure input form screen actions
description: Learn how to configure actions that affect the whole input form screen. These actions can be accessed with an icon or within a more menu button, located in the top menu bar. For example, you can configure a writeback action to save your work progress on the input form.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Configure an input form screen, Input form screen, Mobile screen types, Mobile screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Configure input form screen actions

Learn how to configure actions that affect the whole input form screen. These actions can be accessed with an icon or within a more menu button, located in the top menu bar. For example, you can configure a writeback action to save your work progress on the input form.

## Before you begin

Role required: admin

A loading mechanism is required to refresh the input form screen with updated data. The options available are autofill variables and data sources. For more information, see [Loading mechanisms for input form screens](../concept/loading-mechanisms.md).

If your input form only includes input values for loading, and you don’t need to load an input type of attachment, then the autofill variable option is sufficient. If your input form includes either attachments, comments, or descriptive elements, the data source option must be used. The data source option also handles input values.

## About this task

Input form screen actions are accessed in the top menu as either an icon \(![More menu icon.](../image/icon-ifs-save-progress.png)\) or within the more menu button options \( ![More menu button.](../image/IconAppMenuAndroid.png)\). The configuration of the writeback action in this task explains how to create a function that enables users to save the progress of data entered in an input form screen before users submit the final version. This feature enables multiple users to collaborate on a single input form screen. Once a user saves the data, it becomes visible to all other users working on the form when they refresh their input form. Writeback actions use the action item function. For more information, see [Configure an action item](sg-studio-create-action-item.md).

**Note:** Input form screens contain a submit button. For this configuration you have the option to configure a save-as-you-work option, the data of which is available to other users after it is saved.

|Top navigation more menu \(iOS\)|Top menu icon for input form screen action|
|--------------------------------|------------------------------------------|
|![Top navigation more menu (iOS).](../image/ifs-top-nav-menu-iOS.png)|![Top menu button for input form screen action.](../image/ifs-top-nav-icon.png)|

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile App Builder**.

    The Mobile App Builder opens in a new browser tab and displays the application scope selection screen.

2.  Search for the application scope you're working in and then select the name of the application scope.

    The Mobile App Builder categories home screen displays.

3.  Select the **Screens** category and then either select an existing input form screen or **New**.

    If you select **New**, select the **Input form** option in the Create a screen page, and then select **Continue**.

4.  In the Input form screen page, select **Screen** in the **Presentation style** field.

5.  Complete the Input form screen form as required.

    For information about the various fields, see [Configure an input form screen](parameter-screen-config.md).

6.  Select one of the following options:

    -   To add the input form screen action as a top menu icon, select **New** in the Top icon function instances area.
    -   To add the input form screen action as a function in the top menu more \(![Top menu more button.](../image/IconAppMenuAndroid.png)\) button, select **New** in the Top menu function instances area.
    **Note:** The subsequent instructions are the same for either top icon or top menu function instances.

7.  In the Function instance form do the following:

    1.  Enter a **Name** for the function instance.
    2.  Enter a name in the **Display label** field.
    3.  Select an icon from the **Icon** field.

        **Note:** This field is required if you selected the **Top icon function instances** option.

    4.  Select **New** in the Function area, to display the function form.
8.  Enter a **Name** for the function.

9.  Select **Action item** in the Type field.

10. Select **Record** in the Context field.

11. Either **Choose** or create a **New** action item.

    For more information, see [Configure an action item](sg-studio-create-action-item.md).

12. In the **Data** field, select the table relating to what the input form is representing.

13. In the Button attributes area, do the following:

    1.  Select **New**.
    2.  From the **Name** field, select `retain_parent_parameter_screen`. This attribute verifies the parent input form \(the input form that you're working on\) opens when the user taps the button, as opposed to launching a new input form.
    3.  Enter `true` in the **Value** field.
    4.  Select **Save**.
    5.  From the **Name** field, select `refresh_parameter_screen_after_action`. This attribute refreshes the input form with the latest data from the instance.

        **Note:** To display the data in the input form after the save action, you must configure one of the following loading mechanisms:

        -   Autofill variable: For more information, see [Configure input form screen inputs](param-screen-config-inputs.md).
        -   Data source: For more information, see [Data sources](../concept/data-sources.md).
    6.  Enter `true` in the **Value** field.
    7.  Select **Save**.
14. Select **Save**.


## What to do next

**Use timestamps to track users changes in the input form**. To monitor the changes made by different users on an input form screen, you must enable the track timestamps option and use a script. The **Track timestamps for input updates** field is on the main input form screen record. For more information, see [Configure an input form screen](parameter-screen-config.md). It tracks the time the input’s value changed. This information is accessible using the scripted writeback action. For a code example of this writeback action, see [Using timestamps to track user changes in an input form](../reference/track-timestamp-script.md).

