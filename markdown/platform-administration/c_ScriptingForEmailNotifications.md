---
title: Scripting for email notifications
description: Email scripts enable you to use business rule-like scripting within an outbound email message.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [email scripts]
breadcrumb: [Create an email notification, Email and SMS notifications, System notifications, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Scripting for email notifications

Email scripts enable you to use business rule-like scripting within an outbound email message.

With mail scripts, you can dynamically change the email output of your system based on different criteria. Mail scripts enable you to perform simple tasks, such as displaying incident data, and complex ones, such as making advanced database queries.

You can use the same scripts in multiple email notifications or templates by adding an `${mail_script:script name}` embedded script tag to the body of the email notification or template, replacing script name with the name of the script you created.

If you manually enter a mail script bounded by `<mail_script>` and `</mail_script>` in the body of a new or converted email notification or template, and then attempt to save the record, a message asks whether the mail script should be converted. In many cases, an unconverted mail script fails to run from inside the HTML editor. If you select **Yes**, the script is added to the Email Script \[sys\_script\_email\] table and is automatically replaced in the body with an embedded script tag \(`${mail_script:script_name}`\).

When you manually enter a mail script enclosed in `<mail_script>` and `</mail_script>` tags in the body of a new or converted email notification or template and save the record, you will be prompted to convert the mail script.

In many cases, mail scripts that are not converted fail to run within the HTML editor. If you select **Yes**, the script is added to the Email Script \[sys\_script\_email\] table and is automatically replaced in the body with an embedded script tag \(`${mail_script:script_name}`\).

If you enter a mail script inside `${{mail_script:script name}}` and the HTML sanitizer configuration is done, the output of the mail script will be HTML sanitized. For more information about HTML sanitizer, see [HTML Sanitizer.](https://www.servicenow.com/docs/access?context=c_HTMLSanitizer&version=australia&pubname=australia-platform-security&ft:locale=en-US)

-   **[JavaScript in emails](c_UseJavaScriptInEmails.md)**  
Create mail scripts in **System Notifications** &gt; **Email** &gt; **Notification Email Script**, and refer to them by using `${mail_script:script name}` in the script field.
-   **[Mail script variables](../reference/r_MailScriptAPI.md)**  
Certain variables are available when processing mail\_script scripts.
-   **[Example scripting for email notifications](../reference/r_ExScptEmlNtfn.md)**  
Examples of scripting for email notifications.
-   **[Useful attachment scripts](../../useful-scripts/reference/r_UsefulAttachmentScripts.md)**  
This is a searchable version of the Useful Attachment Scripts.

**Parent Topic:**[Create an email notification](../../../administer/notification/task/t_CreateANotification.md)

