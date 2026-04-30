---
title: Delete a custom table
description: If you no longer need a custom table, you can delete it after you delete all the records in the table.
locale: en-US
release: yokohama
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Deleting custom tables, Manage tables and indexes, Table administration, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Delete a custom table

If you no longer need a custom table, you can delete it after you delete all the records in the table.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Tables**.

2.  Open the table to delete.

3.  Select **Delete All Records**.

    Deleting all records before deleting the table ensures that the business logic is properly executed \(for example, reference cascade rules or other delete business rules\). If you do not delete all records from the table first, then you must manually fix any other records or tables that the table deletion impacts. Cascade deletions are also taken care of in this step.

4.  Select **Delete**.

    The **Delete** button is only available for custom tables beginning with u\_ \(global\) or x\_ \(scoped\).

5.  In the confirmation dialog box, enter `delete` and click **OK**.

    The table and all items that reference the table are deleted, including:

    -   Choice list items
    -   Forms, form sections, lists, and related lists
    -   Reports and Performance Analytics widgets
    -   Reference fields that reference the table
    -   Access controls

**Parent Topic:**[Deleting custom tables](../concept/c_DeleteATable.md)

**Related topics**  


[Deleting custom tables](../concept/c_DeleteATable.md)

