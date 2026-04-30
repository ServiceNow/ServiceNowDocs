---
title: Configure input sources in an input form screen
description: Configure the actions that you want to appear on an Input field to trigger a UI rule. These input source actions are shown above the keyboard, or next to the selected input. Use it to configure summarization actions for GenAI.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Input actions and input sources, Configure an input form screen, Input form screen, Mobile screen types, Mobile screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Configure input sources in an input form screen

Configure the actions that you want to appear on an Input field to trigger a UI rule. These input source actions are shown above the keyboard, or next to the selected input. Use it to configure summarization actions for GenAI.

## Before you begin

You must create an input form screen before you can create actions. For information about creating an input form screen, see [Configure an input form screen](parameter-screen-config.md).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile App Builder**.

    The Mobile App Builder opens in a new browser tab and displays the application scope selection screen.

2.  Search for the application scope you're working in and then select the name of the application scope.

    The Mobile App Builder categories home screen displays.

3.  Select the **Screens** category and then select the input form screen for which you want to configure variables.

4.  Scroll down to the Actions section of the form, and select **New** to create a variable.

    The Action form appears.

5.  Complete the following fields as needed.

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

Option to choose if your input is populated from another source or modified by an action.**Note:** For this configuration select `Input source`.

Input source: Provides users with the option of text summarization using GenAI

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

Select which input the action is applied.

</td></tr><tr><td>

Action attributes

</td><td>

Determine where or how the action handles the generated data.**Note:** The only action attribute available when `Input source` is selected in the **Input type** field, is *UserActionID*. For a list of the attributes when the **Input type** is `Input action`, see [.](input-actions-configure.md)

**UserActionID**: A unique value that identifies this action record. It is needed to associate the action with a UI rule.

</td></tr></tbody>
</table>6.  Select **Save**.


## What to do next

Associate the **UserActionID** for this action to a UI rule. For more information, see [Create a mobile UI rule](create-mobile-ui-rule.md).

