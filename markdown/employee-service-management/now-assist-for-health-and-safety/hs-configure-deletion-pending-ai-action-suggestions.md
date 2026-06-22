---
title: Configure retention period and cleanup of pending AI action suggestions
description: Configure how long the pending AI-generated action suggestions are retained before they are automatically deleted.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/now-assist-for-health-and-safety/hs-configure-deletion-pending-ai-action-suggestions.html
release: zurich
product: Now Assist for Health and Safety
classification: now-assist-for-health-and-safety
topic_type: task
last_updated: "2026-06-02"
reading_time_minutes: 2
breadcrumb: [Configure, Now Assist for Health and Safety, Health and Safety, Employee Service Management]
---

# Configure retention period and cleanup of pending AI action suggestions

Configure how long the pending AI-generated action suggestions are retained before they are automatically deleted.

## Before you begin

Verify the following conditions:

-   The Now Assist for Health and Safety application \(sn\_hs\_gen\_ai\) is installed. For more information, see [Install Now Assist for Health and Safety](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/now-assist-for-health-and-safety/now-assist-hs-install.md).
-   The application scope is selected as Health and Safety Core. For more information, see [Application picker](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/building-applications/c_ApplicationPicker.md).

Role required: sn\_ohs\_im.admin

## About this task

When the Action Planner generates AI suggestions, they are stored in the AI action suggestion \[sn\_ohs\_im\_ai\_action\_suggestion\] staging table. Users accept the suggestions to create actions or dismiss them. Suggestions that are never acted on \(that is, not accepted for action creation or dismissed\) accumulate over time and remain in the Pending state. A scheduled cleanup job deletes these pending suggestions after the configured number of days, helping to keep the staging table manageable.

For information on using Action planner for AI suggested actions, see [Generate and manage AI‑suggested safety actions in Action planner](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/now-assist-for-health-and-safety/now-assist-hs-generate-ai-suggested-actions-in-action-planner.md).

## Procedure

1.  Navigate to **All** &gt; **Health and Safety** &gt; **Health and Safety administration** &gt; **Properties**.

2.  To enable or disable cleanup, set the **Enables or disables the scheduled job that cleans up stale pending AI action suggestions** \[sn\_ohs\_im.ai\_suggestion.cleanup\_enabled\] property.

    -   **Yes**: The scheduled cleanup job runs daily and deletes pending suggestions that have exceeded the retention period. This is set by default.
    -   **No**: The scheduled cleanup job does not run. Pending suggestions are retained indefinitely.
3.  To configure the retention period, enter a value in the **Number of days to retain pending AI action suggestions before the scheduled cleanup job permanently deletes them as stale** \[sn\_ohs\_im.ai\_suggestion.retention\_days\] property.

    By default, this value is set to 90.

4.  Verify the scheduled cleanup job.

    1.  Navigate to **All** &gt; **Scheduled Jobs**.

    2.  Open the **Cleanup stale AI action suggestions** scheduled job and review the settings.

        **Note:** To run the scheduled job on demand, select **Execute Now**.


## Result

-   The scheduled job runs daily at the specified time. On each run, it queries the AI action suggestion \[sn\_ohs\_im\_ai\_action\_suggestion\] staging table for suggestions with `status = Pending` that are older than the configured retention period and deletes them.
-   Suggestions with `status = Accepted` or `status = Rejected` aren't deleted by the scheduled job, regardless of age.

**Parent Topic:**[Configuring Now Assist for Health and Safety](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/now-assist-for-health-and-safety/now-assist-hs-configuring.md)

