---
title: Configure a roster
description: Edit a roster to specify its reminder and escalation settings and to identify a subset of group members to participate in the On-Call roster.
locale: en-US
release: xanadu
product: On-Call Scheduling
classification: on-call-scheduling
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configure or update an On-Call shift, Manage schedules and shifts, On-Call Scheduling, IT Service Management]
---

# Configure a roster

Edit a roster to specify its reminder and escalation settings and to identify a subset of group members to participate in the On-Call roster.

## Before you begin

Role required: rota\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **On-Call Scheduling** &gt; **On-Call Calendars**.

2.  Right-click a shift and select **Edit Shift** from the **Actions** list.

3.  In the **Rosters** related list, select a roster and then fill the form.

<table id="table_cqt_yjf_2gb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the roster.

</td></tr><tr><td>

Shift

</td><td>

Shift associated with the current roster.

</td></tr><tr><td>

Active

</td><td>

If selected, the roster is active for on-call operations.

</td></tr><tr><td>

Order

</td><td>

Order of the roster.

</td></tr><tr><td>

Rotation interval

</td><td>

Type of the rotation interval.

</td></tr><tr><td>

Day of week for rotation

</td><td>

Weekday on which the roster rotation should start. When this field is specified, roster rotation happens based on the specified frequency and the weekday.**Note:** This field is displayed only if the **Rotation interval** field is set to **Weekly**.

</td></tr><tr><td>

Rotate every

</td><td>

Frequency of the rotation interval.

</td></tr><tr><td>

Rotation start date

</td><td>

Start date of the rotation.

</td></tr><tr><td>

Rotation start time

</td><td>

Start time of the rotation.

</td></tr><tr><td>

All day rotation

</td><td>

If selected, roster rotation happens throughout the day.To specify a particular time of day for roster rotation, for example 08:00 instead of midnight, deselect the check box and specify the time.

</td></tr><tr><td class="sub-head" colspan="2">

Escalation Settings

</td></tr><tr><td>

\# reminders

</td><td>

Number of times that reminders are sent to a user who does not reply within the time frame defined in **Time between reminders**.

</td></tr><tr><td>

Time between reminders

</td><td>

Time between each reminder.

</td></tr><tr><td>

Time before escalation

</td><td>

Values in the**Number of reminders** and **Time between reminders** fields determine the value in the **Time before escalation** field. For example, if **Number of reminders** is 2 and **Time between reminders** is 10 minutes, then the **Time before escalation** is 30 minutes. That is, the time that passes between the first notification of a non-responsive roster member and the first notification of the next member in the escalation path.

</td></tr><tr><td class="sub-head" colspan="2">

Reminder Communication

</td></tr><tr><td>

Send on-call reminders

</td><td>

If selected, a reminder is sent to the email address specified in the user record, unless it is specified somewhere else in the notification preferences. Notification preferences take precedence over the user record.

</td></tr><tr><td>

Reminder lead time \(days\)

</td><td>

Lead time for email reminders.**Note:** This field is displayed only when the **Send On-Call Reminders** check box is selected.

</td></tr></tbody>
</table>4.  Click **Update**.

    **Note:**

    -   Initially, roster members are automatically populated from the user group.
    -   All members of a roster must be members of the same user group.

**Parent Topic:**[Configure or update an On-Call shift](config-update-shift-oncall.md)

**Related topics**  


[Escalation and reminder settings for rosters](../reference/escalation-remind-settings-oncall.md)

