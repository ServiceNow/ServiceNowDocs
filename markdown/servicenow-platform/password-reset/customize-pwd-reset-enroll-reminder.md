---
title: Customize the Password Reset enrollment reminder email
description: The email message that reminds users to enroll for the Password Reset process is based on an email template. To customize the message, you can modify the default template or create a custom template.
locale: en-US
release: yokohama
product: Password Reset
classification: password-reset
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Send email to remind users to enroll for Password Reset, Configure your Password Reset process, Configure, Password Reset, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Customize the Password Reset enrollment reminder email

The email message that reminds users to enroll for the Password Reset process is based on an email template. To customize the message, you can modify the default template or create a custom template.

## Before you begin

Role required: password\_reset\_admin

## About this task

The default email content is:

-   Subject: Reminder: Enroll in the Password Reset program
-   Body: Click here to enroll in the Password Reset program.

## Procedure

1.  To modify the email subject text:

    1.  Navigate to **System Policy** &gt; **Email** &gt; **Templates**.

    2.  Open the **Password reset enrollment reminder** template.

    3.  Update the **Subject** field as needed.

    4.  In the **Message HTML** text box, you can add code as needed, but do not modify the default text.

2.  To modify the email body content:

    1.  Navigate to **System Notifications** &gt; **Email** &gt; **Notification Email Scripts**.

    2.  Open the **pwd.enrollment\_reminder** script.

    3.  Modify only the indicated portion of the script.

    ![Text to edit in the enrollment reminder script](../image/enrollment_reminder-script.png)

3.  To create a custom email template:

    1.  Make a copy of the **Password reset enrollment reminder** template and edit as described above.

    2.  Navigate to **Password Reset** &gt; **Properties** and enter the template name in the **Email template for enrollment reminder emails** field.


**Parent Topic:**[Send email to remind users to enroll for Password Reset](config-pwd-reset-enroll-reminder.md)

