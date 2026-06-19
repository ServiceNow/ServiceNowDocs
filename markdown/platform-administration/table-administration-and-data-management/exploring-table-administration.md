---
title: Exploring ServiceNow AI Platform tables
description: Applications use tables and records to manage data and processes, such as Incident, Problem, and CMDB. Tables can extend other tables, creating parent tables and child tables.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/table-administration-and-data-management/exploring-table-administration.html
release: australia
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Table admin, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Exploring ServiceNow AI Platform tables

Applications use tables and records to manage data and processes, such as Incident, Problem, and CMDB. Tables can extend other tables, creating parent tables and child tables.

## Table administration overview

The ServiceNow AI Platform® uses a table-based data structure to store and organize information. Pre-built tables are included for common IT service management \(ITSM\) processes, with their data fully importable and exportable in CSV, XML, or other formats.

## Table administration users

|User|Description|
|----|-----------|
|Administrator|Admins can create custom tables for specific business requirements, define field properties, create relationships between tables, and extend existing tables without modifying the originals. Administrators also define access controls to allow only approved user access to records, business rules for various tasks, and table cleanup policies for unused and outdated records.|

## Table administration workflow

This infographic depicts how an administrator can extend both core tables and custom tables.

\[Omitted image "exploring-now-platform-tables.png"\] Alt text: Data can be exported and imported between Core Tables and Custom Tables. Admins define access controls to restrict access.

1.  An administrator views table relationships and learns how table extension works on the ServiceNow AI Platform®.
2.  The administrator creates a custom parent table and extends it by creating a custom child table.
3.  The administrator defines access controls to restrict access to each table.
4.  The administrator exports and imports data to core and custom tables as needed.

## Table administration benefits

|Benefit|Feature|Users|
|-------|-------|-----|
|Define models and entity relationships across multiple tables.|[Data dictionary tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/table-administration-and-data-management/c_DataDictionaryTables.md)|Admin|
|Access visual references for tables and their contents.|[Viewing table references and extensions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/table-administration-and-data-management/c_SchemaMapForTables.md)|Admin|
|Store records for your instance.|[Create a table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/table-administration-and-data-management/t_CreateATable.md)|Admin|
|Remove unneeded tables from your instance.|[Deleting custom tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/table-administration-and-data-management/c_DeleteATable.md)|Admin|
|Quickly find data stored in a table.|[Create a table index](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/table-administration-and-data-management/t_CreateCustomIndex.md)|Admin|
|Connect a list to another list of multiple entries instead of a single field.|[Create a many-to-many table relationship](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/table-administration-and-data-management/t_CreateAManyToManyRelationship.md)|Admin|
|Organize and store task-related data.|[Working with the Task table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/table-administration-and-data-management/c_TaskTable.md)|Admin|
|Connect tables for reporting purposes.|[Working with database views for reporting](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/table-administration-and-data-management/c_DatabaseViews.md)|Admin|

## What to explore next

To learn more about using table administration features, see:

-   [Managing tables and indexes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/table-administration-and-data-management/using-table-administration.md)
-   [Working with the Task table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/table-administration-and-data-management/c_TaskTable.md)
-   [Working with database views for reporting](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/table-administration-and-data-management/c_DatabaseViews.md)

-   **[Custom tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/table-administration-and-data-management/custom-tables.md)**  
Custom tables enable you to expand the functionality of the ServiceNow AI Platform and create custom applications.
-   **[Data dictionary tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/table-administration-and-data-management/c_DataDictionaryTables.md)**  
Access details related to tables, columns, and field labels in your instance.
-   **[System dictionary](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/table-administration-and-data-management/c_SystemDictionary.md)**  
View a list of all tables in columns in your instance from the system dictionary.
-   **[Table relationships](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/table-administration-and-data-management/table-relationships.md)**  
You can create relationships between tables by extending tables, referencing records in another table, creating many-to-many relationships, and joining tables in a database view.
-   **[Table extension and classes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/table-administration-and-data-management/table-extension-and-classes.md)**  
Enable one or more child tables to share fields and records with a parent table. Administrators and application developers can only extend tables during table creation.
-   **[Storage aliases](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/table-administration-and-data-management/storage-aliases.md)**  
Learn about the role storage aliases play in data manipulation and field creation in the ServiceNow AI Platform.

**Parent Topic:**[ServiceNow AI Platform tables and data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/table-administration-and-data-management/tables-fields-and-forms.md)

