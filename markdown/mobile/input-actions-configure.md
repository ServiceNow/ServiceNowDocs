---
title: Configure input form actions in an input form screen
description: Add a button next to input form fields to give users the ability to perform various input actions. These actions include adding a comment, adding one or more attachments, and navigating to other screens.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Input form actions, Input actions and input sources, Configure an input form screen, Input form screen, Mobile screen types, Mobile screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Configure input form actions in an input form screen

Add a button next to input form fields to give users the ability to perform various input actions. These actions include adding a comment, adding one or more attachments, and navigating to other screens.

## Before you begin

Role required: admin

This topic describes how to configure input actions for your various input fields. These configurations should be performed within the general setup of input form screens. Additional input action configurations are only available when `Screen` is selected in the **Presentation style** field of the Input form screen. For more information, see [Configure an input form screen](parameter-screen-config.md).

## About this task

Add a more menu button ![More menu icon.](../image/icon-ifs-input-more-iOS.png) by specified input value fields.

**Note:** The button appearance may vary between iOS and Android operating systems. The button is indicated with three dots either horizontally or vertically.

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile App Builder**.

    The Mobile App Builder opens in a new browser tab and displays the application scope selection screen.

2.  Search for the application scope you're working in and then select the name of the application scope.

    The Mobile App Builder categories home screen displays.

3.  Select the **Screens** category and then either select an existing input form screen or **New**.

    If you select **New**, select the **Input form** option in the Create a screen page, and then select **Continue**.

4.  In the Input form screen page, select `Screen` in the **Presentation style** field.

5.  Select **New** in the Actions area to open the Input form action page.

6.  Complete the following fields as needed.

<table id="table_lqq_zxv_21c"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td colspan="2">

Properties

</td></tr><tr><td>

Name

</td><td>

Name of the action.

</td></tr><tr><td>

Label

</td><td>

Label that displays for the action.

</td></tr><tr><td>

Active

</td><td>

Whether the action is active. Inactive actions don't appear on the input form screen.

</td></tr><tr><td>

Available offline

</td><td>

Determine whether this action is available offline.

</td></tr><tr><td>

Input type

</td><td>

Option to choose if your input is populated from another source or modified by an action.**Note:** For this configuration select **Input action**.

 Apply input actions to an input field such as comments, attachments, or navigation functions.

</td></tr><tr><td>

Icon

</td><td>

Icon used to represent your action on the user’s mobile screen.

</td></tr><tr><td colspan="2">

Action Placement

</td></tr><tr><td>

Input form screen

</td><td>

Select the input form screen where the action appears.

</td></tr><tr><td>

Input form section

</td><td>

Select the input form section where the action appears. If the selected input form screen doesn't contain sections, this field isn't available.

</td></tr><tr><td>

Parent table

</td><td>

The parent table that the action applies to. This field is auto-filled.

</td></tr><tr><td>

Parent input

</td><td>

Select which input the action will be applied to.

</td></tr><tr><td>

Action attributes

</td><td>

Determine where or how the action handles the generated data.**Note:** Unless otherwise stated, all the listed attributes are available when you select **Input actions** in the **Input type** field.

**InputActionType**: Input actions are actions that can be triggered in the more menu icon ![More menu icon.](../image/icon-ifs-input-more-iOS.png) displayed by the side of an input value field. The actions are: `attachments`, `comment`, or `button` \(navigation function\).

**ButtonId**: The navigation function associated with the input action. This navigation input action can be either a `global` or `record` context. The *ButtonId* is the sys\_id of a record from the Button \[sys\_sg\_button\] table.

**HiddenAttachmentSources**: Ability to prevent the upload of specific attachment sources from the user. The user can upload only images either from the phone’s camera or the gallery.

**DataSourceID**: The data source used for loading data from the database. Used for comment and attachment input action.

**Note:** An *ElementIdentifier* attribute is also required. For more information, see [Data sources](../concept/data-sources.md).

**ElementIdentifier**: The unique ID contained within a data source, used for loading data from the database. Used for comment and attachment input action.

**Note:** A *DataSourceID* attribute is also required. For more information, see [Data sources](../concept/data-sources.md).

**UserActionID**: A unique value that identifies this action record. It's needed to associate the action with a UI rule.

**Note:** This field is available when the **Input type** field is `Input source`.

</td></tr></tbody>
</table>7.  Enter a name for your input action in the **Name** field.

8.  Enter a label for your input action that is visible to your users, in the **Label** field.

9.  Select **Input action** in the **Input type** field.

10. Select where you want the action to show by completing the following fields in the Action placement area: **Input form screen**, **Parent table**, and **Parent input**.

11. Select **New** in the Action attributes area.

    The input form action attributes opens.

12. Do the following for input actions that you want to include to the input field area.

<table id="choicetable_p4n_gxy_42c"><thead><tr><th align="left" id="d69507e487">

Input action type

</th><th align="left" id="d69507e490">

Procedure

</th></tr></thead><tbody><tr><td id="d69507e496">

**Attachment**

</td><td>

1.  Select **InputActionType** in the **Name** field.
2.  Enter the text `attachments` in the **Value** field.
3.  Select **Save**.


</td></tr><tr><td id="d69507e532">

**Comment**

</td><td>

1.  Select **InputActionType** in the **Name** field.
2.  Enter the text `comment` in the **Value** field.
3.  Select **Save**.


</td></tr><tr><td id="d69507e568">

**Navigation button**

</td><td>

1.  Select **InputActionType** in the **Name** field.
2.  Enter the text `button` in the **Value** field.
3.  Select **Save**.

You're returned to the Input form action attribute table.

4.  Select **New** in the Action attributes area.
5.  Select **ButtonId** in the **Name** field.
6.  Select a preconfigured navigation type in the **Value** field. For more information on creating navigation buttons, see [Navigation functions](../concept/mobile-nav-functions.md).

**Note:** If the navigation function you selected has a Record context \(as opposed to a Global context\), you must map it to the specific record using data sources.

If the *ButtonId* refers to a button with a record context, it defaults to the context of the input form. However, you can override this default context by using the data source to link to a different record context.

7.  Select **Save**.


</td></tr></tbody>
</table>13. Select **Save**.


## What to do next

To open the input form screen with attachments and comments already loaded from the instance \[instance\] table, you must configure the attributes *DataSourceId* and *ElementIdentifier*. For example, in a scenario where multiple users work on the same form, the data source loading mechanism validates that the latest data is displayed to the next user on the input form screen. For a navigation function with a record context, the record context is defined in the data source script. The script maps to the sys\_id of the record that contains a context for the navigation. For more information, see [Configure data sources](data-sources-config.md).

