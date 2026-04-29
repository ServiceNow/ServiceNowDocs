---
title: Create a data management policy in Core UI
description: Define a set of rules for managing table data on your instance.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Manage data growth in Core UI, Data Management, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Create a data management policy in Core UI

Define a set of rules for managing table data on your instance.

## About this task

Data management policies streamline administration by allowing you to define multiple archive and table cleaner rules for a table within a single policy record. Additionally, you can easily activate or deactivate all rules simultaneously from the data management policy record.

After upgrading to Xanadu or higher, data management policies are automatically created for any table with an archive rule or table cleaner rule. If a data management policy doesn't exist for a table on your instance, you can create one manually.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Data Management** &gt; **Data Management Policies**.

2.  Determine if a data management policy exists for the table that you want to manage by searching the **Tablename** column.

    If the table already has a data management policy record, use that record instead of creating one.

3.  Select **New**.

4.  On the form, fill in the fields.

<table id="table_ptv_mpy_y1c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The name of the data management policy that typically includes the table name.

</td></tr><tr><td>

Tablename

</td><td>

The table that you want to manage to use a data management policy.

</td></tr><tr><td>

Description

</td><td>

An optional summary of the data management policy and its rules.

</td></tr><tr><td>

Active

</td><td>

Option to activate the data management policy. You must activate the data management policy for any of its rules to be activated.Clear this option to deactivate all the rules under the data management policy.

</td></tr></tbody>
</table>5.  Select **Update**.


## Result

A data management policy is established for the designated table. You can now create multiple data management rules for the table directly from the data management policy record.

## What to do next

Define archive and cleanup rules for the table by creating rules in the data management policy.

-   [Create an archive rule in Core UI](../../database-rotation/task/t_CreateAnArchiveRule.md#)
-   [Create a table cleanup rule in Core UI](activate-table-cleanup.md)

**Parent Topic:**[Managing data growth in Core UI](../concept/data-management-policies.md)

