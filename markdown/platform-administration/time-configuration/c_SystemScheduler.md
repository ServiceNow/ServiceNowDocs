---
title: System scheduler
description: The System Scheduler application contains two separate engines for scheduling: the Scheduled Jobs engine and the Schedules engine.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/time-configuration/c\_SystemScheduler.html
release: australia
product: Time Configuration
classification: time-configuration
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Explore, Time configuration, Configure core features, Administer the ServiceNow AI Platform]
---

# System scheduler

The System Scheduler application contains two separate engines for scheduling: the Scheduled Jobs engine and the Schedules engine.

## Scheduled jobs

Scheduled Jobs executes any work that must be performed at a specific time, or on a recurring basis. The Scheduled Jobs module links to the Schedule \[sys\_trigger\] table. Manipulating records on the Schedule table is not recommended. Use this table to view existing base system scheduled jobs.

The Scheduled Jobs module in System Definition is an admin-friendly interface for scheduling work. Use this module to create new scheduled jobs. For more information, see [Create a Scheduled Job](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/time-configuration/t_CreateAScheduledJob.md).

## Schedules

Schedules are rules that include or exclude time on a calendar. They are used by service levels, inactivity monitor, and group on-call rotation. For instance, you can define a schedule to restrict service levels to only apply to weekdays during business hours. You can also exclude holidays from an on-call rotation.

For more information, see [Use Schedules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/time-configuration/c_UseSchedules.md).

-   **[Event scheduling](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/time-configuration/c_ScheduleEvents.md)**  
You can use various tools for scheduling actions or tasks to happen in the future.
-   **[Scheduled jobs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/time-configuration/c_ScheduledJobs.md)**  
Scheduled Jobs are automated pieces of work that can be performed at a specific time or on a recurring schedule.

**Parent Topic:**[Exploring time configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/time-configuration/exploring-time-configuration.md)

