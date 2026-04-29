---
title: Email templates
description: Email templates enable administrators to create reusable content for the subject line and message body of email notifications.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Email and SMS notifications, System notifications, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Email templates

Email templates enable administrators to create reusable content for the subject line and message body of email notifications.

Templates deliver consistent information on specific system activities and improve the efficiency of creating multiple email notifications for similar actions. If necessary, you can make minor changes on the fly to an email that uses a template by overriding the subject line and message body content in the notification form. A common practice is to define the message body in a template and create new subject lines for different types of recipients. There is no limit to the number of templates that you can create.

Email templates are created in rich HTML format, and administrators have the option of converting existing email templates to rich HTML \(starting with the Eureka release\). This format provides several advantages, including:

-   Raw HTML content is converted into a WYSIWYG format.
-   The content can be edited in a feature-rich HTML editor.
-   Mail scripts are condensed into a single, easy-to-read line that can be reused in multiple email notifications.
-   To prevent broken links, images linked using URLs relative to a particular instance are converted to absolute links.

-   **[Create an email template](../task/t_CreateAnEmailTemplate.md)**  
You can create an email template with rich HTML formatting, rather than plain text.
-   **[Apply a template to an email notification](../task/t_ApplyATemplateToAnEmailNotif.md)**  
After you create an email template, you can apply it to a notification.
-   **[Convert an email template to rich HTML](../task/t_ConvertAnEmailTemplateToHTML.md)**  
If you have an email template created prior to the Eureka release, you can convert it to rich HTML.
-   **[Construct an email message with a template](../../../integrate/email-integrations/reference/r_ConstructAnEmailMessage.md)**  
Email templates provide a list of the fields from database tables that are available for constructing an email message.
-   **[Calendar integration](../reference/r_CalendarIntegration.md)**  
With email notifications, you can use import export maps to leverage information about records and integrate with Outlook or another calendar.

**Parent Topic:**[Email and SMS notifications](c_EmailNotifications.md)

**Related topics**  


[Create notification categories](../task/create-notification-categories.md)

[Create an email notification](../task/t_CreateANotification.md)

[Email notifications dashboard](email-notifications-dashboard.md)

[Email diagnostics dashboard](email-diagnostics-dashboard.md)

[Email layouts](email-layouts.md)

[Email retention](email-retention.md)

[Watermarks on notification emails](c_WorkingWithWatermarks.md)

[Parse an email thread](../task/parse-email.md)

[Email digests](email-digests.md)

[Domain separation and Notifications](domain-separation-notifications.md)

[Email FAQs and troubleshooting notification emails](troubleshooting-notification-emails.md)

