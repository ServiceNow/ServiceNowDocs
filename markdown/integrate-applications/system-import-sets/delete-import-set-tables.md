---
title: Delete import set tables
description: Delete import set tables, related transform maps, or data only \(preserving the table structure\) to clean up your database.
locale: en-US
release: yokohama
product: System Import Sets
classification: system-import-sets
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Importing data using import sets, Import sets, Imports, Data and Automation]
---

# Delete import set tables

Delete import set tables, related transform maps, or data only \(preserving the table structure\) to clean up your database.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Import Sets** &gt; **Import Set Tables** &gt; **Cleanup**.

2.  Move the tables you want to delete from **Available tables for deletion** to **Delete these tables**.

    Deleting any table deletes all records and removes the table.

3.  Include deleting related transform maps when you delete the import set tables by selecting the **Delete related transform maps** check box.

    All records and all associated transform maps are removed.

4.  Delete only data from the selected import set tables and preserve the table structure by selecting the **Delete data only \(preserve table structure\)** check box.

    All records are removed, but the tables remain intact.

5.  Click **Cleanup**.


**Parent Topic:**[Importing data using import sets](../concept/c_ImportDataUsingImportSets.md)

