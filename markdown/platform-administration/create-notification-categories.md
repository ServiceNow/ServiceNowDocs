---
title: Create notification categories
description: You can create notification categories to identify and group related notifications that are listed in the notification settings for your users.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/create-notification-categories.html
release: australia
topic_type: task
last_updated: "2026-03-12"
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

**Parent Topic:**[Email and SMS notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/c_EmailNotifications.md)

**Related topics**  


[Create an email notification]()

[Email notifications dashboard]()

[Email diagnostics dashboard]()

[Email templates]()

[Email layouts]()

[Email retention]()

[Watermarks on notification emails]()

[Parse an email thread]()

[Email digests]()

[Domain separation and Notifications]()

[Email FAQs and troubleshooting notification emails]()

