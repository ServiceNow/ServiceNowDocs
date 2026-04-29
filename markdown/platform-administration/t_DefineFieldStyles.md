---
title: Define field styles
description: Field styles enable you to declare individual CSS styles for a field in a list or form.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Customize, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Define field styles

Field styles enable you to declare individual CSS styles for a field in a list or form.

## Before you begin

Role required: personalize\_styles or admin

## About this task

The CSS lets you change the following attributes of a field.

-   Change the color.
-   Change the font attributes \(bold, italics, underline\).
-   Change the padding and alignment of text.

You can define field styles for tables and database views that are in the same scope as the field style and for other tables that have at least one field in the same scope as the field style. Field styles defined for a table don’t apply to database views that include the table. Create separate field styles for database views.

**Note:** Field styles aren’t applied to comments and work notes fields used with the activity formatter. Background color for these fields can be set using the **glide.ui.activity\_stream.style.comments** and **glide.ui.activity\_stream.style.work\_notes** system properties located in the sys\_properties table.

## Procedure

1.  Navigate to the list of styles for the field in one of the following ways.

    -   Right-click the field label on the form and select **Configure Styles**.
    -   Navigate to **System UI** &gt; **Field Styles**, and locate the field to apply a style \(admin only\).
2.  Select **New**, or select the style to modify.

3.  Complete the form.

<table id="table_jzt_1mz_qp"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table

</td><td>

Table that contains the field. **Note:** The list shows only tables and database views that meet the scope protections for field styles.

</td></tr><tr><td>

Field name

</td><td>

The field to which the style applies.

</td></tr><tr><td>

Value

</td><td>

The exact value or script-based-condition required to apply the style.**Note:** The value only affects list field styles when the field isn’t read-only. The value affects both list and forms if the field is read-only.

To apply field styles to forms only, leave the value field empty.

</td></tr><tr><td>

Style

</td><td>

The CSS style to apply.For example, to make the background of the Incident Category fields red in record lists, with a 24-px font size and white text color, enter the following code.

```
background-color:red;
font-size:24px;
color:white;
```

</td></tr></tbody>
</table>    You can use a script-based-condition with the syntax `javascript:<script>` in the **Value** field to determine whether the system should apply a style to a field in the list. If the evaluated script returns true, the system applies the style to the list item.

    The script has access to the **current** script object, which enables you to build conditions based on the field values of the current record. For example, this script checks for overdue items based on a field value:

    ```
     javascript:gs.dateDiff(gs.now(), current.u_datefield.getDisplayValue(), true) < 0
    ```

    **Note:** In this example, `current.u_datefield` refers to the name of a custom date field.

    The system only supports one `javascript:<script>` entry in a **Value** field. If you want to enter multiple JavaScript conditions, consolidate the conditions into one statement. For example, instead of this invalid entry:

    ```
    javascript: current.state == "Completed" javascript: current.error_tables > 0
    ```

    Consolidate the conditions into one statement such as:

    ```
    javascript: current.state == "Completed" && current.error_tables > 0
    ```

4.  To add alternative text for a style, [configure the form](../../form-administration/concept/configure-form-layout.md#) to add the alternative text field.

    For styles like the VIP style icon, you can add alternative text so that screen readers can differentiate between the style and the text.

5.  Select **Submit** or **Update**.


**Parent Topic:**[Customizing fields on the ServiceNow AI Platform](../../field-administration/concept/customize-fields-now-platform-landing.md)

