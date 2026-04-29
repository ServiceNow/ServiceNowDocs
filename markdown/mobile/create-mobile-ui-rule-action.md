---
title: Create a mobile UI rule action
description: Create the actions that execute when your mobile UI rule conditions are met.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Mobile UI Rules, Mobile styles, Mobile app components, Building mobile apps, Mobile Platform]
---

# Create a mobile UI rule action

Create the actions that execute when your mobile UI rule conditions are met.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile UI** &gt; **Mobile UI Rules**.

2.  Open the mobile UI rule where you want to add actions.

3.  In the mobile UI rule form, select **New** in the **Mobile UI rule actions** related list.

    **Note:** If you don't see the **New** button, you may be in a difference scope than the UI Rule. Change scopes and reload the form to display the button.

4.  In the mobile UI rule action form, fill in the fields.

<table id="table_xqw_clq_lnb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

UI Rule

</td><td>

The UI rule related to this action. This field automatically populates with the rule that you opened in step 2.

</td></tr><tr><td>

Operation

</td><td>

Select the operation that the action performs See the following table for details on these actions.

</td></tr><tr><td>

Target

</td><td>

The element affected by the action. The actions available to select depend on the parent selected in your mobile UI rule.-   For input form screens, the targets are input form screen inputs
-   For mobile views, targets are elements from the mobile card template JSON.


</td></tr><tr><td>

Order

</td><td>

Order in which the action executes. If there are multiple actions for the same mobile UI rule, the actions execute according to this value. Lower numbered rules execute before higher numbered rules

</td></tr><tr><td>

Value

</td><td>

Defines how the action applies to the element in the **Target** field. This value depends on the selected **Operation**. See the following table for operation descriptions and the values that they use.

</td></tr><tr><td>

Target Mapping

</td><td>

Defines which string input field the generated summary text should be added to when using the **Record Summarization** operation.

</td></tr></tbody>
</table><table id="table_adx_dmq_lnb"><thead><tr><th>

Operation

</th><th>

Definition

</th><th>

Values

</th></tr></thead><tbody><tr><td>

Disable Button

</td><td>

Determines whether the button in the **Target** field is inactive.

</td><td>

Set the **Value** to `true` to disable a button or `false` to enable it.

</td></tr><tr><td>

Set Mandatory

</td><td>

Determines if the element in the **Target** field is required.

</td><td>

Set the **Value** to `true` to make the element mandatory or `false` to make it optional.

</td></tr><tr><td>

Set Read-only

</td><td>

Determines whether the element in the **Target** field is read-only.

</td><td>

Set the **Value** to `true` to make an element read-only, or `false` make the element editable.

</td></tr><tr><td>

Set UI Style

</td><td>

Applies UI styling to an element.**Note:**

This operation doesn’t reverse when using **Reverse If False** on your mobile UI rule.

</td><td>

Use this value to set a background color, font color, and text decorator icon. The value must be in JSON format. This example changes the colors of the background and text:

```
{
"BackgroundColor": "#E1E1E1",
"BackgroundColorVariable": "--now-color-secondary-3"
}

```

 This example sets a text decorator icon.

 ```
{
"TextDecorator":{
        "Type": "Font",
        "FontName": "now-mobile-icons-cards",
        "Value": "IconCode",
        "FontColor": "#1E4335"
    }
}
```

 You can also use color variables to change theming in your mobile UI rules. For details see [Color variable support for UI rules](../reference/color-var-ui-rule.md).

 **Note:**

-   `IconCode` must be replaced with a valid icon code. For a list of icon codes, see [Mobile icons](../reference/sg-mobile-icon.md)
-   Use a JSON validator when copying and pasting JSON code from a topic, to make sure all code is correctly applied.


</td></tr><tr><td>

Set Visibility

</td><td>

Determines the visibility of the element in the **Target** field is read-only.

</td><td>

Set the **Value** to `true` to display the element, or `false` to hide the element.

</td></tr><tr><td>

Simple Arithmetic

</td><td>

**Note:** This operation doesn’t reverse when using **Reverse If False** on your mobile UI rule.

</td><td>

Set the **Value** by creating a mathematical operation using inputs from the input form screen associate with your mobile UI rule. For example, if you wanted to calculate travel costs you could use:```
cost_per_mile*miles_traveled
```

 In this example, the values in the `cost_per_mile` and `miles_traveled` inputs would be multiplied. For this operation to work, the input form screen would need inputs matching these names.

</td></tr><tr><td>

Time ago

</td><td>

Applies a time indicator to a record, for example "Updated 3 minutes ago" or "Created 2 months ago".**Note:** This operation doesn’t reverse when using **Reverse If False** on your mobile UI rule.

</td><td>

The following fields must be set:-   In the **Operation** field, enter `Date Formatter`.
-   In the **Target** field, set the target to a mobile view element that uses a DateTime input.
-   In the **Value** field, enter `timeago`.
Use any of the following option parameters for `timeago`:

`timeago(negative text value, positive text value, verbose flag);`-   **negative text value**

The value displayed for past dates, using `%d` in place of the numerical value.

-   **positive text value**

The value displayed for future dates, using `%d` in place of the numerical value.

-   **verbose flag**

Whether a short or long version of the time format is displayed. This field value is `true` or `false`.

For example, when set to true, '2 minutes ago' is displayed. If set to false, '2 m ago' is displayed.

In this example, you see values such as "Expired 5 hours ago" or "Expires in 5 days" depending on the time value.```
timeago(“Expired %d ago”, “Expires in %d”, true)​;
```

</td></tr><tr><td>

Time and date calculation

</td><td>

Automatically calculates an end time after entering a start time. The end time value can be in the past or the future. For example, you select a meeting to start at 15:00, the default calculation is set to 30 minutes later, so 15:30 displays as the default end time.**Note:** This operation doesn’t reverse when using **Reverse If False** on your mobile UI rule.

</td><td>

The following fields must be set:-   In the **Operation** field, enter `Date Calculation`.
-   In the **Target** field, set the target to an input form screen element that uses a DateTime input.
-   In the **Value** field, enter the input structure using the following syntax &lt;input name&gt; +/- &lt;duration&gt;.

The duration value is formatted in the following way:

    -   `10d` = 10 days
    -   `5h` = 5 hours
    -   `3m` = 3 minutes
    -   `2s` = 12 seconds
For example, an entry of `start_time + 1d8h`sets the value to be calculated at 1 day and 8 hours after the start time.

 **Note:** You can’t use month and year in the time and date calculation.

</td></tr><tr><td>

Record Summarization

</td><td>

Enables record summarization using Now Assist.**Note:** This operation requires Now Assist to be configured. For more information, see [Overview tab in Now Assist Admin](https://www.servicenow.com/docs/access?context=configuring-now-assist&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

</td><td>

In the **Target Mapping** field, enter the string input field that the generated text should be added to.

</td></tr></tbody>
</table>
