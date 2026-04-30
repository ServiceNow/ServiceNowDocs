---
title: Configure the lead time for email reminders
description: On-Call Scheduling includes a scheduled job that checks if any shift members should be notified about upcoming On-Call commitments. Modify the lead time for the reminder to be sent.
locale: en-US
release: yokohama
product: On-Call Scheduling
classification: on-call-scheduling
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure or update an On-Call shift, Manage schedules and shifts, On-Call Scheduling, IT Service Management]
---

# Configure the lead time for email reminders

On-Call Scheduling includes a scheduled job that checks if any shift members should be notified about upcoming On-Call commitments. Modify the lead time for the reminder to be sent.

## Before you begin

Role required: rota\_manager or rota\_admin

## Procedure

1.  Navigate to **All** &gt; **On-Call Scheduling** &gt; **On-Call Calendars**.

2.  Right-click the shift and select **Edit Shift**.

3.  Update the **Reminder lead time \(days\)** value for the on-call schedule record or for any of its rosters.

    The reminder lead time defined on a roster is always respected. If no lead time is defined, the instance uses the schedule reminder lead time. If the reminder lead time is not defined for either the schedule or its rosters, then the instance uses a default of 2 days.

    **Note:** The **Reminder lead time** on the Roster form is different from the **\# reminders** and **Time between reminders** values in the Escalation Settings section of the form.

    The escalation settings are used only to configure reminders for escalations. The **Reminder lead time** is in the Reminder Communication section of the Roster form, and is used to email reminders for upcoming on-call commitments.


**Parent Topic:**[Configure or update an On-Call shift](config-update-shift-oncall.md)

