---
title: Email layouts
description: Create reusable content for the message body of email templates.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Email and SMS notifications, System notifications, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Email layouts

Create reusable content for the message body of email templates.

![Sample Email Layout record for Demo Layout - Go to Instance Button. This record consists of a single column HTML table with rows for a header, body, button, and footer.](../image/email-layout-overview.png "Email layout overview")

Administrators can use email layouts to:

-   Ensure all email notifications have a consistent layout such as always displaying a header, body, and footer.
-   Display static content on all email notifications such as a company logo or a background.
-   Declare inline styles available for use in the message body of an email template such as setting a text font, size, and color.
-   Provide users with links to common response actions such as unsubscribe from a notification or manage notification preferences.

**Note:** To display dynamic content such as mail scripts, use email templates. For more information, see [Create an email template](../task/t_CreateAnEmailTemplate.md).

Email layouts insert HTML elements into the message body of email templates. Any style elements you define in the email layout are available to the email template. Email layouts support style sheets in these formats.

-   Internal style sheets defined within a `<style>` element.
-   Inline styles within a `style` attribute.

By default, the system includes several sample layouts administrators can use to create their own layouts. Administrators can create email layouts using an inline HTML editor or manually entering HTML code. The system stores email layout records in the Email Layout \[sys\_email\_layout\] table.

**Note:** If there is no content in the notification from either the notification record or the template, the layout won't be applied.

-   **[Create an email layout](../task/create-email-layout.md)**  
Create an email layout to specify the HTML content you want to appear in the body of one or more email templates.

**Parent Topic:**[Email and SMS notifications](c_EmailNotifications.md)

**Related topics**  


[Create notification categories](../task/create-notification-categories.md)

[Create an email notification](../task/t_CreateANotification.md)

[Email notifications dashboard](email-notifications-dashboard.md)

[Email diagnostics dashboard](email-diagnostics-dashboard.md)

[Email templates](c_EmailTemplates.md)

[Email retention](email-retention.md)

[Watermarks on notification emails](c_WorkingWithWatermarks.md)

[Parse an email thread](../task/parse-email.md)

[Email digests](email-digests.md)

[Domain separation and Notifications](domain-separation-notifications.md)

[Email FAQs and troubleshooting notification emails](troubleshooting-notification-emails.md)

