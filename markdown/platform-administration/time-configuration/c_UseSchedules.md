---
title: Schedules
description: Use schedules to specify when service level agreements or inactivity monitors are active, or to specify when on-call rotations should take effect. Schedules are rules that include or exclude time for various actions or tasks.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/time-configuration/c\_UseSchedules.html
release: australia
product: Time Configuration
classification: time-configuration
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Explore, Time configuration, Configure core features, Administer the ServiceNow AI Platform]
---

# Schedules

Use schedules to specify when service level agreements or inactivity monitors are active, or to specify when on-call rotations should take effect. Schedules are rules that include or exclude time for various actions or tasks.

For example, if a service level agreement is set to an 8-5 Weekdays schedule, the SLA only counts time during those hours. Generate and validate schedules in the **System Scheduler** &gt; **Schedules** menu.

-   **[Default schedules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/time-configuration/r_DefaultSchedules.md)**  
Default schedules are available in a base system.
-   **[Holidays](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/time-configuration/c_Holidays.md)**  
You can define each individual holiday as a schedule entry to create exceptions to existing schedules.
-   **[Create a holiday schedule for multiple regions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/time-configuration/t_CreateAHolidaySchedMultiRegions.md)**  
You can create holiday schedules for multiple regions that follow the same work schedule but have different holidays.
-   **[Parent and child schedules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/time-configuration/c_ParentAndChildSchedules.md)**  
Schedules can have one of two parent-child relationships with other schedules.
-   **[Define a schedule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/time-configuration/t_DefineASchedule.md)**  
Configure schedules using schedule and schedule entry records.
-   **[Schedule for the fifth instance of a week date](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/time-configuration/t_FifthInstanceOfADayOfTheWeek.md)**  
You can select a date that computes to the fifth instance of a weekday for a date near the end of a month for a repeating monthly schedule,
-   **[Repeat a monthly schedule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/time-configuration/t_RepeatAMonthlySchedule.md)**  
Repeat a monthly schedule to reduce the amount of time required to define schedules and to provide consistency in scheduling.
-   **[Using schedules and calendars](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/time-configuration/r_CreateCalendarsWithSchedulePages.md)**  
Specific applications within the ServiceNow AI Platform generate graphical calendar displays based on schedule pages.
-   **[Domain support and schedules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/time-configuration/domain-support-for-schedules.md)**  
Domain separation is supported in schedules. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data. Activate the Domain Support \[com.glide.domain\] plugin to enable the domain separation functionality for schedules.

**Parent Topic:**[Exploring time configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/time-configuration/exploring-time-configuration.md)

