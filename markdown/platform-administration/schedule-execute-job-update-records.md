---
title: Schedule or execute a job to update records
description: Schedule a date and time to execute an update job or execute the job immediately.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Update records safely, Data Management, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Schedule or execute a job to update records

Schedule a date and time to execute an update job or execute the job immediately.

## Before you begin

Role required: admin

## About this task

Consider scheduling the update job to run during non-business hours to minimize the potential performance impact on your users. Updating a large number of records can degrade performance depending on the size of the table. On instances running MariaDB, UPDATE operations affecting a majority of rows may trigger gap locks, escalating to a full table lock until the update completes. INSERT operations are not affected by this locking behavior.

## Procedure

1.  Navigate to **All** &gt; **System Data Management** &gt; **Update jobs**.

2.  Select an update job record.

3.  Determine whether to schedule the update job for a later time or run it right away.

<table id="choicetable_vjl_krf_vtb"><thead><tr><th align="left" id="d242443e88">

Option

</th><th align="left" id="d242443e91">

Description

</th></tr></thead><tbody><tr><td id="d242443e97">

**Schedule the update job**

</td><td>

1.  Select the calendar icon in the **Run at** field.
2.  Enter the date and time you want the update job to run.
3.  Select **Update**. Note that you must select **Update** to successfully schedule the job.


</td></tr><tr><td id="d242443e127">

**Run the update job now**

</td><td>

1.  Select **Execute Now** to run the update job immediately.
2.  When prompted, select **Proceed** to update the records now.
3.  On the Progress page, select **Cancel** to stop the job from continuing to run.
4.  Select **Check execution results** to return to the update job form.


</td></tr></tbody>
</table>
## Result

The records are scheduled for update or updated immediately. If you want to revert the updates to the records, see [Rollback an update job](rollback-update-job.md).

**Parent Topic:**[Updating records safely](../concept/updating-records-safely.md)

