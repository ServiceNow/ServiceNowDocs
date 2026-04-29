---
title: Rollback an update job
description: Rollback a completed update job to revert the updates to the records.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Updating records safely in Core UI, Manage data growth in Core UI, Data Management, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
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

**Parent Topic:**[Updating records safely in Core UI](../concept/updating-records-safely.md)

