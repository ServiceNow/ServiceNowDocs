---
title: Schedule job for audit date enhancement
description: Scheduled Jobs are automated pieces of work that can be performed at a specific time or on a recurring schedule. Execute this scheduled job to enable enhanced audit date behavior. The audit date enhancements provide improved handling of fieldwork dates at the engagement level, making them independent of child audit task dates.
locale: en-US
release: zurich
product: Audit Management
classification: audit-management
topic_type: task
last_updated: "2025-11-20"
reading_time_minutes: 1
breadcrumb: [Create audit engagement, Manage engagements, Use, Audit Management, Governance, Risk, and Compliance]
---

# Schedule job for audit date enhancement

Scheduled Jobs are automated pieces of work that can be performed at a specific time or on a recurring schedule. Execute this scheduled job to enable enhanced audit date behavior. The audit date enhancements provide improved handling of fieldwork dates at the engagement level, making them independent of child audit task dates.

## Before you begin

Role required: sn\_audit.admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

2.  Enter **Audit date enhancements** in the filter search bar to search for the audit date-scheduled jobs.![Searching audit date enhancement scheduled jobs](../image/Scheduled-Jobs-Audit-Date-Enhancements.png)

3.  Select **Audit date enhancements** from the search result list.

4.  Select **Execute Now** to schedule the audit date enhancement job.


## Result

The scheduled job will update the behavior for the following tables:

-   Engagement \(sn\_audit\_engagement\)
-   Audit Task \(sn\_audit\_task\)
-   Control Test \(sn\_audit\_control\_test\)
-   Walkthrough \(sn\_audit\_walkthrough\)
-   Interview \(sn\_audit\_interview\)
-   Activity \(sn\_audit\_activity\)

After the job completes, the new audit date behavior will be active for all engagements and related records.

**Note:** If you have updated to application version 21.1.2 or later, the audit date enhancements are activated automatically during the update. You do not need to run this scheduled job.

**Parent Topic:**[Create an engagement](t_CreateEngagement.md)

