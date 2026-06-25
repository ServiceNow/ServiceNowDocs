---
title: Parent and child schedules
description: Schedules can have one of two parent-child relationships with other schedules.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/time-configuration/c\_ParentAndChildSchedules.html
release: australia
product: Time Configuration
classification: time-configuration
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Schedules, Explore, Time configuration, Configure core features, Administer the ServiceNow AI Platform]
---

# Parent and child schedules

Schedules can have one of two parent-child relationships with other schedules.

-   **Parent field**

    When a schedule record lists a value for the **Parent** field, schedule entries from the parent schedule apply to both the parent schedule and the child schedule. By default, there are no sample schedules that use the **Parent** field.

-   **Child schedule**

    When a schedule record has one or more child schedules in the **Child Schedules** related list, schedule entries from the child schedule apply to the containing schedule. By default, there are several sample schedules that use child schedules. For example, see the **8-5 weekdays excluding holidays** schedule that includes the **U.S. Holidays** schedule.


Parent and child schedules cannot contain conflicting schedule entry types. For example, a schedule containing maintenance schedule entries cannot also contain blackout schedule entries. Nor can a maintenance schedule have a child schedule containing blackout schedule entries.

**Note:** To create a Holiday schedule and include it in a parent schedule, you must add it as a child schedule and with an Include type.

Parent schedules must have at least one entry that is not an **Excluded** type. If parent schedules are only exclusionary, they are invalid.

**Note:** The **Show Schedule** related link shows schedule entries from the current schedule and the child schedule record. For example, when showing the **8-5 weekdays excluding holidays** schedule, holidays are also shown as excluded because the holiday schedule is a child schedule.

**Parent Topic:**[Schedules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/time-configuration/c_UseSchedules.md)

**Related topics**  


[Default schedules]()

[Holidays]()

[Create a holiday schedule for multiple regions]()

[Define a schedule]()

[Schedule for the fifth instance of a week date]()

[Repeat a monthly schedule]()

[Using schedules and calendars]()

[Domain support and schedules]()

[Schedules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/time-configuration/c_UseSchedules.md)

[Define a schedule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/time-configuration/t_DefineASchedule.md)

