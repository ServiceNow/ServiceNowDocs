---
title: Password Expiration Configuration form
description: The Password Expiration Configuration form allows you to define how frequently users must update their passwords and receive reminder notifications before expiration.
locale: en-US
release: australia
product: Password Reset
classification: password-reset
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Password Reset reference, Password Reset, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Password Expiration Configuration form

The Password Expiration Configuration form allows you to define how frequently users must update their passwords and receive reminder notifications before expiration.

## Access the Password Expiration Configuration form

To access the **Password Expiration Configuration** form, navigate to **All** &gt; **System Properties** &gt; **Password Expiration**.

<table id="table_gr2_vhw_rsb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Days password is valid

</td><td>

The number of days that you want a password to be set as valid.

 The default value is **90**.

</td></tr><tr><td>

Days prior to start reminders

</td><td>

The number of days required to send notifications before password expiration. For example, if you set it to 5 days, a notification is sent 5 days prior to password expiration.

 The default value is **10**.

</td></tr><tr><td>

Schedule Frequency

</td><td>

Frequency to send reminders, such as daily or periodically. The default value is **Daily**.

 If you select **Periodically**, then notifications are sent based on the period, for example, alternate days or once in three days.

</td></tr><tr><td>

Time zone

</td><td>

The time zone to send reminders.

</td></tr><tr><td>

Time

</td><td>

The time when you want reminder notifications to be sent.

</td></tr><tr><td>

Repeat Interval

</td><td>

The days and the time that you want to use to send reminders with a specific interval. For example, when you enter 2 days and time, the notification is sent alternate days on the time you specified.

 This field appears only when **Periodically** is selected from the **Schedule Frequency** field.

</td></tr><tr><td>

Start time

</td><td>

The time when you want a notification reminder to be started.

</td></tr></tbody>
</table>