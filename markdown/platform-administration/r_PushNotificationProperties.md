---
title: Push notification properties
description: Push notifications provides several properties to customize the setup.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Push notifications, System notifications, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Push notification properties

Push notifications provides several properties to customize the setup.

Add these properties to the System Properties \[sys\_properties\] table.

-   **__glide.push.apns.version__**

    Controls which version of the Apple Push Notification service \(APNs\) to use in your instance. You can use APNs version 1 or 2. The system uses APNs version 2 by default. To use APNs version 1 instead, set the value to **1**.

    -   Type: integer
    -   Default value: 2
-   **__glide.push.debug__**

    Creates entries in the system log for push notification errors.

    -   Type: true \| false
    -   Default value: false
-   **__glide.push.enabled__**

    Enables or disables push notifications.

    -   Type: true \| false
    -   Default value: true
-   **__glide.push.feedback.debug__**

    Creates entries in the system log for feedback sent by the APNs for custom iOS push applications.

    -   Type: true \| false
    -   Default value: false
-   **__glide.push.notification.ttl\_seconds__**

    Specifies the number of seconds after which a queued push notification expires. After a push notification is triggered, it is queued and finally processed by a scheduled job. If the time the notification sits in the queue exceeds this value, the notification is not sent. Check the [Push Notifications log](../task/t_HandlingFailedPushMessages.md) for more information.

    -   Type: integer
    -   Default value: 21600

**Parent Topic:**[Push notifications](../concept/c_PushNotifications.md)

**Related topics**  


[Push notification system](r_PushMessageArchitecture.md)

[Activate push notifications](../task/t_ActivatePushNotifications.md)

[Enable push notifications for logged-out users](../task/enable-notifications-logged-out-users.md)

[Installed with push notifications](r_InstalledWithPushNotifications.md#)

[Push notification setup with the ServiceNow mobile app](r_PushNotificationSetupSN.md)

[Push notification setup with a custom push application for ServiceNow mobile apps](r_PushNotificationSetupCustom.md)

[Requeue failed push notification messages](../task/t_HandlingFailedPushMessages.md)

[Push notification retention](../concept/push-notification-retention.md)

