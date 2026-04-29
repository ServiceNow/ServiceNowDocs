---
title: Send or resend reminders of an upcoming shift
description: Remind roster members of an upcoming shift by sending an email notification. You specify the number of days before their shift starts for the email.
locale: en-US
release: australia
product: On-Call Scheduling
classification: on-call-scheduling
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure or update an On-Call shift, Managing schedules and shifts, On-Call Scheduling, IT Service Management]
---

# Send or resend reminders of an upcoming shift

Remind roster members of an upcoming shift by sending an email notification. You specify the number of days before their shift starts for the email.

## Before you begin

Role required: rota\_admin or admin

## About this task

The reminder is sent to the email address specified in the user record, unless the address is specified in other notification preferences. Notification preferences take precedence over the user record.

For all major on-call shift email notifications, you can now decide where the links to an on-call shift records are redirected. Instead of an on-call shift record automatically opening in the classic UI16 interface in On-Call Scheduling, the record can be opened in SOW. The on-call shift record link in an email notification opens in SOW only if the following conditions are met:

-   The **Redirect SOW Email notification** \(**sow\_email\_notification\_redirect**\) property is set to `true`.
-   The **Redirect SOW Email notification for On-call scheduling** \(**sow\_email\_notification\_redirect.on\_call**\) property is set to `true`.
-   You have the sn\_sow\_user role.

The ITSM Notifications Redirection \(com.snc.itsm.notifications\_redirection\) plugin is installed and activated automatically to support this behavior.

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

