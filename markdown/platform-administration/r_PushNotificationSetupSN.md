---
title: Push notification setup with the ServiceNow mobile app
description: The ServiceNow mobile application automatically enables push notifications and configures mobile devices for push notifications when users initially log in to the instance.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Push notifications, System notifications, Notifications, Configure core features, Administer]
---

# Push notification setup with the ServiceNow mobile app

The ServiceNow mobile application automatically enables push notifications and configures mobile devices for push notifications when users initially log in to the instance.

**Note:** Push notifications with the ServiceNow mobile application are not supported in on-premise instances.

Setting up push notifications involves both the system administrator and users.

-   Admin creates or updates push notifications for the ServiceNow mobile app. The admin does not need to set up the mobile devices for users nor update their user preferences for receiving push notifications.
-   Users install the ServiceNow mobile mobile on their iOS or Android mobile devices and set their preferences for receiving notifications on the ServiceNow mobile app.

![Push notification setup tasks for the ServiceNow mobile app](../image/PushNotificationSNSetup.png "Push notification setup tasks for the ServiceNow mobile app")

## What to do — admins

Admins create push notifications, similar to setting up email notifications. A push notification has two main parts: the push message and the notification, which includes the push message.

**Note:** The push message and notification must be for the same table.

-   **Create the push message**

    Before creating a push notification, create the [push message](../task/t_CreateAPushMessage.md) with the actual message content \(JSON payload\) to be included in the push notification.

-   **Create the push notification that includes the push message**

    Create the [push notification](../task/t_CreatePushNotification.md) that includes the push message and message content. A push notification specifically sends the push message. You can update a standard platform notification and use it as a push notification that includes the push message.

-   **Add the new push notification to the Push Default Registration table**

    To ensure that a new push notification is included and enabled in the notification preferences of your users, [register a new push notification](../task/add-push-notif-reg-table.md) in the Push Default Registration table. The notification is listed in the notification preferences of your users the next time that they log in to the ServiceNow mobile app.


## What to do — ServiceNow mobile app users

-   **Download the ServiceNow mobile app**

    Install the ServiceNow mobile app on an iOS or Android mobile device.

-   **Agree to accept push notifications**

    After installing the ServiceNow mobile app, users are asked to accept push notifications. When the instance receives the push notification acceptance message from a user, it creates a record in the Push Notification Installations \[sys\_push\_notif\_app\_install\] table. This record is what the instance uses to identify the device + mobile application combination necessary to identify a push notification recipient.

    The device then performs the following actions:

    -   Obtains a token that identifies the device.
    -   Triggers the creation of the device in the user notification preferences.
-   **Log in to the company instance from the ServiceNow mobile app**

    Logging in automatically subscribes users to the push-specific notifications registered in the Push Default Registration table.

-   **Update preferences for receiving notifications on the ServiceNow mobile app**

    Users can enable and disable through **Notification Settings** in the ServiceNow mobile app. They can set additional notification preferences, such as conditions or filters that affect notification delivery, by using the System Settings window on a desktop or mobile browser. For details, see [Setting notification preferences in Core UI](../concept/user-notification-preferences.md).


## Next steps

If you are an admin, review the base system notifications and determine if new [push message content](../task/t_CreateAPushMessage.md) and [push notifications](../task/t_CreatePushNotification.md) are needed.

