---
title: System and custom notification and delivery channel preferences in Next Experience
description: You can manage and set your own notification preferences, including customized notifications and channels for receiving them.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Notification Preferences, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# System and custom notification and delivery channel preferences in Next Experience

You can manage and set your own notification preferences, including customized notifications and channels for receiving them.

With notification preferences, you can control the system notifications and custom notifications that you receive and apply conditions to restrict notification delivery and choose how the notifications are delivered to you.

You can also search for notifications under both system and custom notifications.

## System notifications

System notifications alert you of record changes that might concern or interest you. You can be notified via email, SMS text messages, push notifications, or messaging applications.

With system notifications, you can:

-   Set your preferences for specific notifications by searching in the list of your notifications or by filtering them by category.
-   Set preferences at a global level.
-   Easily enable or disable all notifications or individual notifications.
-   Add or modify a notification schedule for individual delivery channels for each system notification.
-   Set a schedule for all notifications, individual system notifications, or delivery channels.

    For more information, see [Apply notification conditions](../task/apply-notification-conditions.md)


## Custom notifications

A custom notification is a system notification that you can subscribe to and customize by adding conditions.

With custom notifications, you can:

-   Search for a specific notification in the list of your notifications to be able to set your preferences for that notification.
-   Create and modify custom notifications, which are subscriptions to notifications that are important to you.
-   Set preferences at a global level.
-   Easily enable or disable all notifications or individual notifications.
-   Enable or disable notification channels.
-   Add or modify a notification schedule for individual delivery channels for each system notification.
-   Set a schedule for all notifications, individual system notifications, or delivery channels.

    For more information, see [Apply notification conditions](../task/apply-notification-conditions.md)


**Note:**

Custom notifications for Next Experience do not support notifications that require a related affected record. For these notifications, you have to set the preference in the Core UI. For more information, see [Setting notification preferences in Core UI](user-notification-preferences.md).

**Note:** Subscription-based notifications are not domain aware and cannot support domain-specific settings.

## Delivery Channels

Delivery channels is a list of your chosen channels such as email, SMS, instant message and voice channels for receiving notifications.

With Delivery Channels, you can:

-   Enable or disable a particular channel for receiving notifications.
-   Create, edit, or delete notification channels for instant messages, email, SMS, and voice.

    **Note:** Only admins can delete channels from the cmn\_notif\_device table.

-   Choose how notifications are delivered.
-   Set a schedule for the record in the channel and apply to the notifications you want to receive.

-   **[Set notification preferences](../task/set-notification-preferences.md)**  
View, enable, and disable general settings for notification preferences, and delivery channels.
-   **[Customize system notifications](../task/create-custom-notifications.md)**  
Create custom notifications, which are subscriptions to notifications of importance to you, and apply conditions that control specific content included in your custom notification. You can also enable or disable the channels for delivery.
-   **[Modify a notification](../task/modify-notification-schedule.md)**  
Modify a notification by establishing a schedule or setting conditions to control the notifications you receive.
-   **[Delete a custom notification](../task/delete-custom-notifications.md)**  
Delete custom notifications that you don't need any more.
-   **[Add a new notification delivery channel](../task/add-email-device.md)**  
Add new channels for email, instant message, SMS, and voice to receive notifications and set a schedule for the channel for the notifications you want to receive.
-   **[Edit a delivery channel](../task/edit-or-delete-a-channel.md)**  
Edit an email, instant message, SMS, or voice channel for receiving notifications, and schedule when the channel can receive notifications.

**Parent Topic:**[Notification Preferences](preferences-landing.md)

