---
title: Create new table from spreadsheet import
description: Create new tables directly from a Microsoft Excel spreadsheet import.
locale: en-US
release: zurich
product: App Engine Studio
classification: app-engine-studio
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Use a spreadsheet, Create a data model, Enhance your app, Build, App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Create new table from spreadsheet import

Create new tables directly from a Microsoft Excel spreadsheet import.

## Before you begin

-   Import a spreadsheet into App Engine Studio. See [Import a spreadsheet](spreadsheet-importing-spreadsheet.md).

Role required: admin, sn\_app\_eng\_studio.user, sn\_app\_eng\_studio.admin, or delegated developer permissions. For more information, see [Delegate developers using AES](../concept/aes-app-dev-workflow.md).

## Procedure

1.  After you have uploaded your spreadsheet as described in [Import a spreadsheet](spreadsheet-importing-spreadsheet.md), choose what you want to do with the imported data in the displayed wizard.

    ![Create new table from spreadsheet.](../image/aes-spreadsheet-import-data.png "Create new table from spreadsheet")

    1.  Select **A new table**.

    2.  Choose **Create new table**.

2.  Select **Continue**.

3.  Review the properties for each column header, using the **Expand options** drop-down to display more properties.

<table id="table_nnz_2mq_5mb"><thead><tr><th>

Column header property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Field Label

</td><td>

Unique label for the column.

</td></tr><tr><td>

Field name

</td><td>

Database name for the column.

</td></tr><tr><td>

Type

</td><td>

Type of information that the column contains. For example, to contain plain text in the column, select **String**.

 Depending on the type that you select, fill in the additional fields to further define the table column. For example, if you select **String**, define the character limit of the string input. Or, if you select **Choice**, define the choices that users can choose from.

 See [Field types reference](https://www.servicenow.com/docs/access?context=r_FieldTypes&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

</td></tr><tr><td>

Character limit

</td><td>

Max length of the strings that can be stored.

</td></tr><tr><td>

Display

</td><td>

Option to set the column as the display value for the table. A reference field shows the display value of the table to which it is referring. For example, the **Opened by** column of the task table refers to the user table. Because the display value of the user table is the user name, the **Opened by** field shows something like **Beth Anglin** or **Joe Employee**. When you select a display value, choose the table column that would act as an appropriate title for individual records.

 Only one column can act as the display value for a table.

</td></tr><tr><td>

Mandatory

</td><td>

Option to require that the column must contain a value before a new record can be saved.

</td></tr></tbody>
</table>    To add another column to your table, select **Add new field**.

    To delete a column, select the trash icon \(![Trash icon](../image/blue-trash-icon.png)\).

4.  Select **Continue** to define table properties.

5.  On the form, fill in the fields.

<table id="table_ac1_z5q_5mb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table label

</td><td>

Unique label to identify the table.

</td></tr><tr><td>

Table name

</td><td>

Database name for the table. A table name is created automatically after you enter a table label. You can edit the name if needed.

</td></tr><tr><td>

Make extensible

</td><td>

Option to allow other tables to share data from this table. For more information on table extension, see [Table extension](../concept/add-data.md#section_ebj_sdb_d5b).

</td></tr><tr><td>

Auto number

</td><td>

Option to track table records with a unique number. If you select this option, define the **Prefix**, **Starting number**, and **Number of digits**.

</td></tr><tr><td>

Prefix

</td><td>

Abbreviated name of the table to append to the beginning of the record number. For example, if you are creating a "Laptop" table, then your prefix may be "LPTP" or "LT."

</td></tr><tr><td>

Starting number

</td><td>

Number to identify the first record created for your table.

</td></tr><tr><td>

Number of digits

</td><td>

Maximum number of digits to allow in the record number. This value determines the highest possible record number. For example, if you enter `7`, then the highest possible number is 9999999.

</td></tr></tbody>
</table>6.  Select **Continue**.

7.  Control who has access to create, read, write, and delete content from this table by adding new roles and/or defining the desired Create, Read, Write, Delete permissions for existing roles.

    Roles that you create in the table persist throughout the application and can be further defined in other tables you add. See [Add application security](../concept/add-security.md) for more information on how security permissions work.

    **Note:** At least one role must have read access for you to be able to preview the table.

8.  Select **Continue** to add the new table created from your spreadsheet to your app.

9.  Convert any remaining worksheets if your file contained multiple worksheet tabs.

    -   **Note:** For each sheet that you want to convert, you will need to select **Convert to table**, and then repeat steps in this procedure or choose a different pathway for the additional worksheet \(see [Create new table from extensible table and spreadsheet import](spreadsheet-create-new-ext-table.md) or [Modify existing table using spreadsheet import](spreadsheet-import-existing-table.md) for steps\).

    -   If you do not have multiple worksheets, proceed to the next step.
10. Select **Done** on the summary screen.

    Alternatively, to view your table in Table Builder, you can select **Edit table\(s\)** on the summary screen.


## What to do next

For more information on editing your data tables in Table Builder, see [Table Builder](../../../administer/form-builder/concept/tb-landing-page.md).

**Parent Topic:**[Use a spreadsheet to add data](upload-multi-sheets.md)

