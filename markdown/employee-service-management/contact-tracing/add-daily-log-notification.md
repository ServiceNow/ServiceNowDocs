---
title: Configure an email notification for the daily contact log
description: Configure a custom email notification to use with Emergency Outreach notifications so you can request that users submit a list of other users they came in contact with throughout the workday.
locale: en-US
release: zurich
product: Contact Tracing
classification: contact-tracing
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Setting up Contact Tracing, Contact Tracing, Safe Workplace, Health and Safety, Employee Service Management]
---

# Configure an email notification for the daily contact log

Configure a custom email notification to use with Emergency Outreach notifications so you can request that users submit a list of other users they came in contact with throughout the workday.

## Before you begin

Review the existing **Employee Daily Log Alert** and **Daily Contact Log Notification** email notifications to familiarize yourself with the base scripts and settings.

Role required: admin

## About this task

When you configure an email notification for use as a daily contact log, you are creating a customized email notification for contact tracing purposes. The **Employee Daily Log Alert** and **Daily Contact Log Notification** are email notifications you can review for a better understanding on how notifications similar to the one you might create are configured.

## Procedure

1.  Navigate to **All** &gt; **System Notifications** &gt; **Email** &gt; **Notifications**.

2.  Click **New**.

3.  In the **Name** field, enter a descriptive name for the notification.

4.  In the **Table** field, select the Daily Log Acknowledgements \[sn\_imt\_tracing\_daily\_log\_acknowledgement\] table.

5.  On the **When to send** tab, set the conditions.

    -   Enter conditions in the condition builder to define when users are sent the email notification.
    -   Copy the following example script in the **Advanced condition** field and make these modifications.
        -   Give the variable a different name, for example, *employeeCheckInAcmeSysId*.
        -   Enter the new notification sys\_id as the value.
        -   Enter the variable name that you declared at the end of the second line.
    Example Advanced condition script:

    ```
    var employeeCheckInAcmeSysId = '<replace with this notification sys_id';
    answer = current.employee_check_in.notification == employeeCheckInAcmeSysId
    
    ```

6.  On the **Who will receive** tab, select from **Users** and **Groups** to determine who will receive the notification.

7.  Complete the remaining information on the **What it will contain** tab.

<table id="table_u5n_3gx_gqb"><thead><tr><th>

Field

</th><th>

Action

</th></tr></thead><tbody><tr><td>

Email template

</td><td>

Select the email template used to determine any pre-configured content within the subject line and message body.

</td></tr><tr><td>

Subject

</td><td>

Create the subject line that users see when they receive the email.

</td></tr><tr><td>

Message HTML

</td><td>

In the **Message HTML** field, add and customize the text or source code of the message to meet your organization's needs.**Note:** While entering the email content in the **Message HTML** field, make sure that you include the link to the Daily Contact Log form.

</td></tr></tbody>
</table>8.  Click **Submit**.

9.  In the Notifications list, open the notification that you added and click **Preview Notification**.

10. Review the notification and make any changes required.

11. Click **Update**.


## Result

You created a custom email notification for use as daily contact log with Emergency Outreach notifications. When you modify or create an Emergency Outreach notification, you can select this notification for the Daily Contact Log or custom outreaches.

## What to do next

To use this email notification for as your daily contact log, see [Configure an Emergency Outreach notification for the daily contact log](configure-outreach-notif-daily-log.md).

**Parent Topic:**[Setting up Contact Tracing](../concept/set-up-contact-tracing.md)

