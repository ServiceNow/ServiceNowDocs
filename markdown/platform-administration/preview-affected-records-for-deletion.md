---
title: Preview affected records for deletion
description: Before you run a delete job, preview the count of affected records to see the impact of executing the delete job.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Delete records safely, Data Management, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Preview affected records for deletion

Before you run a delete job, preview the count of affected records to see the impact of executing the delete job.

## Before you begin

Role required: admin

## About this task

Deleting records in a table also deletes records from tables that extend or reference the source table. Preview the affected records before you execute a delete job and learn about other tables that are impacted.

Up to three levels of cascaded records are deleted when the job is executed. For example, if the preview identifies incidents that match the conditions, it will also delete any problems that reference those incidents, defects that reference those problems, and test records that reference the defects. If sys\_attachment and sys\_attachment\_docs table records are associated with the incidents, those records might not appear in the preview but they are deleted as well.

## Procedure

1.  Navigate to **All** &gt; **System Data Management** &gt; **Delete jobs**.

2.  Select a delete job record.

3.  Select the **Preview Cascade** related link to view the count of records from the source table that match the conditions in the delete job.

    The record count appears in the **Preview record count** column. Counts for records in other tables that reference those source records are listed as well, although those counts are only close estimates.

4.  Review the count of affected records by table to ensure that the records are safe to delete.


## What to do next

[Schedule or execute a job to delete records](schedule-execute-job-delete-records.md)

**Parent Topic:**[Deleting records safely](../concept/deleting-records-safely.md)

