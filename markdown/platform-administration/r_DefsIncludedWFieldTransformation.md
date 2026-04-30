---
title: Default Transform Definitions
description: The system offers default transform definitions for fields containing text, text numeric, and numeric values.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Field normalization and transformation, Administering fields, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Default Transform Definitions

The system offers default transform definitions for fields containing text, text numeric, and numeric values.

<table id="table_y13_51d_dr"><thead><tr><th>

Transform Type

</th><th>

Category

</th><th>

Description

</th><th>

Parameters

</th></tr></thead><tbody><tr><td>

Change case

</td><td>

Text

</td><td>

Changes the case of the characters in the field value.

</td><td>

**Mode**: Select one of the following modes: -   **Upper**: Converts the value to all upper case characters
-   **Lower**: Converts the value to all lower case characters
-   **Proper**: Converts the value to title case, with the first character in each string in upper case, and the remaining characters of the string in lower case.
-   **Formal**: Converts the value to a string in which only the first letter of the first word is in upper case.

</td></tr><tr><td>

Constant

</td><td>

Text Numeric

</td><td>

Converts the value in this field to a constant.

</td><td>

**Constant**: The constant with which to replace the value in this field.

</td></tr><tr><td>

Delete

</td><td>

Text

</td><td>

Delete a specified sequence of characters from a field value.

</td><td>

-   **Starting position**: Specifies the first character in a sequence of characters to delete from a string. See the discussion of position modes at the beginning of this section for details.
-   **Ending position**: Specifies the final character in a sequence of characters to delete from a string. See the discussion of position modes at the beginning of this section for details.

</td></tr><tr><td>

Insert

</td><td>

Text

</td><td>

Insert a fixed character sequence into a field value.

</td><td>

-   **Position**: The character position at which to insert the new value. See the discussion of position modes at the beginning of this section for details.
-   **Insert**: The value to insert into this field.

</td></tr><tr><td>

Left

</td><td>

Text

</td><td>

Deletes or keeps a specified number of characters from the left side of this field value.

</td><td>

-   **Position**: Specifies the number of characters to keep or delete from the left side of the value. See the discussion of position modes at the beginning of this section for details.
-   **Mode**: Select the mode for this transform: **Keep** or **Delete**.

</td></tr><tr><td>

Prefix

</td><td>

Text

</td><td>

Adds characters to the beginning of a field value.

</td><td>

**Prefix**: Defines the characters to add to the beginning of the transformed field value.

</td></tr><tr><td>

Replace

</td><td>

Text

</td><td>

Replaces occurrences of one string with another string. The special characters backslash \(\\\) and dollar sign \($\) in the replacement string can cause the transform to be different than if the replacement string were being treated as a literal replacement string. Use a regular expression to replace a string or parts of a string.

</td><td>

-   **Find**: Enter the string or regular expression to replace.
-   **Replace with**: Enter the replacement string.

</td></tr><tr><td>

Right

</td><td>

Text

</td><td>

Retains or deletes a specified number of characters from the right side of a field value.

</td><td>

-   **Position**: The number of characters to delete or keep from the right side of this transformed field. See the discussion of position modes at the beginning of this section for details.
-   **Mode**: Select the mode for this transform: **Keep** or **Delete**.

</td></tr><tr><td>

Round

</td><td>

Numeric

</td><td>

Rounds integers to a configured rounding interval using specific criteria. The interval must be appropriate to the value being transformed, such as an interval of 12 for a value expressed in dozens or 0.01 for decimal values expressed in hundredths.

</td><td>

-   **Interval**: Select the rounding interval that is appropriate to the units of the field value. For example. an interval of 256 is appropriate for expressing RAM values in megabytes, but does not work for Disk space expressed in gigabytes. The rounding interval for the examples below is 1
-   **Mode**: Criteria for applying the rounding interval.
    -   **Half up**: Always round up a value that is exactly half way between two intervals. For example, 3.5 is always rounded up to 4, and -3.5 is always rounded up to -3.
    -   **Half down**: Always round down a value that is exactly half way between two intervals. For example, 3.5 is always rounded down to 3, and -3.5 is always rounded down to -4.
    -   **Half away from zero**: Always round an integer that is half way between the specified interval away from zero. For example, 3.5 is always rounded to 4, and -3.5 is always rounded to -4.
    -   **Half toward zero**: Always round an integer that is half way between the specified interval toward zero. For example, 3.5 is always rounded to 3, and -3.5 is always rounded to -3.
    -   **Half to even**: Always round an integer that is half way between the specified interval to the nearest interval whose least significant digit is even. For example, 3.5 is always rounded to 4, and 4.5 is always rounded to 4.
    -   **Half to odd**: Always round an integer that is half way between the specified interval to the nearest interval whose least significant digit is odd. For example, 3.5 is always rounded to 3, and 4.5 is always rounded to 5.
    -   **Up**: Always round an integer up by the specified rounding interval. For example, 3.4 is always rounded to 4 by a rounding interval of 1.0.
    -   **Down**: Always round an integer down by the specified rounding interval. For example, 4.6 is always rounded to 4 by a rounding interval of 1.0.
    -   **Away from zero**: Always round an integer away from zero by the specified rounding interval. For example, 3.3 is always rounded to 4, and -3.3 is always rounded to -4 by a rounding interval of 1.0.
    -   **Toward zero**: Always round an integer toward zero by the specified rounding interval. For example, 3.3 is always rounded to 3, and -3.3 is always rounded to -3 by a rounding interval of 1.0.

</td></tr><tr><td>

Substring

</td><td>

Text

</td><td>

Keep or delete characters from a specified sub-sequence of characters in the field value.

</td><td>

-   **Starting position**: Specifies the first character in a sub-sequence of characters within the value. See the discussion of position modes at the beginning of this section for details.
-   **Ending position**: Specifies the final character in a sub-sequence of characters within the value. See the discussion of position modes at the beginning of this section for details.
-   **Mode**: Select whether to **Delete** the sub-sequence selected or **Keep** only those characters defined.

</td></tr><tr><td>

Suffix

</td><td>

Text

</td><td>

Appends characters to the end of a field value.

</td><td>

**Suffix**: Defines the suffix to add to the end of the field value.

</td></tr><tr><td>

Trim

</td><td>

Text Numeric

</td><td>

Removes blank spaces from the field value.

</td><td>

No parameters

</td></tr></tbody>
</table>