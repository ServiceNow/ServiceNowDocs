---
title: Updating records safely
description: Update several records simultaneously without using scripts by creating and executing a batch update job.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Data Management, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Updating records safely

Update several records simultaneously without using scripts by creating and executing a batch update job.

## Overview

To update multiple records safely, create an update job, and then preview the number of affected records before you schedule or execute the job. For example, you might want to update the Assigned to value for multiple incidents on a test instance without running a script.

If you must restore the updated records to their previous state, use the rollback option in the update job.

-   **[Mark records for updating](../task/mark-records-update.md)**  
Mark records for updating according to one or more criteria by creating an update job.
-   **[Schedule or execute a job to update records](../task/schedule-execute-job-update-records.md)**  
Schedule a date and time to execute an update job or execute the job immediately.
-   **[Rollback an update job](../task/rollback-update-job.md)**  
Rollback a completed update job to revert the updates to the records.

**Parent Topic:**[Data Management](c_DataManagement.md)

