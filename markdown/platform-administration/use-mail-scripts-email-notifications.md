---
title: Include mail scripts in email notifications
description: Include mail scripts to customize email notifications, which enable you to apply conditional logic and insert dynamic record data in your notifications.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/use-mail-scripts-email-notifications.html
release: australia
topic_type: task
last_updated: "2026-05-04"
reading_time_minutes: 1
breadcrumb: [Scripting for email notifications, Create an email notification, Email and SMS notifications, System notifications, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Include mail scripts in email notifications

Include mail scripts to customize email notifications, which enable you to apply conditional logic and insert dynamic record data in your notifications.

## Before you begin

Role required: admin

## About this task

For more information about using scripts with email notifications, see [Scripting for email notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/c_ScriptingForEmailNotifications.md) and [Notification Email Scripts](https://developer.servicenow.com/dev.do#!/learn/learning-plans/australia/servicenow_administrator/app_store_learnv2_automatingapps_australia_notification_email_scripts) on the developer site.

## Procedure

1.  Navigate to **All** &gt; **System Notification** &gt; **Email** &gt; **Notifications**.

2.  Select and open the email notification where you want to include the mail script.

3.  In the **Message HTML** field on the **What it will contain** tab, either embed an existing mail script or enter a mail script manually.

    -   To embed an existing mail script if you do not have HTML sanitizer configured, add `${mail_script:script_name}`. If you have HTML sanitizer configured, add `${{mail_script:script_name}}` to apply HTML sanitization and help avoid security concerns in your HTML content. For more information, see [Configuring HTML sanitizer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/t_ConfigureHTMLSanitizer.md).
    -   To enter a mail script manually, add the script and enclose it within the `<mail_script>` and `</mail_script>` tags.
4.  On the form header, right-click and select **Save**.

5.  If you manually added a mail script in the **Message HTML** field, select **Yes** in the configuration dialog box that appears.

    The script is added to the Email Script \[sys\_script\_email\] table and replaced in the **Message HTML** field with an embedded script tag: `${mail_script:script_name}`.


## Mail scripts embedded in an email notification

\[Omitted image "example-mail-script-notification.png"\] Alt text: Message HTML field displaying mail script tags in an email notification

**Parent Topic:**[Scripting for email notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/c_ScriptingForEmailNotifications.md)

**Related topics**  


[Mail script variables]()

[Example scripting for email notifications]()

[Useful attachment scripts]()

