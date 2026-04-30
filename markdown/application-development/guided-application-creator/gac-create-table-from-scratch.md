---
title: Create a table in Guided Application Creator
description: Create a table in Guided Application Creator to customize your application to fit your business needs.
locale: en-US
release: yokohama
product: Guided Application Creator
classification: guided-application-creator
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Designate data tables in Guided Application Creator, Setting up an application in Guided Application Creator, Guided Application Creator, Building pro-code applications, Developing your application, Building applications]
---

# Create a table in Guided Application Creator

Create a table in Guided Application Creator to customize your application to fit your business needs.

## Before you begin

Complete:

1.  [Create an application record in Guided Application Creator](gac-create-app-record.md)
2.  [Define roles in Guided Application Creator](gac-create-roles.md)
3.  [Select user experiences in Guided Application Creator](gac-select-ux.md)
4.  [Designate data tables in Guided Application Creator](gac-designate-data-table.md)

Role required: sn\_g\_app\_creator.app\_creator or admin

## Procedure

1.  To select a table creation method, on the screen, select **Create table from scratch** and then select **Continue**.

    ![Table creation options](../image/GAC-data-tables.png)

2.  Add fields to your custom table.

    1.  Select **+ Add a new field**.

    2.  On the form, fill in the fields.

<table id="table_dd3_stw_5hb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Field Label

</td><td>

Unique label for the field.

</td></tr><tr><td>

Field Name

</td><td>

Name of the field in the database.

</td></tr><tr><td>

Field Type

</td><td>

Type of field. For more information on the different field types, see [Field types](https://www.servicenow.com/docs/access?context=r_FieldTypes&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

 By default, there are only 18 field types to choose from. You can add a property to include more field types in Guided Application Creator. For more information, see [Add field types in Guided Application Creator](gac-add-field-types.md).

</td></tr><tr><td>

Display

</td><td>

When used as a reference field, the field is used as the display value for the table. Only one field can be defined as the display value for a table.

</td></tr><tr><td>

Mandatory

</td><td>

Option to require that the field must contain a value before the record can be saved.

</td></tr></tbody>
</table>3.  Select **Continue** to define properties and permissions for your custom table.

4.  On the form, fill in the fields.

<table id="table_b2v_pcw_5hb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table label

</td><td>

Unique label for the table \(such as **Laptops** or **Thin clients**\). The label appears on list and form views for the table. See Field Labels in [Data dictionary tables](https://www.servicenow.com/docs/access?context=c_DataDictionaryTables&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

</td></tr><tr><td>

Table name

</td><td>

Name of the table in the database. The table name is automatically populated based on the table label and the application scope that you defined earlier.

</td></tr><tr><td>

Make extensible

</td><td>

Option to enable other tables to extend this table.

 For more information on table extension, see [Table extension and classes](https://www.servicenow.com/docs/access?context=table-extension-and-classes&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

</td></tr><tr><td>

Auto-number

</td><td>

Option to add a number field to the table and automatically increment the ID numbers as they get added.

</td></tr><tr><td>

Manage access

</td><td>

User permissions for your application. For each role that you selected earlier, you can give different levels of access.-   **Create**

Enables users to insert new records \(rows\) into a table.

-   **Read**

Enables users to display records from a table.

-   **Write**

Enables users to update records in a table.

-   **Delete**

Enables users to remove records from a table or drop a table.

</td></tr></tbody>
</table>5.  Select **Continue**.

6.  On the confirmation screen, select **Continue**.

7.  To add more tables to your application, follow the steps in [Designate data tables in Guided Application Creator](gac-designate-data-table.md).

8.  To finish designating tables, select **Done with tables**.


## What to do next

Continue building your application by following the steps in [Customize user experiences in Guided Application Creator](gac-customize-ux.md#). If you exit Guided Application Creator, the tables that you configured are not saved to the system.

**Parent Topic:**[Designate data tables in Guided Application Creator](gac-designate-data-table.md)

