---
title: Managing archived data
description: Change the schedule for an archive rule, stop the archive rule from running, or restore your archived data.Modify the system-scheduled job if you need to change the archive interval.Stop archiving by deactivating, deleting, or canceling an archive rule.Restore an archive record and optionally any related records back into the primary table.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Archiving records, Manage data growth, Data Management, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Managing archived data

Change the schedule for an archive rule, stop the archive rule from running, or restore your archived data.

**Parent Topic:**[Archiving records](archiving-older-records.md)

## Change an archive schedule

Modify the system-scheduled job if you need to change the archive interval.

### Before you begin

Role required: admin

### About this task

All active archive rules are executed by a system-scheduled job set to run every 60 minutes.

### Procedure

1.  Navigate to **All** &gt; **System Scheduler** &gt; **Scheduled Jobs**.

2.  Open the **Archive** record.

3.  Modify the **repeat** value.


## Stop an active archive rule

Stop archiving by deactivating, deleting, or canceling an archive rule.

### Before you begin

Role required: admin

### Procedure

1.  Access the archive rule that you want to stop in one of the following ways.

<table id="choicetable_cxh_nkk_1bc"><thead><tr><th align="left" id="d204688e185">

Option

</th><th align="left" id="d204688e188">

Steps

</th></tr></thead><tbody><tr><td id="d204688e194">

**Using a data management policy**

</td><td>

1.  Navigate to **All** &gt; **System Data Management** &gt; **Data Management Policies**.
2.  Select the data management policy with the archive rule that you want to stop.
3.  In the Archive Rules related list, select the archive rule that you want to stop.


</td></tr><tr><td id="d204688e227">

**Using the Archive Rules module**

</td><td>

1.  Navigate to **All** &gt; **System Archiving** &gt; **Archive Rules**.
2.  Select the archive rule that you want to stop.


</td></tr></tbody>
</table>2.  Stop the archive rule from running.

    -   Deactivate the archive rule by clearing the **Active** check box. The **Archive - Handle archive chunks** business rule updates the state of the corresponding record in the Archive Job Execution Chunks \[sys\_archive\_run\_chunk\] table from **waiting** to **not-needed**.
    -   Contact Customer Service and Support to delete the archive rule.
    -   Cancel the archive rule by calling GlideArchiver\(\).cancel\(\) from **System Maintenance** &gt; **Scripts - Background**. This automatically changes the chunks in the Archive Job Execution Chunks \[sys\_archive\_run\_chunk\] table from **running** to **cancelled**.

### Result

No additional chunks are processed.

## Restore archived records and related records

Restore an archive record and optionally any related records back into the primary table.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to the archived record that you want to restore in one of the following ways.

<table id="choicetable_l2x_vvy_1bc"><thead><tr><th align="left" id="d204688e368">

Option

</th><th align="left" id="d204688e371">

Steps

</th></tr></thead><tbody><tr><td id="d204688e377">

**Using a data management policy**

</td><td>

1.  Navigate to **All** &gt; **System Data Management** &gt; **Data Management Policies**.
2.  Select the data management policy that contains the archive rule.
3.  In the Archive Rules related list, select the archive rule that archived the record.
4.  In the Archive Run related list, select the archive run that was executed.
5.  In the Archive Log related list, select the archived record that you want to restore.


</td></tr><tr><td id="d204688e416">

**Using the Archive Log module**

</td><td>

1.  Navigate to **All** &gt; **System Archiving** &gt; **Archive Log**.
2.  Select the archived record to restore.


</td></tr></tbody>
</table>2.  In the Archive Log form, select the applicable related link:

    -   **Restore Record**
    -   **Restore Record and Related Records**
    **Warning:** Don’t delete archive record log entries. Deleting an archive log entry prevents you from restoring the data for the archived records.


### Result

The record is restored to the primary table. The archive record is deleted from the archive table.

### What to do next

View the restore date and time in the **Restored** column in the Archive Log related list.

