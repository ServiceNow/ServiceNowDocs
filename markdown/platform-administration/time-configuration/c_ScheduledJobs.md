---
title: Scheduled jobs
description: Scheduled Jobs are automated pieces of work that can be performed at a specific time or on a recurring schedule.
locale: en-US
release: zurich
product: Time Configuration
classification: time-configuration
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [System scheduler, Explore, Time configuration, Configure core features, Administer]
---

# Scheduled jobs

Scheduled Jobs are automated pieces of work that can be performed at a specific time or on a recurring schedule.

You can automate the following kinds of tasks:

-   Automatically generate and distribute a report
-   Automatically generate and schedule an entity of records, such as an incident, change item, configuration item, from a template
-   Run scheduled jobs from scripts or business rules
-   Scheduling at the end of the month
-   Scheduling for weekdays

For developer training, see [Scheduled Script Executions and Events Objectives](https://developer.servicenow.com/dev.do#!/learn/courses/washingtondc/app_store_learnv2_automatingapps_washingtondc_automating_application_logic/app_store_learnv2_automatingapps_washingtondc_scheduled_script_executions_and_events/app_store_learnv2_automatingapps_washingtondc_scheduled_script_executions_and_events_objectives) on the ServiceNow Developer Site.

Use the [System Events and Jobs Dashboard](../../platform-events/concept/track-events.md) to monitor the system event processing system and the scheduled jobs processing system.

## Scheduled job states

A scheduled job can be in any one of the following states.

-   **Ready**

    Job is ready to run at the next scheduled interval.

-   **Running**

    Job is in the process of carrying out a task.

-   **Queued**

    Job has been added to the scheduler queue and is waiting to run.

-   **Error**

    Error occurred while running the job.


## Schedule job errors

If you encounter errors generating a scheduled job, visit [Troubleshoot a scheduled job through Application Insights](../../platform-performance/task/troubleshoot-a-scheduled-job.md) for additional information.

-   **[Create a scheduled job](../../time/task/t_CreateAScheduledJob.md)**  
Create a scheduled job on the Schedule Job \[sysauto\] table.
-   **[Special cases in job schedules](../../time/reference/r_SpecialCasesInJobSchedules.md)**  
Some special cases require care in job scheduling.
-   **[View a schedule item](../../time/task/t_ViewAScheduleItem.md)**  
You can view scheduled items, which are individual instances of a scheduled job, from the system scheduler.
-   **[Advanced options for scheduled jobs](../../time/task/advanced-options-for-scheduled-jobs.md)**  
Advanced scheduling options are available when configuring Scheduled Jobs in **sysauto**, offering greater flexibility in job planning and execution. You can configure jobs to start on a future date, end on a particular date, and define how the job should repeat.

**Parent Topic:**[System scheduler](../../time/concept/c_SystemScheduler.md)

