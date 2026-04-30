---
title: Use event input information
description: The Event Input pane that is included in the steps to create an event rule provides a reference to the information that you can use when configuring an event rule.
locale: en-US
release: xanadu
product: Event Management
classification: event-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Event rules, Processing Events, Configuring Event Management, Event Management, ITOM Health, IT Operations Management]
---

# Use event input information

The **Event Input** pane that is included in the steps to create an event rule provides a reference to the information that you can use when configuring an event rule.

In the **Transform and compose alert output** pane, you can also drag the information into the required fields to customize alert content. The fields in the right-hand pane appear as a reference to which fields, expressions, and their values are available when working in the Event Rule designer. The fields that display in the Transform and compose alert output left-hand workarea become the fields in the generated alert form. In addition, you can define alert tags that are specific for customization.

## General components and navigation

The Event Input pane consists of these sections:

-   Event Additional Info
-   Expressions
-   Event Raw Info

The Event Input pane displays in all Event Rule designer sections, except for the Event Rule Info section. The fields in the right-pane can be modified only in the Transform and compose alert output section. In all the other sections, the Event Input pane is read-only and available for reference purposes.

**Note:** If **Accessibility enabled** ![Accessibility enabled](../image/accessibility-enabled.png) is selected in System Settings, standard edit mode is not available ![Standard edit mode icon](../image/standard-edit-mode-icon.png).

## Edit modes

<table id="table_d5z_gym_xy"><thead><tr><th>

Mode

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Standard edit mode ![Event Management icon](../image/transform-standard-mode.png)

</td><td>

Text selected in the left-hand workarea cannot be edited. Undo is not available. In this mode, you can only mark the text or values and transform it by selecting a field name.

</td></tr><tr><td>

Regex edit mode![Event Management icon](../image/transpose-regex-mode.png)

</td><td>

Edit text in the left-hand workarea by selecting it, as required. After you have edited the text, you cannot go back to the standard mode. **Undo** is not available. However, **Reset** is available, returning the field to its original value. You can compose text using regular expression \(regex\) format conventions, for example, type \(.\*\) to create a field name. You cannot use field values like: type "$" to include the value of a field and specify the name of the field in parentheses \{\}. You can include special characters in a field by "escaping" them, that is, by prefixing the character with a "\\". For example, to include a "\\" in your text, enter "\\\\".

</td></tr></tbody>
</table>## Event additional info

The Event additional info section displays default event form fields, plus fields that were created to display in alerts and that are added to the **Additional information** section of the alert.

When configuring text in the fields in the left-hand workarea, you can drag field names and/or their value from this section into the fields.

## Expressions

The Expressions section is available only if an additional information field was created. You can create expressions from event raw data or from additional information data.

1.  Click in a field in the **Event Input** pane to perform transformation actions.
2.  Create an expression by transforming information and associating it with a field name. Either select a field name from the suggested list, or create a field name, as required.

    ![Event Management rule expression](../image/event-rule-expression.png)

3.  Click in a field in the **Event Input** pane. In the left-hand workarea, select the required information.

Create expressions by transforming information and associating it with a field name. Select a field name from the suggested list, or you can create a field name, as required.

## Event raw info

The Event raw info section is always available. Its contents are the fields from the Event form.

To transform text, click a field in the right-panel to open it in the work area on the left-panel, in the Mark Expressions section. You can select text in the **Mark Expressions** section where the selected text becomes the value of a newly created field. Name the new field. This new field is added to the Expressions section.

**Note:** When creating regex expression for input, ensure that you create input with the variables in sequential order. While variables can be skipped for inclusion, the selected order must be maintained.

Controlling how fields appear:

-   Use the exclusion list \[em\_event\_rule\_black\_list\] table to hide fields from the right-pane.
-   Use the em\_event\_rule\_order form to order the position of each field.
-   Fields that are not in the exclusion list and also not part of the em\_event\_rule\_order table, still appear in the event rule designer, in the right-panel and in the **Transform and Compose Alert Output** tab.

**Parent Topic:**[Event rules](create-event-rules.md)

**Related topics**  


[Create or edit an event rule](../task/create-or-edit-event-rule.md)

[Configure an event rule to customize alert content](../task/t_EMComposeOuput.md)

[Filter the events that an event rule applies to](../task/t_EMCreateFilter.md)

[Set a threshold to suppress alert generation](../task/t_EMISetThresholdEvent.md)

