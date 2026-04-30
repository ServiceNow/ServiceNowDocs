---
title: Email and SMS notifications
description: Use email notifications to send selected users email or SMS notifications about specific activities in the system, such as updates to incidents or change requests.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [System notifications, Notifications, Configure core features, Administer]
---

# Email and SMS notifications

Use email notifications to send selected users email or SMS notifications about specific activities in the system, such as updates to incidents or change requests.

**Important:** Service providers such as AT&amp;T and Verizon may soon be deprecating the **email-to-text** functionality. See [Using Notify with SMS](https://www.servicenow.com/docs/access?context=c_NotifySMS&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US) for SMS delivery.

Email notifications allow administrators to specify:

-   When to send the notification
-   Who receives the notification
-   What content is in the notification
-   Whether the notification can be delivered in an [email digest](email-digests.md) and if so, the digest content

Additional email notification options are available. You can [subscribe to notifications](c_SubscriptionBasedNotifications.md), and administrators can make some [notifications mandatory](../task/t_MakingANotificationMandatory.md).

Administrators also have the option of converting existing email notifications to a rich HTML format. This format provides several advantages, including:

-   Raw HTML content is converted into a WYSIWYG format.
-   The content can be edited in a feature-rich HTML editor.
-   Mail scripts are condensed into a single, easy-to-read line that can be reused in multiple email notifications.
-   To avoid broken links, items like images and incidents, that are linked with URLs relative to an instance are converted to absolute links. For example, if an incident is linked using a relative URL, the link is converted to an absolute link.

**Note:** The rich HTML format is the default for all new email notifications.

**Note:** Instances can’t send or receive encrypted email messages. The system strips out the body of the encrypted email because it can’t process the encrypted content in plain text or HTML.

An email notification can also send as an SMS notification if the recipient has subscribed to the notification on an SMS channel. The system uses the subject line of the email notification and converts it to an SMS message. If the administrator doesn't want to use the email notification subject for the SMS notification, they can define an alternate SMS message in the email template form or email notification form. For more information, see [Create an email notification](../task/t_CreateANotification.md).

For more information on creating an SMS channel, see [Create notification channels](../task/create-channel.md).

For more information on setting up SMS notification see [KB0712569](https://support.servicenow.com/nav_to.do?uri=%2Fkb%3Fid%3Dkb_article_view%26sysparm_article%3DKB0712569).

If you want to change how the instance processes incoming email, see [Inbound email actions](c_InboundEmailActions.md). See [System email log and mailboxes](../../time/reference/r_EmailLogs.md) for examples of messages the system displays when notifications or inbound email actions aren’t processed.

-   **[Create notification categories](../task/create-notification-categories.md)**  
You can create notification categories to identify and group related notifications that are listed in the notification settings for your users.
-   **[Create an email notification](../task/t_CreateANotification.md)**  
Create an email notification specifying when to send it, who receives it, what it contains, and if it can be delivered in an email digest.
-   **[Email notifications dashboard](email-notifications-dashboard.md)**  
The email notification dashboard provides visibility into key metrics and enables admins to configure the dashboard to enable access to other users.
-   **[Email diagnostics dashboard](email-diagnostics-dashboard.md)**  
The email diagnostics dashboards provide visibility in to email delivery metrics that can help in improving the email health by identifying errors and areas that need deeper investigation.
-   **[Email templates](c_EmailTemplates.md)**  
Email templates enable administrators to create reusable content for the subject line and message body of email notifications.
-   **[Email layouts](email-layouts.md)**  
Create reusable content for the message body of email templates.
-   **[Email retention](email-retention.md)**  
You can archive and eventually destroy email messages that you no longer need or if your Email table is excessively large.
-   **[Watermarks on notification emails](c_WorkingWithWatermarks.md)**  
By default, a unique watermark label will be generated at the bottom of each notification email to allow matching incoming email to existing records.
-   **[Parse an email thread](../task/parse-email.md)**  
When an email is received, parse the most recent message in an email thread by creating **Email Reply Separators** using specified string or regular expressions.
-   **[Email digests](email-digests.md)**  
An email digest is a single email that summarizes the activity for a selected notification and its target records during a specified time interval. You can enable an email digest to reduce the number of notifications received when frequent updates to the associated records occur within a short time period.
-   **[Domain separation and Notifications](domain-separation-notifications.md)**  
Domain separation is supported in the Notifications application. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
-   **[Email FAQs and troubleshooting notification emails](troubleshooting-notification-emails.md)**  
Logs and diagnostics are provided to help determine whether notification emails are being sent and received successfully, what any issues are, and who receives the email.

**Parent Topic:**[System notifications](system-notifications-landing.md)

