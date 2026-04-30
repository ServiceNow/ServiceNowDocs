---
title: Send or resend reminders of an upcoming shift
description: Remind roster members of an upcoming shift by sending an email notification. You specify the number of days before their shift starts for the email.
locale: en-US
release: xanadu
product: On-Call Scheduling
classification: on-call-scheduling
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure or update an On-Call shift, Manage schedules and shifts, On-Call Scheduling, IT Service Management]
---

# Send or resend reminders of an upcoming shift

Remind roster members of an upcoming shift by sending an email notification. You specify the number of days before their shift starts for the email.

## Before you begin

Role required: rota\_admin or admin

## About this task

The reminder is sent to the email address specified in the user record, unless the address is specified in other notification preferences. Notification preferences take precedence over the user record.

## Procedure

1.  Navigate to **All** &gt; **On-Call Scheduling** &gt; **My Group Schedules**.

    The option is also available when you edit a shift in an On-Call calendar.

2.  Select the shift.

3.  On the Shift form, select the **Send on-call reminders** check box and then specify the number of days in the **Reminder lead time** field.

    **Note:** If you set the value of **Reminder lead time \(days\)** to more than one day and also set the roster to daily rotation, the instance does not send reminder emails.

4.  To resend a reminder, click **Resend**.

5.  Click **Update**.


**Parent Topic:**[Configure or update an On-Call shift](config-update-shift-oncall.md)

**Related topics**  


[Assigning On-Call Scheduling roles](../concept/roles-assigning-oncall.md)

[Manage shifts from the Calendar view](customize-calendar-view-oncall.md)

