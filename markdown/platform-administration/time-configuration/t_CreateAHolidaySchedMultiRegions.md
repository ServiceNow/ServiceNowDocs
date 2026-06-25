---
title: Create a holiday schedule for multiple regions
description: You can create holiday schedules for multiple regions that follow the same work schedule but have different holidays.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/time-configuration/t\_CreateAHolidaySchedMultiRegions.html
release: australia
product: Time Configuration
classification: time-configuration
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Schedules, Explore, Time configuration, Configure core features, Administer the ServiceNow AI Platform]
---

# Create a holiday schedule for multiple regions

You can create holiday schedules for multiple regions that follow the same work schedule but have different holidays.

## About this task

The following method supports multiple regions with the same work schedule \(for example, an 8-5 weekdays schedule\) but with different holiday schedules.

## Procedure

1.  Create a holiday schedule for each region. For example, U.S. Holidays, British Holidays, and Australian Holidays.

2.  Add the work schedule as a child schedule to each region's holiday schedule.

    This method requires making &lt;number of schedules&gt; + 1 total schedules. If you make the regional holiday schedule a child schedule of the work hours schedule, you must create a separate work hours schedule for each region. The total number of schedules in this case is &lt;number of schedules&gt; x two schedules.


**Parent Topic:**[Schedules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/time-configuration/c_UseSchedules.md)

**Related topics**  


[Default schedules]()

[Holidays]()

[Parent and child schedules]()

[Define a schedule]()

[Schedule for the fifth instance of a week date]()

[Repeat a monthly schedule]()

[Using schedules and calendars]()

[Domain support and schedules]()

[Schedules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/time-configuration/c_UseSchedules.md)

[Define a schedule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/time-configuration/t_DefineASchedule.md)

