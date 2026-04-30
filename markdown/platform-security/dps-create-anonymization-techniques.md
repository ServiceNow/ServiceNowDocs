---
title: Create anonymization techniques
description: Create a data privacy technique configuration to customize how data privacy anonymizes your data.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Data anonymization, Platform Privacy]
---

# Create anonymization techniques

Create a data privacy technique configuration to customize how data privacy anonymizes your data.

## Before you begin

Role required: data\_privacy\_admin and admin

## Procedure

1.  Elevate to the **data\_privacy\_admin** role.

    For details on role elevation, see [Elevate to a privileged role](../../security/task/t_ElevateToAPrivilegedRole.md).

2.  Navigate to **System Security** &gt; **Data Privacy** &gt; **Anonymization**.

3.  Select **View techniques**.

    There are several pre-defined techniques available for selection.

<table><thead><tr><th>

Technique

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Selective Replace

</td><td>

This technique does a selective replace of String data. All characters between the input's start and end indices are replaced with the character you choose. You can specify characters to exclude from masking:-   start\_index: Technique masks data starting at the specified character. If left blank, masking begins with the first character.
-   end\_index: Technique masks data from the start of the string to the specified character. If left blank, masking ends with the last character.
-   exclude\_char: Define a character to exclude from masking.
-   replacement\_char: Define a character used for masking. If none is provided, asterisks\(\*\) are used by default.


</td></tr><tr><td>

Static Replace

</td><td>

This technique swaps values with static values. String, Number, and Date data can use this technique:-   date\_time\_value: Replace Date values with this date. Use the yyyy-MM-dd HH:mm:ss format.
-   date\_value: Replace Date values with this date. Use the yyyy-MM-dd format.
-   number\_value: Replace Number values with this number.
-   string\_value: Replace String values with this text.
-   number\_type: Accepts an integer number


</td></tr><tr><td>

Random Replace

</td><td>

This technique swaps values with randomly generated values. String and Number data can use this technique.

</td></tr><tr><td>

Remove

</td><td>

This technique removes values, replacing them with empty \(null\) values.

</td></tr><tr><td>

No Action

</td><td>

This technique is a placeholder. It does not modify fields when selected.

</td></tr><tr><td>

Selective Replace with X

</td><td>

Transforms String data and selectively replaces sensitive characters with the letter X.**Note:** Default technique for data patterns in [Exploring Data Discovery](../../security/concept/data-discovery.md).

</td></tr><tr><td>

Data pattern anonymization

</td><td>

Only anonymizes discovered data patterns within unstructured data fields while keeping underlying context intact. **Note:** Settings for this technique reference data pattern anonymization technique settings in [Exploring Data Discovery](../../security/concept/data-discovery.md).

</td></tr></tbody>
</table>4.  Select **Add custom technique**, if not using a pre-defined technique.

5.  Fill in the fields in the **Customize technique** form.

    |Field1|Description|
    |------|-----------|
    |Base technique|Select a pre-defined technique, as custom techniques are based on the pre-defined techniques.|
    |Technique name|Enter a name for the technique.|
    |Technique description|Enter a description for the technique.|

6.  Select **Next**.

7.  Enter the technique parameters.

    The available parameterized values depend on which privacy technique you have selected. There are no parameterized values for the **No Action** and **Remove** techniques.

    |Base Technique|Privacy Technique Parameter value|Description|Default value|
    |--------------|---------------------------------|-----------|-------------|
    | | | | |
    |Selective Replace|end\_index|Technique masks data from the start of the string to the specified character. If left empty, masking ends with the last character.|\(Empty\)|
    |Selective Replace|exclude\_char|Character to skip masking. Only a single character can be used in this value. If more than one is entered, the first character is used.|\(Empty\)|
    |Selective Replace|replacement\_char|Character to use when replacing values using a selective replace.|An asterisk \(**\***\) is used if no other value is entered.|
    |Selective Replace|start\_index|Technique masks data starting at the specified character.|If left blank, masking starts at the first character.|
    |Static Replace|date\_time\_value|Replace date and time values with this date. Use the yyyy-MM-dd HH:mm:ss format.|1988-11-11 10:10:10|
    |Static Replace|date\_value|Replace date values with this date. Use the yyyy-MM-dd format.|1988-11-11|
    |Static Replace|number\_value|Replace Number values with this number.|1234567|
    |Static Replace|string\_value|Replace String values with this text.|TEXT123|
    |Random Replace|preserve\_data\_length|Set to **true** to preserve data length. De-identified data will have the same length as the original data.|True|

8.  Select **Create Custom Technique**.

    Your custom technique is added to the Anonymization techniques.


## What to do next

See [Create anonymization policies](dps-create-anonymization-policies.md) to configure an anonymization policy to specify which techniques are used when anonymizing your data.

