---
title: Use the Deleted Records module to restore a deleted record
description: You can recover deleted records that are in audited tables.
locale: en-US
release: zurich
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Roll back and delete recovery, Tables and data, Configure core features, Administer]
---

# Use the Deleted Records module to restore a deleted record

You can recover deleted records that are in audited tables.

## Before you begin

Role required: admin

## About this task

The instance can track deletions on any table, and references on audited tables, with a few exceptions. Record deletions are not tracked in these circumstances:

-   Record deletions are not tracked on tables with the `no_audit_delete=true` [dictionary attribute](../../reference-pages/concept/c_DictionaryAttributes.md).
-   Not all tables with a sys prefix track deletions by default. You can [Enable auditing for a system table](https://www.servicenow.com/docs/access?context=t_ConSysTablDelAud&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).
-   References are restored only if the reference field is on an audited table and the Restore Deleted Record plugin is activated.
-   References that use an **Image** field type are not restored.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Deleted Records**.

2.  Open the deleted record that you want to restore.

    **Note:** You can only restore one deleted record and its associated references at a time.

3.  Do one of the following to restore the record.

<table id="choicetable_rxr_mx3_jdb"><tbody><tr><td id="d242428e126">

**Undelete With Related**

</td><td>

Recovers the record and all cascaded deletes and other database actions that resulted from the delete.This option appears when a rollback context is available for the delete.

</td></tr><tr><td id="d242428e138">

**Recover entire operation**

</td><td>

If this record was deleted as part of another delete, all records from the parent delete are recovered including all cascaded deletes and other database actions that resulted from the parent delete. If this is the top level delete, then this is the same as **Undelete with Related**.This option appears when a rollback context is available for the delete.

</td></tr><tr><td id="d242428e153">

**Undelete Record**

</td><td>

Recovers only this record.**Important:**

The undelete operation performs an insert, which can trigger business rules. This might lead to additional inserts and updates on related records in other tables, potentially resulting in unexpected outcomes. For guidance on avoiding this behavior, contact Customer Service and Support.

</td></tr></tbody>
</table>    An instructions page appears, explaining the process and its limitations.

4.  Click **Restore deleted record**.

    A Progress page shows the progress of the restore process, and shows a count of the references restored.


## Result

When the process completes, a Restore Summary itemizes the changes and provides links for viewing the restored record or returning to the deleted records list.

**Parent Topic:**[Roll back and delete recovery](../concept/rollback-delete-recovery.md)

