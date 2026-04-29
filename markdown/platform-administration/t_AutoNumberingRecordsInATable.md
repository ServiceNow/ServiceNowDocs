---
title: Add auto-numbering records in a table
description: You can define one number format per table in the system.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Record numbering, Customize, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Add auto-numbering records in a table

You can define one number format per table in the system.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Number Maintenance**.

2.  Select a table name to view the number record for that table, or click **New**.

3.  Define the number format by completing the fields \(see table\).

4.  Select **Submit** or **Update**.

    If an auto-numbered field does not already exist, a new field is automatically created on the table with the following values:

    -   Label: Number
    -   Name: u\_number
    -   Default value:

        ```
        javascript:getNextObjNumberPadded();
        ```

        **Note:** This script renumbers records when the **Number of digits** is updated. To use a script that does not renumber records when the **Number of digits** is updated, open the dictionary entry for the **Number** field and enter the following script in the **Default value** field.

        ```
        javascript:getNextObjNumber();
        ```

<table id="table_m1c_qbf_tp"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table

</td><td>

Select a table.

</td></tr><tr><td>

Prefix

</td><td>

Enter a prefix for every number in the table \(for example, **INC** for Incident\).

</td></tr><tr><td>

Number

</td><td>

Enter the base number for this table \(default value is 1000\). Record numbers are automatically incremented, and the next number is maintained in the Counter \[sys\_number\_counter\] table.If you set the base number to a value higher than the current counter, the next record number uses the new base number. Otherwise the next record number uses the current counter. The counter does not reset to a base number lower than itself. To see the current counter, click the **Show Counter** related link.

</td></tr><tr><td>

Number of digits

</td><td>

Enter the minimum number of digits to use after the prefix \(default value is 7\).-   Leading zeros are added to auto-numbers, if necessary. For example, **INC0001001** contains three leading zeros.
-   The number of digits can exceed the minimum length. For example, if **Number of digits** is **2** and more than 99 records are created on the table, the numbers continue past 100 \(such as **INC101**\).
 **Warning:** Changing this field may update all number values for existing records on a table. Take care when changing this field on a production instance.

</td></tr></tbody>
</table>    When moving some applications these records may not be automatically included. Take care to ensure that all necessary records are present when moving applications.

    **Note:** To change the default values for new number formats, change the **Default value** field on the system dictionary record for the **Number** or **Number of digits** field. These fields are on the Number table.


**Parent Topic:**[Record numbering](../concept/c_ManagingRecordNumbering.md)

**Related topics**  


[System dictionary](../../data-dictionary-tables/concept/c_SystemDictionary.md)

