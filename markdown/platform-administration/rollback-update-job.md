---
title: Rollback an update job
description: Rollback a completed update job to revert the updates to the records.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Updating records safely, Data Management, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Rollback an update job

Rollback a completed update job to revert the updates to the records.

## Before you begin

Role required: admin

## About this task

If you want to revert the updates to records made through an update job, execute a rollback operation.

## Procedure

1.  Navigate to **All** &gt; **System Data Management** &gt; **Update jobs**.

2.  Select an update job that has been executed.

3.  Select the **Rollback** related link to revert the updated records.

4.  When prompted, confirm that you want to rollback the delete job.


## Result

The rollback job is executed immediately and the updated records are reverted to their prior versions. If you want to update the records again, create an update job using the same conditions, and then schedule the update job or execute it immediately.

**Parent Topic:**[Updating records safely](../concept/updating-records-safely.md)

