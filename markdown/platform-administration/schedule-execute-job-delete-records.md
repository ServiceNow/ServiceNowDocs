---
title: Schedule or execute a job to delete records
description: Schedule a date and time to execute a delete job or execute the job immediately.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Delete records safely, Data Management, Tables and data, Configure core features, Administer]
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


## Result

The records are scheduled for deletion or deleted immediately. If you want to restore the deleted records, see [Rollback a delete job](rollback-delete-job.md).

**Parent Topic:**[Deleting records safely](../concept/deleting-records-safely.md)

