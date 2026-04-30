---
title: Deleting custom tables
description: Administrators can delete custom tables that are no longer needed. For example, delete a table from an application that is under development because the business requirements change.
locale: en-US
release: yokohama
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Manage tables and indexes, Table administration, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Deleting custom tables

Administrators can delete custom tables that are no longer needed. For example, delete a table from an application that is under development because the business requirements change.

A table is custom if an administrator created it and it is not part of a system upgrade or plugin activation. Custom table names always begins with `u_`, or `x_` for scoped tables.

**Warning:** You cannot delete base system tables. If you inadvertently delete such a table, it is automatically recreated when you upgrade an instance.

You cannot delete a table that has associated tables that extend from it.

You must first delete all records in the table before you delete the table itself. If you do not first delete the records, errors can result on the parent table if it references the records. Deleting the records removes any references from the parent table. To learn more, see [delete the records in the table](../task/t_DeleteAllRecordsFromATable.md).

-   **[Delete a custom table](../task/t_DeleteACustomTable.md)**  
If you no longer need a custom table, you can delete it after you delete all the records in the table.
-   **[Delete all records from a table](../task/t_DeleteAllRecordsFromATable.md)**  
You may decide to delete all the records on a table without deleting the table itself. For example, the administrator may want to delete all incidents on a test instance without deleting the incident table itself.

**Parent Topic:**[Managing tables and indexes](using-table-administration.md)

