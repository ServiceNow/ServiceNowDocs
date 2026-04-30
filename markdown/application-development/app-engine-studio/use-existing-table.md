---
title: Create a blank table
description: Add a data table to your application from an existing table that you or someone else previously created or from scratch.
locale: en-US
release: zurich
product: App Engine Studio
classification: app-engine-studio
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Create a data model, Enhance your app, Build, App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Create a blank table

Add a data table to your application from an existing table that you or someone else previously created or from scratch.

## Before you begin

Role required: sn\_app\_eng\_studio.user, sn\_app\_eng\_studio.admin, or delegated developer for AES. For more information about granular admin roles, see [Granular admin roles required to secure your instance](https://www.servicenow.com/docs/access?context=roles-within-platform-security&version=zurich&pubname=zurich-platform-security&ft:locale=en-US). For more information about delegated development, see [Delegate developers using AES](../concept/aes-app-dev-workflow.md).

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **App Engine Studio**.

2.  From the My Apps page, open your application.

3.  Next to the Data heading, select the Add icon \(![Add icon](../image/plus-icon.png)\).

4.  Select **Create a blank table**, and then select **Continue**.

5.  Choose from the following choices.

<table id="choicetable_qfr_n3p_tvb"><tbody><tr><td id="d136495e123">

**Create new table**

</td><td>

Select this option to create a blank table from scratch.1.  Choose **Create new table**.
2.  Click **Continue**.


</td></tr><tr><td id="d136495e147">

**Create from an extensible table**

</td><td>

Select this option to create a new blank table from an existing extensible table in the ServiceNow AI Platform.1.  Choose **Create from an extensible table**.
2.  Search for and select an existing table.

**Note:** Tables already in the app display first in the list and recommended ServiceNow AI Platform tables display next, along with a short description of the type of information the table stores.

3.  Select **Continue**.


</td></tr></tbody>
</table>6.  On the form, fill in the properties of your new table.

<table id="table_wzh_3sc_zmb"><thead><tr><th>

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
</table>7.  Select **Continue**.

8.  Control who has access to create, read, write, and delete content from this table by adding new roles and/or defining the desired Create, Read, Write, Delete permissions for existing roles.

    Roles that you create in the table persist throughout the application and can be further defined in other tables you add. See [Add application security](../concept/add-security.md) for more information on how security permissions work.

    **Note:** At least one role must have read access for you to be able to preview the table.

9.  Select **Continue** to add the new table.

10. Return to your application home page or continue editing your table.

    -   Select **Done** to return to your application home page.
    -   Select **Edit table** to review the columns that were added to your table and continue editing it in Table Builder.
11. If you continue editing, in the new tab that opens, review the table columns.

    Each table column appears as a row in Table Builder.

    A lock icon \(![Lock icon](../image/lock-icon.png)\) appears next to columns from the extended table. You can't modify these columns.

12. Customize your table by adding table columns.

    1.  In Table Builder, select **+ Add new field**.

    2.  On the empty row, fill in the fields.

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
</table>13. Select **Save**.


## What to do next

For more information on Table Builder, see [Table Builder](../../../administer/form-builder/concept/tb-landing-page.md).

**Parent Topic:**[Create a data model for your application](../concept/add-data.md)

