---
title: Schedule entry fields
description: You can only associate a schedule entry with one schedule. The Schedule Entries related list contains the definitions of the time periods you want to include in or exclude from the schedule.
locale: en-US
release: zurich
product: Time Configuration
classification: time-configuration
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Define a schedule, Schedules, Explore, Time configuration, Configure core features, Administer]
---

# Schedule entry fields

You can only associate a schedule entry with one schedule. The **Schedule Entries** related list contains the definitions of the time periods you want to include in or exclude from the schedule.

<table id="table_tq3_h4w_bp"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name for the schedule entry.

</td></tr><tr><td>

Type

</td><td>

Label that describes the purpose of the schedule. The system also uses the schedule type to determine how to process certain schedules.-   **Excluded**: Excludes time periods from SLA counts.
-   **Maintenance**: Specifies time periods where change management activities are allowed. A schedule containing maintenance schedule entries cannot also contain blackout schedule entries.
-   **Blackout**: Excludes time periods from change management schedules. A schedule containing blackout schedule entries cannot also contain maintenance schedule entries.

</td></tr><tr><td>

Show As

</td><td>

Option that indicates how the schedule entry should appear in calendar applications and how it should interact with other schedule entries.-   **Busy**: Schedule entry is not available for scheduling a work task.
-   **At no extra charge**: Schedule entry is available for scheduling a work task.
-   **Tentative**: Schedule entry is tentatively available for scheduling a work task.
-   **On call**: Schedule entry is on call, which provides a means to determine which member of a user group is available to complete a task.

</td></tr><tr><td>

When

</td><td>

Date and time to which the schedule entry applies. If the schedule entry applies to a full 24-hour day, select the **All day** check box.**Note:** Changing the global date and time format in the **glide.sys.date\_format** System Properties setting has significant impact on schedule calculations made when you select the **All day** check box. To learn more, see [Global date and time field format](r_FormatDateAndTimeFields.md).

</td></tr><tr><td>

Repeats

</td><td>

Repetition interval for the schedule entry, if any. If you select a repetition interval, other fields appear so you can further specify the repeat interval.

</td></tr><tr><td>

Repeat every

</td><td>

Scheduling repetition frequency - weekly, monthly, or yearly. This field is only visible when the **Repeats** field has a value of **Daily**, **Weekly**, **Monthly**, or **Yearly**.

</td></tr><tr><td>

Repeat on

</td><td>

Days of the week a weekly schedule repeats on. This field is only visible when the **Repeats** field has a value of **Weekly**.

</td></tr><tr><td>

Monthly type

</td><td>

[Monthly schedule repetition frequency](../task/t_RepeatAMonthlySchedule.md). This field is only visible when the **Repeats** field has a value of **Monthly**. Monthly repeat options include:-   Repeat on a specific day of the month
-   Repeat on a specific day in a specific week of the month
-   Repeat on the last day of the month
-   Repeat on a specific weekday in the last week of the month

</td></tr><tr><td>

Yearly type

</td><td>

Yearly schedule repetition frequency. This field is only visible when the **Repeats** field has a value of **Yearly**. Yearly repeat options include:-   Repeat on a specific day of the year
-   Repeat on a floating day

</td></tr><tr><td>

Float week

</td><td>

Week of the month a floating yearly schedule repeats on. This field is only visible when the **Yearly type** field has a value of **Floating**.

</td></tr><tr><td>

Float day

</td><td>

Day of the week a floating yearly schedule repeats on. This field is only visible when the **Yearly type** field has a value of **Floating**.

</td></tr><tr><td>

Month

</td><td>

Month of the year a floating yearly schedule repeats on. This field is only visible when the **Yearly type** field has a value of **Floating**.

</td></tr><tr><td>

Repeat until

</td><td>

Repetition end date. If you leave this field blank, the schedule repeats indefinitely.

</td></tr><tr><td>

Type

</td><td>

\[Optional\] Schedule entry description.

</td></tr></tbody>
</table>**Parent Topic:**[Define a schedule](../task/t_DefineASchedule.md)

**Related topics**  


[Schedules](../concept/c_UseSchedules.md)

[Define a schedule](../task/t_DefineASchedule.md)

