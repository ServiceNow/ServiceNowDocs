---
title: Schedule for the fifth instance of a week date
description: You can select a date that computes to the fifth instance of a weekday for a date near the end of a month for a repeating monthly schedule,
locale: en-US
release: australia
product: Time Configuration
classification: time-configuration
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Schedules, Explore, Time configuration, Configure core features, Administer the ServiceNow AI Platform]
---

# Schedule for the fifth instance of a week date

You can select a date that computes to the fifth instance of a weekday for a date near the end of a month for a repeating monthly schedule,

## About this task

Three options are available for handling months that do not have a matching Fifth instance of the selected day.

-   Last: Selects the last instance of the weekday in the month.
-   Next: Selects the first instance of the weekday in the next month.
-   Strict: Skips any month without a matching Fifth instance and selects only months that have a matching Fifth instance.

Use the **glide.schedules.fifth** system property to control how a schedule entry that selects the fifth occurrence of a weekday behaves in months containing only four occurrences of that day.

-   Use of this property is only valid when the **glide.schedules.repeat\_nth** property is set to **Day**.
-   The following example illustrates computing what day of the month a schedule repeats on when the schedule starts on the Fifth instance of a weekday in the month.

## Procedure

1.  Navigate to **sys\_properties.list**.

2.  Open the **glide.schedules.fifth** property.

3.  Verify that the **Value** is set to **last**.

4.  Navigate to **System Scheduler** &gt; **Schedules** &gt; **Schedules**, [define a new schedule](t_DefineASchedule.md), and click **Submit**.

5.  Open the new schedule and in the **Schedule Entries** related list, create a new entry with the following parameters:

    -   When: November 29, 2012 at 10:00 to November 29, 2012 at 11:00
    -   Repeats: Monthly
    -   Monthly type: Day of the Week
    -   Starting: November 29

        **Note:** In this example, November 29 is the fifth Thursday in the month.

6.  Click **Submit**.

7.  Open the same schedule entry.

    **Note:** The message **Every month on the Fifth Thu** appears on the form.

    The schedule for the first three months is computed as:

    -   November 29, 2012 \(Fifth Thursday of the month\)
    -   December 27, 2012 \(Last Thursday of the month\)
    -   January 31, 2013 \(Fifth Thursday of the month\)
8.  If you set the **Value** on the **glide.schedules.fifth** property to **next** instead of **last** in step 3, the schedule for the first three months is computed as:

    -   November 29, 2012 \(Fifth Thursday of the month\)
    -   January 3, 2012 \(First Thursday of the next month since December 2012 does not have five Thursdays\)
    -   January 31, 2013 \(Fifth Thursday of the month\)
9.  If the **Value** on the **glide.schedules.fifth** property is set to strict instead of **last** in step 3, the schedule for the first three months is computed as:

    -   November 29, 2012 \(Fifth Thursday of the month\)
    -   No meeting \(December 2012 skipped because it does not have five Thursdays\)
    -   January 31, 2013 \(Fifth Thursday of the month\)

**Parent Topic:**[Schedules](../concept/c_UseSchedules.md)

**Related topics**  


[Default schedules](../reference/r_DefaultSchedules.md)

[Holidays](../concept/c_Holidays.md)

[Create a holiday schedule for multiple regions](t_CreateAHolidaySchedMultiRegions.md)

[Parent and child schedules](../concept/c_ParentAndChildSchedules.md)

[Define a schedule](t_DefineASchedule.md)

[Repeat a monthly schedule](t_RepeatAMonthlySchedule.md)

[Using schedules and calendars](../reference/r_CreateCalendarsWithSchedulePages.md)

[Domain support and schedules](../concept/domain-support-for-schedules.md)

[Schedules](../concept/c_UseSchedules.md)

[Define a schedule](t_DefineASchedule.md)

[Repeat a monthly schedule](t_RepeatAMonthlySchedule.md)

