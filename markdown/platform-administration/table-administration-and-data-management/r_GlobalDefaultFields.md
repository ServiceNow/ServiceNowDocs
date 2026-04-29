---
title: Global default fields
description: When you create a new custom table, several fields appear in the Table Columns embedded list. For all tables, required system fields are added automatically. You cannot delete or modify these fields.
locale: en-US
release: australia
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create a table, Managing tables and indexes, Table admin, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Global default fields

When you create a new custom table, several fields appear in the **Table Columns** embedded list. For all tables, required system fields are added automatically. You cannot delete or modify these fields.

For tables that extend another table, fields on the parent table also appear on the **Table Columns** embedded list for the current table. If you modify these fields, remember that all changes to fields on the parent table also affect all child tables, not just the current table.

These required system fields are added to all tables:

|Field|Type|Description|
|-----|----|-----------|
|Class \[sys\_class\_name\]|System Class Name|If the table is extensible, a string field that indicates which child table contains the record.|
|Created \[sys\_created\_on\]|Date/Time|A time-stamp field that indicates when a record was created.|
|Created by \[sys\_created\_by\]|String|A string field that indicates the user who created the record.|
|Sys\_id \[sys\_id\]|Sys ID|The [Unique record identifier \(sys\_id\)](../../../administer/table-administration/concept/c_UniqueRecordIdentifier.md#) for the record.|
|Updates \[sys\_mod\_count\]|Integer|A numeric field that counts the number of updates for this record since record creation.|
|Updated by \[sys\_updated\_by\]|String|A string field that indicates the user who most recently updated the record.|
|Updated \[sys\_updated\_on\]|Date/Time|A time-stamp field that indicates the date and time of the most recent update.|

**Parent Topic:**[Create a table](../../../administer/table-administration/task/t_CreateATable.md)

