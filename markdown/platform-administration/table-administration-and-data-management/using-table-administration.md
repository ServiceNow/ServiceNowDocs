---
title: Managing tables and indexes
description: Administrators can modify the database structure using table administration tools.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/table-administration-and-data-management/using-table-administration.html
release: australia
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Table admin, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Managing tables and indexes

Administrators can modify the database structure using table administration tools.

## Custom tables and fields

Administrators can add custom tables, define fields, and manage field labels. Administrators can also delete custom tables that aren't needed or delete all the records in a table without deleting the table itself.

## Dictionary entries

The system dictionary is a table, called Dictionary Entry `[sys_dictionary]`, that contains details for each table and defines every column within each table in an instance. Administrators can modify tables and fields in the system dictionary, which subsequently define the lists and forms that users access throughout the instance.

## Dictionary attributes

Dictionary attributes define global behavior for fields. An administrator applies attributes directly to the dictionary entry to control various aspects of how the table or field behaves across the entire system.

## Dictionary overrides

Dictionary overrides enable administrators to override field settings on extended tables. Dictionary overrides enable administrators to customize the behavior of a field for a specific table that inherits from another table. Overrides are used to change the inherited dictionary attributes on child tables without affecting the parent table or other child tables.

## Table flattening

With table flattening, the Task \[task\] table and Base Configuration Item \[cmdb\] table have a hierarchy of related tables where one or more child tables extend from a parent table.

The extension model does not affect how the tables appear or function in the instance. All table functionality, including database views, remains unchanged by the extension model.

## Table indexes

An index puts unordered tables into order, and efficiently speeds up queries to columns in your tables, by creating pointers to where information is stored in your database. Administrators can add indexes to access table data more easily.

## Many-to-many table relationships

Many-to-many \(M2M\) table relationships enable administrators to associate records between two tables in a bidirectional and flexible manner. This relationship type is used to create links between records where each record from one table can relate to multiple records in another table, and vice versa.

**Note:** It is to be noted that when you de-activate or delete a field from the dictionary on a table, it might impact on the personalized UI view lists and will remove all regardless if they contain the de-activated/deleted field.

-   **[Create a table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/table-administration-and-data-management/t_CreateATable.md)**  
Administrators and application developers can create custom tables to store application data. After you create a table, you can also modify field types and field labels.
-   **[Deleting custom tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/table-administration-and-data-management/c_DeleteATable.md)**  
Administrators can delete custom tables that are no longer needed. For example, delete a table from an application that is under development because the business requirements change.
-   **[Modify dictionary entries](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/table-administration-and-data-management/t_ModifyADictionaryEntryFromAForm.md)**  
Modify dictionary entries by configuring a field on a form or from the Dictionary module.
-   **[Configuring read-only security options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/table-administration-and-data-management/read-only-option.md)**  
Control the ability to edit read-only fields by configuring read-only options.
-   **[Altering tables and fields using dictionary attributes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/table-administration-and-data-management/c_DictionaryAttributes.md)**  
Dictionary attributes alter the behavior of the table or field that the dictionary record describes. Administrators can add or modify dictionary attributes.
-   **[Dictionary overrides](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/table-administration-and-data-management/c_DictionaryOverrides.md)**  
Dictionary overrides provide the ability to define a field on an extended table differently from the field on the parent table.
-   **[Table flattening](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/table-administration-and-data-management/c_TaskTableFlattening.md)**  
Table flattening stores a hierarchy of related tables as one table in a relational database.
-   **[Viewing table references and extensions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/table-administration-and-data-management/c_SchemaMapForTables.md)**  
View table relationships in a visual manner using the schema map.
-   **[Create a table index](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/table-administration-and-data-management/t_CreateCustomIndex.md)**  
Build indexes to access the data held in your tables more easily.
-   **[Drop a custom index](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/table-administration-and-data-management/drop-custom-index.md)**  
Remove a custom index by dropping it from a table.
-   **[Create a many-to-many table relationship](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/table-administration-and-data-management/t_CreateAManyToManyRelationship.md)**  
Create a bi-directional relationship between two tables, so that the related records are visible from both tables in a related list.

**Parent Topic:**[ServiceNow AI Platform tables and data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/table-administration-and-data-management/tables-fields-and-forms.md)

