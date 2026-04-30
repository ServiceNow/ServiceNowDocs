---
title: Create personal notifications
description: Create personal notifications, which are subscriptions to notifications of importance to you. You can apply conditions that control specific content included in your personal notification, and also enable or disable the channels for delivery.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 2
breadcrumb: [Subscription-based notifications, Setting notification preferences in Core UI, Notification Preferences, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Create personal notifications

Create personal notifications, which are subscriptions to notifications of importance to you. You can apply conditions that control specific content included in your personal notification, and also enable or disable the channels for delivery.

## Before you begin

Role required: none

**Note:**

To switch to the Core UI from Next Experience, set the property **glide.ui.polaris.core.notification\_preference.enabled** to true.

## About this task

A personal notification is a subscribable notification that you can customize by adding conditions. You can assign the notification a name that is meaningful to you and filter the information received in that notification.

**Note:** Users are limited to one subscription per notification.

## Procedure

1.  Navigate to **User menu** &gt; **Preferences** &gt; **Notifications**.

2.  Select **Create Personal Notification**.

3.  Complete the New Personal Notification form \(see table\).

    |Field|Description|
    |-----|-----------|
    |Name|A descriptive name for your personal notification. Use a meaningful name to distinguish it from system notifications.|
    |Notification|The notification to subscribe to. You can subscribe only to notifications that are configured to allow subscriptions. Depending on the notification you select, the **Table**, **Affected record**, and **Send when** fields are displayed.|
    |Table|The database table that the notification is linked to.|
    |Affected record|The specific record that the notification is based on. This field appears when you select a notification that has an affected record \(for example, a notification for a problem record that has multiple affected CIs\). Click the lookup icon, select the table and specific document \(record\) in that table, and click **OK**.|
    |Send when|Another condition that must be met to send the notification. For example, you might create a filter whose conditions send notifications when an incident with a priority of **1 - Critical** is opened for a network issue.|

4.  Select **Save**.

    In the following example, notice the category in which the system placed the personal notification.

    The system creates the personal notification and adds it to the appropriate notification category.

5.  Enable or disable the channels for your personal notification.

6.  Navigate back to the list of notifications for the category by selecting the left back arrow \(**&lt;**\) at the top of the form.

    Notice that your Personal Notifications are listed above the System Notifications in the given category.

7.  Navigate back by selecting the left back arrow \(**&lt;**\) at the top of the form or by selecting the **Notifications** tab.


**Parent Topic:**[Subscription-based notifications](../concept/c_SubscriptionBasedNotifications.md)

