---
title: Subscription-based notifications
description: Subscription-based notifications enable users to proactively subscribe to items that interest them and unsubscribe from messages that are not mandatory.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-administration/ai-platform-administration/c\_SubscriptionBasedNotifications.html
release: zurich
product: AI Platform Administration
classification: ai-platform-administration
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Preferences in Core UI, Notification Preferences, Notifications, Configure core features, Administer]
---

# Subscription-based notifications

Subscription-based notifications enable users to proactively subscribe to items that interest them and unsubscribe from messages that are not mandatory.

Users can also specify additional notification channels that each of their notifications can be configured to use.

Before users can manage the notifications that are sent to them, administrators must create email notifications to which users can subscribe. Administrators can also make subscription-based notifications mandatory so users cannot unsubscribe to them. Then users can subscribe or unsubscribe to the notifications, and add schedules and filters to the subscription to limit the notifications that can be received.

Notifications that administrators mark as subscribable are automatically available in user notification settings. Users are limited to one subscription per notification.

Administrators should create subscription-based notifications when they do not want to specify users for a notification and want to let users proactively subscribe to the notification.

**Note:** Subscription-based notifications are not domain aware and cannot support domain-specific settings.

## Subscriptions 2.0 plugin

The Subscription Based Notifications 2.0 plugin must be active to use subscribable notifications. This plugin is active by default on all new and upgraded instances.

The plugin installs the Notification Subscription \[sys\_notif\_subscription\] table, which holds user subscriptions to all notifications.

## Subscriptions and notification preferences

Users can subscribe to notifications available to them through their notification preferences. In the Core UI interface, all users can set and modify their notification preferences through the **Notifications** tab of the System Settings window.

-   **[Create personal notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-platform-administration/create-personal-notifications.md)**  
Create personal notifications, which are subscriptions to notifications of importance to you. You can apply conditions that control specific content included in your personal notification, and also enable or disable the channels for delivery.
-   **[Create a service provider](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-platform-administration/t_CreateAServiceProvider.md)**  
Administrators can configure service providers for devices that use SMS.
-   **[Make a notification mandatory](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-platform-administration/t_MakingANotificationMandatory.md)**  
To prevent users from turning off or deleting a subscription to a notification, make the notification mandatory.
-   **[Force a notification to be sent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-platform-administration/t_ForcingANotificationToBeSent.md)**  
To force a notification to be sent to the specified users, enable forced delivery.
-   **[Create a notification filter](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-platform-administration/t_NotificationFilters.md)**  
Notification filters enable a user to control the delivery of messages by creating special conditions on multiple tables in a single, reusable filter.

**Parent Topic:**[Setting notification preferences in Core UI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-platform-administration/user-notification-preferences.md)

