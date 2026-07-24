---
title: Send email to remind users to enroll for Password Reset
description: You can automatically send messages that remind users to enrolled in the Password Reset process. You specify the text of the message and can configure the messages to repeat at intervals.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/password-reset/config-pwd-reset-enroll-reminder.html
release: australia
product: Password Reset
classification: password-reset
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure your Password Reset process, Configuring Password Reset, Password Reset, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Send email to remind users to enroll for Password Reset

You can automatically send messages that remind users to enrolled in the Password Reset process. You specify the text of the message and can configure the messages to repeat at intervals.

## Before you begin

Role required: password\_reset\_admin

## About this task

The default email content is:

-   Subject: Reminder: Enroll in the Password Reset program
-   Body: Click here to enroll in the Password Reset program.

To customize the email, see [Customize the Password Reset enrollment reminder email](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/password-reset/customize-pwd-reset-enroll-reminder.md).

## Procedure

1.  Navigate to **All** &gt; **Password Reset** &gt; **Processes** and select your process.

2.  Click the **Enrollment Reminder** tab, configure the following settings, and then click **Update**.

    **Note:** The tab appears only when the **Password reset** check box is selected.

<table id="table_ocm_jbg_wbb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Send reminder

</td><td>

Select the check box to send reminder emails to users \(either all users or users in the specified groups, as you configured\). Clear the check box to send no reminders.

</td></tr><tr><td>

Sender alias

</td><td>

Enter a non-functional email alias that should appear in both the **To** and **From** fields of the message. For example, `do-not-reply@myCompany.com`. Users will not be able to respond to the alias.The alias is required by the email system to use the **bcc** field for all of the users who receive the message. The intent is that the users should not see the other addressees.

 Default: do-not-reply@ServiceNow.com

</td></tr><tr><td>

Send, Day, and Time

</td><td>

Specify a schedule of one message each month or one message each week. -   If you set **Send** to **Monthly**, then enter the day of the month and optionally the time of day when the message should be sent.
-   If you set **Send** to **Weekly**, then enter the day of the week and optionally the time of day when the message should be sent.
 Default: Weekly message at 00:00 on Monday

</td></tr><tr><td>

Starting

</td><td>

Date and time to send the first message. Click the calendar button to specify the setting.

 Default: \[Now\]

</td></tr></tbody>
</table>
-   **[Customize the Password Reset enrollment reminder email](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/password-reset/customize-pwd-reset-enroll-reminder.md)**  
 The email message that reminds users to enroll for the Password Reset process is based on an email template. To customize the message, you can modify the default template or create a custom template.

**Parent Topic:**[Configure your Password Reset process](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/password-reset/t_CreateAPasswordResetProcess.md)

**Related topics**  


[Calculating the security score for password reset process]()

[Configure password expiration reminder]()

[Credential stores for Password Reset]()

[Password Reset verifications]()

[Configure your Password Reset process to auto-enroll users]()

[Enable users to enroll for Password Reset]()

[Configure Password Reset properties]()

[Configure the required strength for passwords]()

[Specify lockout for failed login attempts]()

[Configure Google reCAPTCHA for the password reset process]()

