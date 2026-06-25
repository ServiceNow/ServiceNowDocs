---
title: Advanced options for scheduled jobs
description: Advanced scheduling options for scheduled jobs support greater flexibility in job planning and execution. You can configure jobs to start on a future date, end on a particular date, and define how the job should repeat.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/time-configuration/advanced-options-for-scheduled-jobs.html
release: australia
product: Time Configuration
classification: time-configuration
topic_type: concept
last_updated: "2026-05-13"
reading_time_minutes: 4
keywords: [scheduled jobs, advanced scheduling, repeat interval, starting ending fields]
breadcrumb: [Scheduled jobs, System scheduler, Explore, Time configuration, Configure core features, Administer the ServiceNow AI Platform]
---

# Advanced options for scheduled jobs

Advanced scheduling options for scheduled jobs support greater flexibility in job planning and execution. You can configure jobs to start on a future date, end on a particular date, and define how the job should repeat.

When the **Run** field is set to one of the following values, an **Advanced** option displays on the scheduled job form:

-   Daily: Runs daily, at a designated time.
-   Day and Month in Year: Runs yearly on a specific day and month \(for example, July 14\), at a designated time.
-   Day in Week in Month in Year: Runs yearly on a specific day of the week in a specific week of a specific month \(for example, the second Monday in October\), at a designated time.
-   Monthly: Runs on a monthly basis, at a designated time and day of the month.
-   Periodically: Runs on a designated repeating interval.
-   Week in Month: Runs monthly during a specific week of the month \(for example, the third week of each month\), on designated days and at a designated time.
-   Weekly: Runs on a weekly basis, at a designated time and day of the week.

If you select the **Advanced** option, the following advanced fields display on the form:

-   Starting: Specifies the beginning of a window in the future within which the job starts running. The **Time** field determines the actual start time in the window.
-   Ending: Specifies the ending of a window in the future within which the job stops running. The **Time** field determines the actual stop time in the window.
-   Repeat every: Enables custom recurrence patterns. For example, a daily job that repeats every two days or a weekly job that repeats every three weeks.

    **Note:** The **Repeat every** field isn't supported with the Day and Month in Year and Day in Week in Month in Year run types.


## Starting and Ending fields

The Scheduled Job \[sysauto\] table has multiple **Starting** and **Ending** fields. Each field behaves differently depending on whether a time zone is selected in the **Time zone** field.

|Column name|Column label|When used|Behavior|
|-----------|------------|---------|--------|
|run\_start|Starting|No time zone selected|Stores the value you enter directly. The job starts at the entered time in the time zone of the user who runs the job. By default, the user who creates the job is the user who runs the job.|
|entered\_run\_start|Starting|Time zone selected|Uses the value you enter and the selected time zone to automatically calculate the value of the other **Starting** \[run\_start\] field by converting your entered time to the equivalent local time as displayed in the UI.|
|run\_end|Ending|No time zone selected|Stores the value you enter directly. The job stops at the entered time in the time zone of the user who runs the job. By default, the user who creates the job is the user who runs the job.|
|entered\_run\_end|Ending|Time zone selected|Uses the value you enter and the selected time zone to automatically calculate the value of the other **Ending** \[run\_end\] field by converting your entered time to the equivalent local time as displayed in the UI.|

When setting the **Starting** and **Ending** fields, follow these guidelines based on your time zone selection:

-   Time zone selected: In the **Time zone** field, select a time zone, and then enter your desired starting and ending times in the **Starting** \[entered\_run\_start\] and **Ending** \[entered\_run\_end\] fields. The system automatically calculates the values of the other **Starting** \[run\_start\] and **Ending** \[run\_end\] fields.
-   No time zone selected: In the **Time zone** field, select **-- None --**, and then enter your desired starting and ending times in the **Starting** \[run\_start\] and **Ending** \[run\_end\] fields. The job runs in the time zone of the user who runs the job.

**Note:** If you select a time zone, you must enter the starting and ending times after setting the **Time zone** field otherwise the times might be reset.

## Daily scheduled job with no time zone

The following example of a daily job illustrates the behavior of the **Starting**, **Ending**, and **Repeat every** fields. The daily job has the following schedule:

-   Starting: June 1 at 00:00
-   Ending: June 30 at 23:59
-   Time: 9:00 a.m.
-   Repeat every: 1 day

Although the job is scheduled to start on June 1 at 00:00, it doesn't run at that time. Instead, the job first runs at 9:00 a.m. on June 1 because that is the specified run time. The starting and ending times define the window of time during which the job is set to run. The first valid scheduled run within that window is when the job will run, in this case at 9:00 a.m. on June 1. When creating scheduled job records, if the value of the **Starting** field is empty, the system uses the current time.

If you change the value of the **Repeat every** field to 2, the job runs every 2 days at 9:00 a.m. starting on June 1. That means it runs on June 1, June 3, June 5, and so on, continuing every other day until June 29—the last occurrence before the ending time of June 30 at 23:59.

**Parent Topic:**[Scheduled jobs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/time-configuration/c_ScheduledJobs.md)

**Related topics**  


[Scheduled jobs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/time-configuration/c_ScheduledJobs.md)

[Create a scheduled job](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/time-configuration/t_CreateAScheduledJob.md)

[Enable run types for scheduled job child tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/time-configuration/customize-run-times-for-scheduled-jobs.md)

