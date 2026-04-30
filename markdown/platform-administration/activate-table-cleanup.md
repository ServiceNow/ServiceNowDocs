---
title: Create a table cleanup rule
description: Define the criteria for deleting unwanted records in a table cleanup rule.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Deleting older or unwanted records, Manage data growth, Data Management, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Create a table cleanup rule

Define the criteria for deleting unwanted records in a table cleanup rule.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Data Management Policies**.

2.  Select the data management policy for the table that contains the records you want to delete.

    If the table doesn't have a data management policy record, create one. See [Create a data management policy](create-data-management-policy.md).

3.  In the Table Cleanup Rules related list, select **New**.

4.  On the form, fill in the fields.

<table id="table_tn5_rbr_ktb"><thead><tr><th>

Field

</th><th>

Description\`

</th></tr></thead><tbody><tr><td>

Tablename

</td><td>

The name of the target table.

</td></tr><tr><td>

Matchfield

</td><td>

The Date/Time field in the target table that is used to monitor duration. Defaults to sys\_created\_on, which deletes records based on the amount of time since their creation date.

</td></tr><tr><td>

Age in seconds

</td><td>

The amount of time the system waits before deleting records. When the **Matchfield** value becomes older than the **Age in seconds**, the record is deleted.

</td></tr><tr><td>

Active

</td><td>

Option to activate or deactivate table cleaning for this table.

</td></tr><tr><td>

Application

</td><td>

The application scope to which this table cleaner job applies.

</td></tr><tr><td>

Clean attachments and journals

</td><td>

If selected, related records in the Journal Entry \[sys\_journal\_field\] table are also deleted.If cleared, the system deletes records from the target table, but not any related journal records in this table.

**Note:** Although attachments are mentioned in the label, this option only applies to journal records.

</td></tr><tr><td>

Clean audit

</td><td>

If selected, related records in these audit tables are also deleted:-   Sys Audit \[sys\_audit\] table
-   Audit Relationship Change \[sys\_audit\_relation\] table
Note that the audit records that are created by table cleaner in the Audit Deleted Record \[sys\_audit\_delete\] table are preserved.

If cleared, the system deletes records from the target table, but not any related audit records in these tables.

</td></tr><tr><td>

Cascade delete

</td><td>

If selected, this option deletes all matching records plus any records referring to them. If cleared, the system deletes matching records, but not records referring to them.

</td></tr><tr><td>

Conditions

</td><td>

Condition builder for specifying filter conditions that define the records to be removed. For example, you might specify that only records where 'active = false AND state =closed' are deleted.

</td></tr></tbody>
</table>5.  Select **Submit**.


## Result

Table cleaner runs automatically and deletes records when they meet the specified record age and any conditions that you set for them.

**Parent Topic:**[Deleting older or unwanted records](../concept/deleting-older-records.md)

