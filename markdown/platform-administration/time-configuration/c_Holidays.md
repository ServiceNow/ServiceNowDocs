---
title: Holidays
description: You can define each individual holiday as a schedule entry to create exceptions to existing schedules.
locale: en-US
release: yokohama
product: Time Configuration
classification: time-configuration
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Schedules, Exploring time configuration, Time configuration, Configure core features, Administer the ServiceNow AI Platform]
---

# Holidays

You can define each individual holiday as a schedule entry to create exceptions to existing schedules.

For instance, if an SLA requires an incident be resolved within three business days excluding Christmas, create a schedule entry for Christmas. Creating this entry ensures that the SLAs do not count Christmas when calculating elapsed time, even if it falls within the work week.

Because schedules can be included in other schedules through a parent-child relationship, it is also possible to create a holiday schedule and include it in other schedules to keep holidays consistent. The following example shows a holiday schedule.

![](../image/ScheduleUSHolidays.png "US Holidays")

The following example shows a schedule that includes the preceding holiday schedule.

![](../image/ScheduleWithChildSchedule.png "Child Schedule")

**Parent Topic:**[Schedules](c_UseSchedules.md)

**Related topics**  


[Default schedules](../reference/r_DefaultSchedules.md)

[Create a holiday schedule for multiple regions](../task/t_CreateAHolidaySchedMultiRegions.md)

[Parent and child schedules](c_ParentAndChildSchedules.md)

[Define a schedule](../task/t_DefineASchedule.md)

[Schedule for the fifth instance of a week date](../task/t_FifthInstanceOfADayOfTheWeek.md)

[Repeat a monthly schedule](../task/t_RepeatAMonthlySchedule.md)

[Using schedules and calendars](../reference/r_CreateCalendarsWithSchedulePages.md)

[Domain support and schedules](domain-support-for-schedules.md)

[Schedules](c_UseSchedules.md)

[Define a schedule](../task/t_DefineASchedule.md)

