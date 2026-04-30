---
title: Configuring Email as a notification channel for Proactive Engagement
description: Email notification is one of the notification channel along with Desktop assistant and Virtual agent when you choose self-help instructions or URL as the resolution type.
locale: en-US
release: xanadu
product: Proactive Engagement
classification: proactive-engagement
topic_type: concept
last_updated: "2025-04-23"
reading_time_minutes: 1
breadcrumb: [Configuring Proactive Engagement, Proactive Engagement, IT Service Management]
---

# Configuring Email as a notification channel for Proactive Engagement

Email notification is one of the notification channel along with Desktop assistant and Virtual agent when you choose self-help instructions or URL as the resolution type.

Email notification is the new notification channel supported for the self-help instructions and URL resolution type. To enable email notification channel as an option in SOW and in core UI, mark the Active field True in the `sn_pren_channel_configuration` table.

Once email notification is chosen while setting the engagement settings, a new field, Choose email notification is enabled, this field helps you choose the email template. Proactive engagement notification option is the out of box email notification template created in the `sysevent_email_action` table. You can customize the email template according to the required subject, email body, and so on. To customize the email subject, use the field issue reference name from the issue registry template `sn_pren_issue_registry_template]`. Leverage the out of the box platform capability to configure and send an email notification. The created experience issue is automatically set to closed complete once the notification is sent. For more information on how to configure an email template and set up the notification, see the links in the related information. For more information on creating an email notification, template and layouts see, [Email and SMS notifications](https://www.servicenow.com/docs/access?context=c_EmailNotifications&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

**Parent Topic:**[Configuring Proactive Engagement](../configuring-proactive-engagement.md)

