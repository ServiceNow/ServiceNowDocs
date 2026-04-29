---
title: Configure inline validation for string fields
description: Configure guidance text to display in string fields with format requirements such as account ID, SSN, or SIN. Use regular expression inline validation to display an error message if the input doesn't meet format requirements.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Forms, Administer, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Configure inline validation for string fields

Configure guidance text to display in string fields with format requirements such as account ID, SSN, or SIN. Use regular expression inline validation to display an error message if the input doesn't meet format requirements.

## Before you begin

Role required: admin

## About this task

Guidance text helps you enter data correctly into string fields with format requirements such as account ID, SSN, or SIN. Inline validation uses a regular expression \(regex\) pattern to enforce format requirements. If the input doesn't match the required format, an error message displays.

The process for configuring string fields with guidance text and inline validation requires two steps:

1.  Create a regex pattern for a required input format.
2.  Map the regex pattern and add guidance text to a string field.

## Procedure

1.  Create a regex pattern for a required input format.

    1.  Navigate to `sys_ui_regex.list`.

        The entire list of regex tables from the Regex Tables \[sys\_ui\_regex\] table opens.

    2.  Select **New**.

        A new Regex Table record opens.

    3.  Complete the following fields:

        -   **Name**

            Create a descriptive name for the regex pattern. For example, if you're creating a regex pattern for an account number, enter `Account Number`.

        -   **Regex pattern**

            Enter the regex pattern that defines the required input format. This field is required. For example, you might use `^\d{10}$` to require a 10-digit number.

    4.  Select **Submit**.

2.  Map the regex pattern and add guidance text to a string field.

    1.  Navigate to `sys_ui_field_regex_mapping.list`.

        The entire list of mapping tables from the Field Regex Mapping Tables \[sys\_ui\_field\_regex\_mapping\] table opens.

    2.  Select **New**.

        A new Field Regex Mapping Table record opens.

    3.  Complete the following fields:

        -   **Table**

            Select the table that contains the string field you want to apply validation and guidance to.

        -   **Field name**

            Select the string field from the list.

        -   **Placeholder Text**

            Enter sample text to display in the field as an example of the required format.

        -   **Field message**

            Enter guidance text that explains the format requirement or gives additional instructions.

        -   **Field message type**

            Select the type of guidance text to indicate whether it's a suggestion, information, warning, positive message, or critical.

        -   **Order**

            Enter a number to set the display priority of the guidance text. Lower numbers appear first.

        -   **Active**

            Select this check box to enable the validation and guidance text.

        -   **Inherited**

            Select this check box to apply the validation and guidance text to child tables with the same field.

    4.  From the Input Validation Rules section, complete the following fields:

        -   **Regex Pattern**

            Select the regex pattern that matches the required format.

        -   **Input Format**

            Use the Input Format Guide to enter an input format.

<table id="table_esy_ggz_m3c"><thead><tr><th>

Symbols

</th><th>

Input Format

</th></tr></thead><tbody><tr><td>

`0`

</td><td>

Accepts any digit \(0-9\)

</td></tr><tr><td>

`a`

</td><td>

Accepts any letter \(A-Z or a-z\)

</td></tr><tr><td>

`*`

</td><td>

Accepts any characters, letters, digits, or symbols.

</td></tr><tr><td>

`[]`

</td><td>

Makes input optional

</td></tr><tr><td>

`{}`

</td><td>

Includes a fixed part in an unmasked value

</td></tr><tr><td>

```

</td><td>

Prevents symbols from shifting back

</td></tr><tr><td>

`\\`

</td><td>

Shows a symbol as-isFor example, `\\0` requires the number zero as 0.

</td></tr></tbody>
</table>            For example, to accept a phone number in the format +91-12345-67890, enter the input format as `{+91-}00000-00000`.

            To accept an ID in the format EMP-1234, enter the input format as `{EMP-}0000`

    5.  Select **Submit**.


