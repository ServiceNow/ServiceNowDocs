---
title: JavaScript in emails
description: Create mail scripts in System Notifications Email Notification Email Script , and refer to them by using $\{mail\_script:script name\} in the script field.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Scripting for email notifications, Create an email notification, Email and SMS notifications, System notifications, Notifications, Configure core features, Administer]
---

# JavaScript in emails

Create mail scripts in **System Notifications** &gt; **Email** &gt; **Notification Email Script**, and refer to them by using `${mail_script:script name}` in the script field.

To print text into the body of the message, use the template.print\("a string"\) function.

![](../image/JavaScriptInTemplates.png "JavaScript in templates")

The **event.parm1** and **event.parm2** parameters that come from the originating event can also be used.

For additional information on creating mail scripts, see [Notification Email Scripts](https://developer.servicenow.com/dev.do#!/learn/learning-plans/washingtondc/servicenow_administrator/app_store_learnv2_automatingapps_washingtondc_notification_email_scripts) on the Developer Site.

**Parent Topic:**[Scripting for email notifications](c_ScriptingForEmailNotifications.md)

**Related topics**  


[Mail script variables](../reference/r_MailScriptAPI.md)

[Example scripting for email notifications](../reference/r_ExScptEmlNtfn.md)

[Useful attachment scripts](../../useful-scripts/reference/r_UsefulAttachmentScripts.md)

