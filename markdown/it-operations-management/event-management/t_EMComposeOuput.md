---
title: Configure an event rule to customize alert content
description: You can configure an event rule to customize alert content. You can customize the order of the fields and select which fields display. The fields in the left-hand work area of the Transform and Compose Alert Output section of an event rule are the fields that appear in the generated alert.
locale: en-US
release: zurich
product: Event Management
classification: event-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 7
breadcrumb: [Event rules, Processing Events, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Configure an event rule to customize alert content

You can configure an event rule to customize alert content. You can customize the order of the fields and select which fields display. The fields in the left-hand work area of the **Transform and Compose Alert Output** section of an event rule are the fields that appear in the generated alert.

## Before you begin

Role required: evt\_mgmt\_admin

## About this task

You can customize alert content by adding the required event fields and modifying the text in the fields.

**Note:** When creating regex expression for input, ensure that you create input with the variables in sequential order. While variables can be skipped for inclusion, the selected order must be maintained.

Format alert text by using one or both of these methods:

|Format method|Description|
|-------------|-----------|
|Transform|Create a field to display in an alert. The field and its value appear in the **Additional Information** section or in the **Alert Tags** section. In the **Event Input** pane, the new field is listed in the **Expressions** section.|
|Compose|Determine which text to display in the selected field.|

**Note:**

-   Configure which fields display in the **Event Input** pane by configuring the exclusion list \[em\_event\_rule\_black\_list\].

    A field entered into the exclusion list that already appears in an existing event rule is not removed from the rule; instead, it is moved to the **Manual Attributes** section in the rule.

-   Control the order of event form fields by configuring em\_event\_rule\_order.

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Rules** &gt; **Event Rules**.

2.  Click **New** or open an event rule.

3.  Click **Transform and compose alert output**.

    In this section, you can use the **Transform** mode and the **Compose** mode.

4.  To transform information in fields—standard mode:

    **Note:** In this step, the selection of text is made in standard edit mode. In this mode, undo is available.

    1.  Click the required field in the Event Input pane. The value and contents of the selected field appear in the workarea on the left.

        ![Event Management output](../image/event-rule-workarea.png)

    2.  Select standard edit mode ![Event Management icon](../image/transform-standard-mode.png).
    3.  Using the pencil cursor, highlight the required text. You can double-click text in the field to select a word ![Event Management icon](../image/event-rule-select-text.png) or select the required text and symbols.

        **Note:** If **Accessibility enabled** ![Accessibility enabled](../image/accessibility-enabled.png) is selected in System Settings, standard edit mode is not available ![Standard edit mode icon](../image/standard-edit-mode-icon.png).

    4.  Select a field name from the list or enter the required expression name. Fields that appear in the list are existing event fields, additional info fields or previously defined alert tags \(fields prefixed with "t\_"\). The field name appears in the **Expressions** pane and the selected text is highlighted. Both the text and the expression name are highlighted in the same color. Each additional expression that you create, plus its value, is highlighted in a different color.

        ![Event Management output](../image/event-rule-transform-list.png)

        **Note:** Transform field names cannot contain a ‘ \(single quote\) character.

    5.  Click **Done**. The expression name appears in the **Expressions** section of the **Event Input** pane.

        ![Event Management output](../image/event-rule-expression-section.png)

    6.  If you click an expression or its value in the **Event Input** pane, the details display in the workarea on the left.
5.  To transform information in fields—regex mode:

    **Note:**

    -   In regex mode, undo is not available.
    -   When building a regex expression from variables that are highlighted in the event, place the selected variables in the same order that they appear in the event field.
    -   When composing the event rule regex, specify the terms using an exact match of the input from the event fields. For example, for the text `vhxy2stlgwc_8888_hec03v012979`, the regex

        ```
        ^([^_]+)_
        ```

        looks as if it should catch the text `“vhxy2stlgwc”` that appears before the underscore. However, it does not work as this text is not an exact match. Use the full regex, as follows:

        ```
        ^([^_]+)_.*
        ```

    -   The Java Matcher parser is used for the regex engine. Ensure that you use a Java parser to test the regex.
    -   If the regex does not match the entire string when parsing data, the event rule will not capture the event, and no parsing takes place.
    -   The Java regex engine “matches” method is used. With this implementation, the regex engine attempts to match the entire input sequence against the specified pattern. Other matching methods, for example, the find method, are not supported.
    -   No regex flags are set by default, except the `Pattern.DOTALL` flag. With this implementation of Java regex, the DOT character ‘.’ matches any character, including a line terminator.
    -   Aside from `Pattern.DOTALL`, other regex flags cannot be changed.
    -   `Lookahead` is supported. However, `Lookbehind` is not supported.
    1.  Click the required field in the Event Input pane. The value and contents of the selected field appears in the workarea on the left.
    2.  Select regex edit mode ![Event Management icon](../image/transpose-regex-mode.png).

        ![Event Management output](../image/event-rule-workarea-regex.png)

    3.  Select the required text and symbols ![Event Management graphic](../image/transpose-regex.png). Replace the highlighted text with \(.\*\) to create a regex expression.
    4.  In the **Expressions** pane, click the **Select or Add Field** field.

        ![Event Management image](../image/transform-add-field.png)

    5.  Select a field name from the list or enter the required expression name. Fields that appear in the list are existing event fields, additional info fields or previously defined alert tags \(fields prefixed with "t\_"\). The field name appears in the **Expressions** pane.

        ![Event Management output](../image/event-rule-transform-list.png)

        **Note:** Transform field names cannot contain a ‘ \(single quote\) character.

    6.  Click **Done**.
    **Note:**

    -   When building a regex expression from variables that are highlighted in the event, place the selected variables in the same order that they appear in the event field.
    -   When composing the event rule regex, specify the terms using an exact match of the input from the event fields. For example, for the text vhxy2stlgwc\_8888\_hec03v012979, the regex ^\(\[^\_\]+\)\_ looks as if it should catch the text “vhxy2stlgwc” that appears before the underscore. However, it does not work as this text is not an exact match. Use the full regex, as follows: ^\(\[^\_\]+\)\_.\*
6.  To compose text, in the Transform and compose alert output section, click in the required field.

    ![Event Management output](../image/alert-rule-compose.png)

    Compose text in the alert fields by performing any of these actions:

    -   Drag a field from the Event Info pane into the required field.
    -   Use the Event Info pane as a reference of which fields are available. Write the field name details, using the format $\{&lt;fieldname&gt;\}, where "$" means "use the value". Between the brackets, the name of the event field replaces the &lt;fieldname&gt; variable.
    -   Freely enter text, spaces, or characters. For example, use spaces or underscore symbols \(\_\) to make the text in the alert field readable.
7.  To specify fields that must display in the generated alert, select the **Manual attributes** check box.

    **Note:** These fields, and their values, display in the **Additional Information** section or in the **Alert Tags** section for attributes prefixed with "t\_".

    1.  In the left-hand column, enter a value.

    2.  In the right-hand column, either drag a value from the Add or Expression fields or type in a value.

        When entering a value with attributes prefixed with "t\_", a drop-down list appears with all the previously defined "t\_" attributes.

8.  Click **Save** or **Update**.


## What to do next

You can filter event rules. See [Filter the events that an event rule applies to](t_EMCreateFilter.md).

**Parent Topic:**[Event rules](../concept/create-event-rules.md)

**Related topics**  


[Create or edit an event rule](create-or-edit-event-rule.md)

[Use event input information](../concept/event-input-information.md)

[Alert tags](../concept/alert-tags.md)

[Filter the events that an event rule applies to](t_EMCreateFilter.md)

