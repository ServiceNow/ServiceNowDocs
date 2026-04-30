---
title: Deleting records safely
description: Safely delete records from a table without using scripts and without deleting the table by creating and executing delete jobs.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Data Management, Tables and data, Configure core features, Administer]
---

# Deleting records safely

Safely delete records from a table without using scripts and without deleting the table by creating and executing delete jobs.

## Overview of deleting records safely

1.  [Mark records for deletion](../task/mark-records-for-deletion.md)

    Determine which records to delete by creating a delete job.

2.  [Preview affected records for deletion](../task/preview-affected-records-for-deletion.md)

    Preview the affected records before you schedule or execute the job. For example, you might want to preview a set of incident records that will be deleted before you delete them.

3.  [Schedule or execute a job to delete records](../task/schedule-execute-job-delete-records.md)

    Schedule the job to run later or execute the job immediately.

4.  [Rollback a delete job](../task/rollback-delete-job.md)

    Use the rollback option in the delete job If you need to restore deleted records after the job has run.


If you must delete a large number of records from a table rather than a selection of records, use the table cleaner option. For details, see [Deleting older or unwanted records](deleting-older-records.md).

-   **[Mark records for deletion](../task/mark-records-for-deletion.md)**  
Mark records for deletion according to one or more criteria by creating a delete job.
-   **[Preview affected records for deletion](../task/preview-affected-records-for-deletion.md)**  
Before you run a delete job, preview the count of affected records to see the impact of executing the delete job.
-   **[Schedule or execute a job to delete records](../task/schedule-execute-job-delete-records.md)**  
Schedule a date and time to execute a delete job or execute the job immediately.
-   **[Rollback a delete job](../task/rollback-delete-job.md)**  
Rollback a completed delete job to restore the deleted records.

**Parent Topic:**[Data Management](c_DataManagement.md)

