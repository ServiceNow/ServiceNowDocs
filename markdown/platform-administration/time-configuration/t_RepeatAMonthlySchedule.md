---
title: Repeat a monthly schedule
description: Repeat a monthly schedule to reduce the amount of time required to define schedules and to provide consistency in scheduling.
locale: en-US
release: xanadu
product: Time Configuration
classification: time-configuration
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Schedules, Exploring time configuration, Time configuration, Configure core features, Administer the ServiceNow AI Platform]
---

# Repeat a monthly schedule

Repeat a monthly schedule to reduce the amount of time required to define schedules and to provide consistency in scheduling.

## About this task

You can specify the following options for monthly schedules that start on a particular day of the month \(**Monthly type** is set to **Day of the month.**\). The following methods are available to compute what day of the week a monthly schedule repeats on:

-   **Day**: Calculates the day of the week to repeat on by determining the order of the selected starting date within the month. For example, if you specified that the starting date appears on the first Monday in the month, the schedule repeats every first Monday of every month.
-   **Week**: Calculates the day of the month to repeat on by determining what week number the selected starting date appears in the month. For example, if the starting date is a Monday during the second week of the month, the schedule repeats the second Monday of every month.

Use the system property **glide.schedules.repeat\_nth** to determine what method your instance uses to compute what day a repeating monthly schedule occurs on. By default, instances use the more accurate Day method.

**Note:** Use the **Week** method to maintain backwards compatibility with customized schedule logic. To learn more about calculations for the starting day of each month, for monthly schedules that start on the fifth instance of a day, see [Fifth Instance of a Day of the Week](t_FifthInstanceOfADayOfTheWeek.md).

The following example illustrates computing what day of the week a monthly schedule repeats on.

## Procedure

1.  Navigate to **sys\_properties.list**.

2.  Open the **glide.schedules.repeat\_nth** property.

3.  Verify that the **Value** is set to **day**.

4.  Navigate to **System Scheduler** &gt; **Schedules** &gt; **Schedules**, [define a new schedule](t_DefineASchedule.md), and click **Submit**.

5.  Open the new schedule and in the **Schedule Entries** related list, create a new entry with the following parameters:

    -   When: November 5, 2012 at 10:00 to November 5, 2012 at 11:00
    -   Repeats: Monthly
    -   Monthly type: Day of the Week
    -   Starting: November 5

        **Note:** In this example, November 5 is the first Monday in the month, but it is in the second week.

6.  Click **Submit**.

7.  Open **Schedule Entry**.

    **Note:** The message **Every month on the first Mon** appears on the form. The first few dates this schedule runs on are:

    -   November 5, 2012 \(First Monday of the month\)
    -   December 3, 2012 \(First Monday of the month\)
    -   January 7, 2012 \(First Monday of the month\)
8.  If you set the **Value** on the **glide.schedules.repeat\_nth** property to **week** instead of **day** in step 3, the first few dates this schedule run on are:

    -   November 5, 2012 \(Schedule starts on Monday in the second week of the month\)
    -   December 10, 2012 \(Second Monday in the month\)
    -   January 14, 2012 \(Second Monday in the month\)

**Parent Topic:**[Schedules](../concept/c_UseSchedules.md)

**Related topics**  


[Default schedules](../reference/r_DefaultSchedules.md)

[Holidays](../concept/c_Holidays.md)

[Create a holiday schedule for multiple regions](t_CreateAHolidaySchedMultiRegions.md)

[Parent and child schedules](../concept/c_ParentAndChildSchedules.md)

[Define a schedule](t_DefineASchedule.md)

[Schedule for the fifth instance of a week date](t_FifthInstanceOfADayOfTheWeek.md)

[Using schedules and calendars](../reference/r_CreateCalendarsWithSchedulePages.md)

[Domain support and schedules](../concept/domain-support-for-schedules.md)

[Schedules](../concept/c_UseSchedules.md)

[Define a schedule](t_DefineASchedule.md)

