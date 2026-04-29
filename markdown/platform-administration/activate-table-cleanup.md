---
title: Create a table cleanup rule in Core UI
description: Define the criteria for deleting unwanted records in a table cleanup rule.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Deleting older or unwanted records in Core UI, Manage data growth in Core UI, Data Management, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Create a table cleanup rule in Core UI

Define the criteria for deleting unwanted records in a table cleanup rule.

## Before you begin

Role required: admin

## Procedure

1.  Access the new Auto Flush form in one of the following ways.

<table id="choicetable_bxv_hjk_1bc"><thead><tr><th align="left" id="d68402e52">

Option

</th><th align="left" id="d68402e55">

Steps

</th></tr></thead><tbody><tr><td id="d68402e61">

**Using the Data Management Console**

</td><td>

1.  Navigate to **All** &gt; **System Data Management** &gt; **Data Management Console** &gt; ****.
2.  On the Overview tab, select **New cleanup rule**.


</td></tr><tr><td id="d68402e96">

**Using a data management policy**

</td><td>

1.  Navigate to **All** &gt; **System Data Management** &gt; **Data Management Policies**.
2.  Select the data management policy for the table with records that you want to delete.
3.  In the Table Cleanup Rules related list, select **New**.


</td></tr></tbody>
</table>2.  On the form, fill in the fields.

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

Clean journals

</td><td>

If selected, related records in the Journal Entry \[sys\_journal\_field\] table are also deleted.If cleared, the system deletes records from the target table, but not any related journal records in this table.

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
</table>3.  Select **Submit**.


## Result

The table cleanup rule runs automatically and deletes records when they meet the specified record age and any conditions that you set for them.

**Parent Topic:**[Deleting older or unwanted records in Core UI](../concept/deleting-older-records.md)

