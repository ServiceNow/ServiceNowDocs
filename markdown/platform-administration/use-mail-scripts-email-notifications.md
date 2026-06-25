---
title: Use mail scripts in email notifications
description: Add dynamic content and custom logic to email notifications using mail scripts.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/use-mail-scripts-email-notifications.html
release: australia
topic_type: task
last_updated: "2026-05-04"
reading_time_minutes: 1
breadcrumb: [Scripting for email notifications, Create an email notification, Email and SMS notifications, System notifications, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Use mail scripts in email notifications

Add dynamic content and custom logic to email notifications using mail scripts.

## Before you begin

Role required: admin

## About this task

For more information on creating mail scripts, see [Notification Email Scripts](https://developer.servicenow.com/dev.do#!/learn/learning-plans/washingtondc/servicenow_administrator/app_store_learnv2_automatingapps_washingtondc_notification_email_scripts) on the developer site.

## Procedure

1.  Navigate to **All** &gt; **System Notification** &gt; **Email** &gt; **Notification Email Scripts**.

2.  Select **New** or open an existing mail script.

3.  Add the text for the message body into the script by using the `template.print()` function.

    .\[Omitted image "JavaScriptInTemplates.png"\] Alt text: Sample JavaScript template

4.  Use event parameters in the script, such as **event.parm1** and **event.parm2**, if the notification is triggered by an event.

5.  Save the mail script.

6.  Open the email notification or template where you want to use the mail script.

7.  To use an existing mail script, open the **What it will contain** tab and add the `${mail_script:script_name}` embedded script to the **Message HTML** field.

    Replace script\_name with the name of the mail script.

8.  To add a mail script inline, enter the script in the **Message HTML** field and enclose it within `<mail_script>` and `</mail_script>` tags.

9.  Save the record.

10. In the confirmation dialog box, select **Yes**.

    The script is added to the Email Script \[sys\_script\_email\] table and replaced in the body with an embedded script tag: $\{mail\_script:mail script\}.

11. Apply HTML sanitization to help avoid security concerns in your HTML content by replacing $\{mail\_script:mail script\} with `${{mail_script:mail_script}}`.

    Confirm that HTML sanitizer is enabled.

    **Note:** For more information, see [HTML Sanitizer.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/c_HTMLSanitizer.md)


**Parent Topic:**[Scripting for email notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/c_ScriptingForEmailNotifications.md)

**Related topics**  


[Mail script variables]()

[Example scripting for email notifications]()

[Useful attachment scripts]()

