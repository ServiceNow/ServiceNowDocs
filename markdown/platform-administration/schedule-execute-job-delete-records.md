---
title: Schedule or execute a job to delete records
description: Schedule a date and time to execute a delete job or execute the job immediately.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Deleting records safely, Data Management, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Schedule or execute a job to delete records

Schedule a date and time to execute a delete job or execute the job immediately.

## Before you begin

Role required: admin

## About this task

Consider scheduling the delete job to run during non-business hours to minimize the potential performance impact on your users. Deleting all records in a table temporarily locks the table, which prevents inserts and updates. If you want to delete all records from a table, use the table cleaner option instead. For more information, see [Deleting older or unwanted records](../concept/deleting-older-records.md).

## Procedure

1.  Navigate to **All** &gt; **System Data Management** &gt; **Delete jobs**.

2.  Select a delete job record.

3.  Determine whether to schedule the delete job for a later time or run it right away.

<table id="choicetable_kdq_2q5_qtb"><thead><tr><th align="left" id="d261106e89">

Option

</th><th align="left" id="d261106e92">

Description

</th></tr></thead><tbody><tr><td id="d261106e98">

**Schedule the delete job**

</td><td>

1.  Select the calendar icon in the **Run at** field.
2.  Enter the date and time you want the delete job to run.
3.  Select **Update** to save the schedule.


</td></tr><tr><td id="d261106e125">

**Run the delete job now**

</td><td>

1.  Select **Execute Now** to run the delete job immediately.
2.  When prompted, select **Proceed** to delete the records now.
3.  On the Progress page, select **Cancel** to stop the job from continuing to run.
4.  Select **Check execution results** to return to the delete job form.
5.  In the **Deletion Counts** table, view the **Actual record count** column to see an updated count of deleted records from each table.
6.  Select the **View Rollback Context** link to review the changes.


</td></tr></tbody>
</table>
## Result

The records are scheduled for deletion or deleted immediately. If you want to restore the deleted records, see [Rollback a delete job](rollback-delete-job.md).

**Parent Topic:**[Deleting records safely](../concept/deleting-records-safely.md)

