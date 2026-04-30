---
title: Create notification categories
description: You can create notification categories to identify and group related notifications that are listed in the notification settings for your users.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Email and SMS notifications, System notifications, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Create notification categories

You can create notification categories to identify and group related notifications that are listed in the notification settings for your users.

## Before you begin

Role required: admin

## About this task

Before adding new categories, review the base system notification categories in the Notification Categories \[sys\_notification\_category\] table to determine if you need a new category.

## Procedure

1.  Navigate to **All** &gt; **System Notification** &gt; **Email** &gt; **Notification Categories**.

2.  Select **New**.

3.  Enter the **Name** of the category to identify the family of notifications.

    Provide a category name that is meaningful to your users, so that they can easily find their notifications under the appropriate category in their notification settings.

4.  Enter a **Short description** to identify the category.

5.  Select **Submit**.


## Result

The system adds the new category to the Notification Categories \[sys\_notification\_category\] table. After you create at least one, active notification that uses the new category, the category and notification are listed in the Notification preferences for users \(**User Menu** &gt; **Preferences** &gt; **Notifications** &gt; **System Notifications**\).

**Parent Topic:**[Email and SMS notifications](../concept/c_EmailNotifications.md)

**Related topics**  


[Create an email notification](t_CreateANotification.md)

[Email notifications dashboard](../concept/email-notifications-dashboard.md)

[Email templates](../concept/c_EmailTemplates.md)

[Email layouts](../concept/email-layouts.md)

[Email retention](../concept/email-retention.md)

[Watermarks on notification emails](../concept/c_WorkingWithWatermarks.md)

[Parse an email thread](parse-email.md)

[Email digests](../concept/email-digests.md)

[Domain separation and Notifications](../concept/domain-separation-notifications.md)

[Email FAQs and troubleshooting notification emails](../concept/troubleshooting-notification-emails.md)

