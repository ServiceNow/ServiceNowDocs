---
title: Rollback a delete job
description: Rollback a completed delete job to restore the deleted records.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Delete records safely, Data Management, Tables and data, Configure core features, Administer]
---

# Rollback a delete job

Rollback a completed delete job to restore the deleted records.

## Before you begin

Role required: admin

## About this task

If you want to restore records deleted through a delete job, execute a rollback operation.

## Procedure

1.  Navigate to **All** &gt; **System Data Management** &gt; **Delete jobs**.

2.  Select a delete job that has been executed.

3.  Select the **Rollback** related link to restore the deleted records.

4.  When prompted, confirm that you want to rollback the delete job.


## Result

The rollback job is executed immediately and the deleted records are restored. If you want to delete the restored records, create a delete job using the same conditions, and then schedule the delete job or execute it immediately.

**Parent Topic:**[Deleting records safely](../concept/deleting-records-safely.md)

