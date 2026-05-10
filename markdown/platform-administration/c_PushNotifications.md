---
title: Push notifications
description: In addition to sending email and SMS notifications, an instance can send push notifications to mobile devices.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [System notifications, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Push notifications

In addition to sending email and SMS notifications, an instance can send push notifications to mobile devices.

A push notification is a text message that appears on a user's mobile device to alert them about something important or to ask them to perform an action. Your instance supports push notifications.

![A ServiceNow push notification](../image/example_push_notification.png "An example push notification")

Use push notifications to send messages to users when certain conditions are triggered on your instance, such as the assignment of an incident to the user. A push notification can even ask for a reply, and the instance can process the reply by acting on the related records. For example, you can have the instance send an approval request for a Change to a user. You can let the user approve or deny the Change by clicking a response button on the push notification. The user's response can then update the status of the Change record.

You can set up push notifications in a similar manner to email and SMS notifications. Determine:

-   who to send the notification to
-   when it should be sent
-   what it should contain

The ServiceNow mobile app is available as ServiceNow Classic and as Mobile Agent. By default, ServiceNow Classic supports push notifications, but you can also develop your own push application and configure your instance to send push notifications to it. For more information on setting up push notifications in Mobile Agent, go to [Mobile push notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/sg-mobile-push-notifications.md).

## Push notification setup

Push notification setup differs depending on the mobile or push application that you want your users to use. For an overview, see: [Push notification setup with a custom push application for ServiceNow mobile apps](../reference/r_PushNotificationSetupCustom.md). If you create your own application, you must understand how push notifications and the Apple Push Notification Service system work. For more information, see the APNs Overview in the[Local and Remote Notification Programming Guide](https://developer.apple.com/library/content/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/APNSOverview.html#/apple_ref/doc/uid/TP40008194-CH8-SW1) for Apple developers.

**Important:** Apple does not guarantee delivery of all push notifications. Review the Quality of Service \(QoS\) information in the [Local and Remote Notification Programming Guide](https://developer.apple.com/library/content/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/APNSOverview.html#/apple_ref/doc/uid/TP40008194-CH8-SW1) for Apple developers.

-   **[Push notification system](../reference/r_PushMessageArchitecture.md)**  
The push notification system involves several key elements that manage the delivery of push messages and push notification responses.
-   **[Activate push notifications](../task/t_ActivatePushNotifications.md)**  
Several plugins must be activated to use push notifications. If you have the Mobile UI \(com.glide.ui.m\) plugin active, push notification plugins are automatically activated.
-   **[Enable push notifications for logged-out users](../task/enable-notifications-logged-out-users.md)**  
Enable push notifications for users when they're logged out to deliver timely critical updates.
-   **[Installed with push notifications](../reference/r_InstalledWithPushNotifications.md#)**  
Several types of components are installed with the push notifications plugins.
-   **[Push notification properties](../reference/r_PushNotificationProperties.md)**  
Push notifications provides several properties to customize the setup.
-   **[Push notification setup with the ServiceNow mobile app](../reference/r_PushNotificationSetupSN.md)**  
The ServiceNow mobile application automatically enables push notifications and configures mobile devices for push notifications when users initially log in to the instance.
-   **[Push notification setup with a custom push application for ServiceNow mobile apps](../reference/r_PushNotificationSetupCustom.md)**  
If you are using your own custom mobile or push application, you must configure your app for use and set up the push contents.
-   **[Requeue failed push notification messages](../task/t_HandlingFailedPushMessages.md)**  
Push notification delivery might fail for various reasons. You can view which messages failed and requeue them to be sent out if necessary.
-   **[Push notification retention](push-notification-retention.md)**  
You can archive and eventually destroy push notifications that you no longer need or if your Push Notification table is excessively large.

**Parent Topic:**[System notifications](system-notifications-landing.md)

