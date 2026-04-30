---
title: Schedule fields
description: The Schedule form contains the following fields.
locale: en-US
release: yokohama
product: Time Configuration
classification: time-configuration
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Define a schedule, Schedules, Exploring time configuration, Time configuration, Configure core features, Administer the ServiceNow AI Platform]
---

# Schedule fields

The Schedule form contains the following fields.

<table id="table_ffs_l3w_bp"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name for the schedule.

</td></tr><tr><td>

Time Zone

</td><td>

Time zone for the schedule. If you select **Floating**, the time zone is relative to whatever process is accessing the item at the time. -   For example, if a resource manager in Amsterdam sets a floating schedule for 8:00A.M. to 5:00P.M., a user in San Jose sees the schedule as 8:00 A.M. to 5:00 P.M.
-   When a schedule is defined in a specific time zone, users in different time zones see the schedule with their own time zone applied.

</td></tr><tr><td>

Parent

</td><td>

Parent schedule that constraints the new schedule.

</td></tr><tr><td>

Application

</td><td>

Application scope of the schedule.

</td></tr><tr><td>

Type

</td><td>

Text label that describes the purpose of the schedule. You can also use one of these system terms to determine how to process certain schedules: -   **Excluded**: Excludes time periods from SLA counts.
-   **Maintenance**: Specifies time periods where change management activities are allowed. A schedule containing maintenance schedule entries cannot also contain blackout schedule entries.
-   **Blackout**: Excludes time periods from change management schedules. A schedule containing blackout schedule entries cannot also contain maintenance schedule entries.

</td></tr><tr><td>

Description

</td><td>

Description of the schedule.

</td></tr></tbody>
</table>**Parent Topic:**[Define a schedule](../task/t_DefineASchedule.md)

**Related topics**  


[Schedules](../concept/c_UseSchedules.md)

[Define a schedule](../task/t_DefineASchedule.md)

