---
title: Create a scheduled job
description: Create a scheduled job on the Schedule Job \[sysauto\] table.
locale: en-US
release: zurich
product: Time Configuration
classification: time-configuration
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Scheduled jobs, System scheduler, Explore, Time configuration, Configure core features, Administer]
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

-   **[Automate generation and distribution of a report](../../reference-pages/task/schedule-report.md)**  
Generate and distribute scheduled reports via email.
-   **[Automatically generate something from a template](../../reference-pages/task/t_ScheduleTheGenerationOfAnEntity.md)**  
Schedule the generation of entities, which include changes, incidents, and CIs.
-   **[Automatically run a script of your choosing](../../reference-pages/task/t_ScheduleAScriptExecution.md)**  
Schedule both conditional and non-conditional scripts. If Domain Separation is installed in the instance, you can also select, filter, sort, and schedule scripts based on their assigned domains.
-   **[Enable run types for scheduled job child tables](customize-run-times-for-scheduled-jobs.md#)**  
The run types; **Day and Month in Year**, **Day in Week in Month in Year**, and **Week in Month**, require the fields; **Day**, **Month**, and **Year** to be visible. Child tables which don’t display those fields can't create jobs with that run type selected.

**Parent Topic:**[Scheduled jobs](../../reference-pages/concept/c_ScheduledJobs.md)

**Related topics**  


[Advanced options for scheduled jobs](advanced-options-for-scheduled-jobs.md)

[Personalize the system date format](t_PersonalizeTheSystemDateFormat.md)

[Set a system time zone](t_SetASystemTimeZone.md)

[Special cases in job schedules](../reference/r_SpecialCasesInJobSchedules.md)

[View a schedule item](t_ViewAScheduleItem.md)

