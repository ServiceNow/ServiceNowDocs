---
title: Holidays
description: You can define each individual holiday as a schedule entry to create exceptions to existing schedules.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/time-configuration/c\_Holidays.html
release: australia
product: Time Configuration
classification: time-configuration
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Schedules, Explore, Time configuration, Configure core features, Administer the ServiceNow AI Platform]
---

# Holidays

You can define each individual holiday as a schedule entry to create exceptions to existing schedules.

For instance, if an SLA requires an incident be resolved within three business days excluding Christmas, create a schedule entry for Christmas. Creating this entry ensures that the SLAs do not count Christmas when calculating elapsed time, even if it falls within the work week.

Because schedules can be included in other schedules through a parent-child relationship, it is also possible to create a holiday schedule and include it in other schedules to keep holidays consistent. The following example shows a holiday schedule.

\[Omitted image "ScheduleUSHolidays.png"\] Alt text:

The following example shows a schedule that includes the preceding holiday schedule.

\[Omitted image "ScheduleWithChildSchedule.png"\] Alt text:

**Parent Topic:**[Schedules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/time-configuration/c_UseSchedules.md)

**Related topics**  


[Default schedules]()

[Create a holiday schedule for multiple regions]()

[Parent and child schedules]()

[Define a schedule]()

[Schedule for the fifth instance of a week date]()

[Repeat a monthly schedule]()

[Using schedules and calendars]()

[Domain support and schedules]()

[Schedules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/time-configuration/c_UseSchedules.md)

[Define a schedule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/time-configuration/t_DefineASchedule.md)

