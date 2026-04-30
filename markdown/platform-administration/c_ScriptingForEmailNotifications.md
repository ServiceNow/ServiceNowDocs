---
title: Scripting for email notifications
description: Email scripts allow for business rule-like scripting within an outbound email message.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
keywords: [email scripts]
breadcrumb: [Create an email notification, Email and SMS notifications, System notifications, Notifications, Configure core features, Administer]
---

# Scripting for email notifications

Email scripts allow for business rule-like scripting within an outbound email message.

With mail scripts, you can dynamically change the email output of your system based on different criteria. Mail scripts allow you to perform simple tasks, such as displaying incident data, and complex ones, such as making advanced database queries.

You can add a `${mail_script:script name}` embedded script tag to the body of the email notification or template, replacing script name with the name of the script you created. This makes it easy to use the same scripts in multiple email notifications or templates.

If you manually enter a mail script bounded by `<mail_script>` and `</mail_script>` in the body of a new or converted email notification or template, and then attempt to save the record, a message asks whether the mail script should be converted. In many cases, an unconverted mail script fails to run from inside the HTML editor. If you select **Yes**, the script is added to the Email Script \[sys\_script\_email\] table and is automatically replaced in the body with an embedded script tag \(`${mail_script:script_name}`\).

-   **[JavaScript in emails](c_UseJavaScriptInEmails.md)**  
Create mail scripts in **System Notifications** &gt; **Email** &gt; **Notification Email Script**, and refer to them by using `${mail_script:script name}` in the script field.
-   **[Mail script variables](../reference/r_MailScriptAPI.md)**  
Certain variables are available when processing mail\_script scripts.
-   **[Example scripting for email notifications](../reference/r_ExScptEmlNtfn.md)**  
Examples of scripting for email notifications.
-   **[Useful attachment scripts](../../useful-scripts/reference/r_UsefulAttachmentScripts.md)**  
This is a searchable version of the Useful Attachment Scripts.

**Parent Topic:**[Create an email notification](../../../administer/notification/task/t_CreateANotification.md)

