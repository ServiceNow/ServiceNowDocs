---
title: Table properties in Table Builder
description: Various table and table column properties can be modified by using Table Builder.
locale: en-US
release: zurich
product: Form Builder
classification: form-builder
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Table Builder reference, Table Builder, Builder library, Developing your application, Building applications]
---

# Table properties in Table Builder

Various table and table column properties can be modified by using Table Builder.

## Table column properties

The following table shows descriptions of the properties that you can modify for the columns in a data table.

<table id="table_add-column"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Column label

</td><td>

Unique label for the column.

</td></tr><tr><td>

Column name

</td><td>

Database name for the column.

</td></tr><tr><td>

Type

</td><td id="entry_fieldtype">

Type of information that the column contains. For example, to contain plain text in the column, select **String**.

 Depending on the type that you select, fill in the additional fields to further define the table column. For example, if you select **String**, define the character limit of the string input. Or, if you select **Choice**, define the choices that users can choose from.

 See [Field types](https://www.servicenow.com/docs/access?context=r_FieldTypes&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

</td></tr><tr><td>

Reference

</td><td>

Table that is associated with the column. This field applies only if the column type is **Reference**.

</td></tr><tr><td>

Max length

</td><td>

Maximum number of characters that users can enter in the field.

</td></tr><tr><td>

Default value

</td><td id="entry_defaultvalue">

Value that populates the field automatically after a new record is created.

</td></tr><tr><td>

Display

</td><td>

Option to set the column as the display value for the table. A reference field shows the display value of the table to which it is referring. For example, the **Opened by** column of the task table refers to the user table. Because the display value of the user table is the user name, the **Opened by** field shows something like **Beth Anglin** or **Joe Employee**. When you select a display value, choose the table column that would act as an appropriate title for individual records.

 Only one column can act as the display value for a table.

</td></tr></tbody>
</table>## Table properties

The following table shows the descriptions of the properties that you can modify for a selected data table.

<table id="table_gqy_5gt_ssb"><thead><tr><th>

Option

</th><th>

Procedure

</th></tr></thead><tbody><tr><td>

Change the table label

</td><td>

In the General information tab, update the **Table label** field.

</td></tr><tr><td>

Make the table extensible

</td><td>

1.  In the General information tab, select **Advanced**.
2.  Select the **Make extensible** check box.

</td></tr><tr><td>

Add record numbers

</td><td>

1.  In the General information tab, select **Advanced**.
2.  Select the **Add record number** check box.
3.  Define the record numbers by updating the **Prefix**, **Starting number**, and **Number of digits** fields.

</td></tr><tr><td>

Accessible from

</td><td>

1.  Open the **Access** tab.
2.  In the **Accessible From** field, select **All Application Scopes** or **This Application Scope Only**.

</td></tr><tr><td>

Application access controls

</td><td>

1.  Open the **Access** tab.
2.  In the **Application Access Controls** field, select Read, Create, Update, and/or Delete selection boxes to specify the desired level of access for the table.

</td></tr></tbody>
</table>**Parent Topic:**[Table Builder reference](../concept/fb-reference.md)

