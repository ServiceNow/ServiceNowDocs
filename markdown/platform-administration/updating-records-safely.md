---
title: Updating records safely in Core UI
description: Update several records simultaneously without using scripts by creating and executing a batch update job.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/updating-records-safely.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Manage data growth in Core UI, Data Management, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Updating records safely in Core UI

Update several records simultaneously without using scripts by creating and executing a batch update job.

## Overview of updating records safely

1.  [Mark records for updating](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/mark-records-update.md)

    Determine which records to update by creating an update job. Preview the number of affected records before you schedule or execute the job. For example, you might want to update the Assigned to value for multiple incidents on a test instance without running a script.

2.  [Schedule or execute a job to update records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/schedule-execute-job-update-records.md)

    Schedule the job to run later or execute the job immediately.

3.  [Rollback an update job](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/rollback-update-job.md)

    Use the rollback option in the update job if you need to restore the updated records to their previous state.


-   **[Mark records for updating](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/mark-records-update.md)**  
Mark records for updating according to one or more criteria by creating an update job.
-   **[Schedule or execute a job to update records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/schedule-execute-job-update-records.md)**  
Schedule a date and time to execute an update job or execute the job immediately.
-   **[Rollback an update job](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/rollback-update-job.md)**  
Rollback a completed update job to revert the updates to the records.

**Parent Topic:**[Managing data growth in Core UI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/data-management-policies.md)

