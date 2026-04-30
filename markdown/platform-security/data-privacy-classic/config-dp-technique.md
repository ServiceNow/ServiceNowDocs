---
title: Create a data privacy technique configuration
description: Create a data privacy technique configuration to customize how data privacy anonymizes your data.
locale: en-US
release: xanadu
product: Data Privacy \(Classic\)
classification: data-privacy-classic
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Data privacy \(Classic\) configuration, Data privacy \(Classic\), Data Privacy, Platform Privacy]
---

# Create a data privacy technique configuration

Create a data privacy technique configuration to customize how data privacy anonymizes your data.

## Before you begin

Role required: data\_privacy\_admin and admin

## Procedure

1.  Elevate to the **data\_privacy\_admin** role.

    For details on role elevation, see [Elevate to a privileged role](t_ElevateToAPrivilegedRole.md).

2.  Navigate to **System Security** &gt; **Data Privacy** &gt; **Privacy Technique Configuration**.

3.  Click **New**.

4.  In the **Name** field, enter a name for your privacy technique configuration.

5.  In the **Privacy Technique** field, select a privacy technique.

<table id="table_n4l_xfv_hrb"><thead><tr><th>

Technique

</th><th>

Description

</th></tr></thead><tbody><tr><td>

No Action

</td><td>

This technique is a placeholder. It does not modify fields when selected.

</td></tr><tr><td>

Random Replace

</td><td>

This technique swaps values with randomly generated values. String and Number data can use this technique.

</td></tr><tr><td>

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


</td></tr><tr><td>

Remove

</td><td>

This technique removes values, replacing them with empty \(null\) values.

</td></tr></tbody>
</table>    **Note:** Previously supported value **Replace** is deprecated and renamed **Replace-Deprecated** and should not be used.

6.  Right-click the header and click **Save** in the context menu.

    After the record is saved, the **Privacy Parameterized Values** list appears.

7.  Use the records in the **Privacy Parameterized Values** list to customize your data privacy technique configuration.

    The available parameterized values depend on which privacy technique you have selected. There are no parameterized values for the **No Action** and **Remove** techniques.

    |Privacy Technique Parameter value|Description|Default value|
    |---------------------------------|-----------|-------------|
    |char\_to\_replace|Character to use when replacing values using a selective replace.|\*|
    |end\_index|Technique masks data from the start of the string to the specified character. If left empty, masking ends with the last character.|\(Empty\)|
    |exclude\_char|Character to skip masking. Only a single character can be used in this value. If more than one is entered, the first character is used.|\(Empty\)|
    |start\_index|Technique masks data starting at the specified character.|1|

    |Privacy Technique Parameter value|Description|Default value|
    |---------------------------------|-----------|-------------|
    |date\_time\_value|Replace date and time values with this date. Use the yyyy-MM-dd HH:mm:ss format.|1988-11-11 10:10:10|
    |date\_value|Replace date values with this date. Use the yyyy-MM-dd format.|1988-11-11|
    |number\_value|Replace Number values with this number.|1234567|
    |preserve\_data\_length|Set to **true** to preserve data length. De-identified data will have the same length as the original data.|true|
    |string\_value|Replace String values with this text.|TEXT123|
    |use\_random\_generated\_value|Set to **true** to replace data with randomly generated values. Only String and Number data can be replaced with random values. This option overrides static values.|false|

8.  Click **Save**.


