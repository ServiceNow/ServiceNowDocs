---
title: Create a scheduled job
description: Create a scheduled job on the Schedule Job \[sysauto\] table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/platform-administration/time-configuration/t\_CreateAScheduledJob.html
release: yokohama
product: Time Configuration
classification: time-configuration
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Scheduled jobs, System scheduler, Exploring time configuration, Time configuration, Configure core features, Administer the ServiceNow AI Platform]
---

# Create a scheduled job

Create a scheduled job on the Schedule Job \[sysauto\] table.

## Before you begin

Role required: admin

## About this task

Create all new scheduled jobs using this method.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

2.  Click **New**.

3.  Select the appropriate type of scheduled job.

    -   Automate the generation and distribution of a report
    -   Automatically generate something \(a change, an incident, a ci, etc\) from a template
    -   Automatically run a script of your choosing

## Result

The fields presented depend on the type of scheduled job required.

-   **[Automate generation and distribution of a report](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/platform-administration/time-configuration/schedule-report.md)**  
Generate and distribute scheduled reports via email.
-   **[Automatically generate something from a template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/platform-administration/time-configuration/t_ScheduleTheGenerationOfAnEntity.md)**  
Schedule the generation of entities, which include changes, incidents, and CIs.
-   **[Automatically run a script of your choosing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/platform-administration/time-configuration/t_ScheduleAScriptExecution.md)**  
Schedule both conditional and non-conditional scripts. If Domain Separation is installed in the instance, you can also select, filter, sort, and schedule scripts based on their assigned domains.

**Parent Topic:**[Scheduled jobs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/platform-administration/time-configuration/c_ScheduledJobs.md)

**Related topics**  


[Personalize the system date format](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/platform-administration/time-configuration/t_PersonalizeTheSystemDateFormat.md)

[Set a system time zone](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/platform-administration/time-configuration/t_SetASystemTimeZone.md)

[Special cases in job schedules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/platform-administration/time-configuration/r_SpecialCasesInJobSchedules.md)

[View a schedule item](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/platform-administration/time-configuration/t_ViewAScheduleItem.md)

