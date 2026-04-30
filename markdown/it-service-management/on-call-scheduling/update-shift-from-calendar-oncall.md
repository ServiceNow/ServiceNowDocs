---
title: Update shift details from the On-Call calendar
description: To save time, update shift details directly from an on-call calendar.
locale: en-US
release: zurich
product: On-Call Scheduling
classification: on-call-scheduling
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure or update an On-Call shift, Manage schedules and shifts, On-Call Scheduling, IT Service Management]
---

# Update shift details from the On-Call calendar

To save time, update shift details directly from an on-call calendar.

## Before you begin

Role required: rota\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **On-Call Scheduling** &gt; **On-Call Calendars**.

2.  In the title bar, click the toggle filters icon ![Configuration icon](../image/ONC_SettingsIcon.png) and select a user group.

3.  Click the shift name on the calendar.

    A dialog box displays the **Actions** list and information about the primary and secondary rosters. For each listed user, you have an option to either connect through phone, email, or chat. The application that is launched for phone or email is dependent on the client that is installed in the local machine.

4.  Navigate to **Actions** &gt; **Edit Shift**.

<table id="table_bv2_vww_khb"><thead><tr><th>

Question

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The name of the shift.

</td></tr><tr><td>

Group

</td><td>

Select **Yes**, and then select one of the predefined options in the next question. Select **No** to set up the schedule's configuration manually.

</td></tr><tr><td>

Active

</td><td>

Shows the state of the shift

</td></tr><tr><td>

Schedule

</td><td>

The shift is a part of this schedule. Choose from a predefined list of schedules using the lookup if you want to change the schedule. Click the calendar to view the complete schedule.

</td></tr><tr><td>

Based on

</td><td>

The template that the schedule is based on

</td></tr><tr><td>

Background Color

</td><td>

Use this field to specify the background color of the shift or to change from an existing color. Differentiate between groups with the colors.

</td></tr><tr><td>

Catch All

</td><td>

Specify who should receive notifications in case none of the people who are on-call accepted the incident assignment. It can be none, a group manager, a shift manager, an individual, or any or all roster members. -   Select **Notify Individual** to specify a member of the group to notify.
-   Select **Notify All** to specify a shift. All shift members are notified.


</td></tr><tr><td>

Manager

</td><td>

The user with the shift manager \[rota\_admin\] role.

</td></tr><tr><td>

Override user preference

</td><td>

User preferences are overridden with contact preferences when set to true.

</td></tr><tr><td>

Send On-Call Reminders

</td><td>

If selected, on-call reminders are sent.

</td></tr><tr><td>

Reminder lead time \(days\)

</td><td>

Lead time for email reminders.**Note:** This field is displayed only when the **Send On-Call Reminders** check box is selected.

</td></tr><tr><td>

Coverage interval

</td><td>

Update interval for the subscribed calendar: Weekly or daily coverage details.

</td></tr><tr><td>

Get coverage for

</td><td>

Number of weeks or days for which you want to update the subscribed calendar.

</td></tr></tbody>
</table>
**Parent Topic:**[Configure or update an On-Call shift](config-update-shift-oncall.md)

