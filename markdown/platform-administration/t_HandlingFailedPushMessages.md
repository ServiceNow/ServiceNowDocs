---
title: Requeue failed push notification messages
description: Push notification delivery might fail for various reasons. You can view which messages failed and requeue them to be sent out if necessary.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Push notifications, System notifications, Notifications, Configure core features, Administer]
---

# Requeue failed push notification messages

Push notification delivery might fail for various reasons. You can view which messages failed and requeue them to be sent out if necessary.

## Before you begin

Role required: admin

## About this task

**Note:** There is no way for the instance to guarantee or confirm push message delivery. For more information on how Apple handles push notifications, see the [Local and Remote Notification Programming Guide](https://developer.apple.com/library/content/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/APNSOverview.html#/apple_ref/doc/uid/TP40008194-CH8-SW1) for Apple developers.

Messages can also fail to send for several reasons, such as a large message queue or other issue with the instance. You can use a [system property](../reference/r_PushNotificationProperties.md) to control how long the instance queues a push notification after it is triggered.

Push notification message payload size is limited by provider:

-   Apple iOS: 2,048 bytes
-   Google: 4,096 bytes

Your instance does not send push messages that exceed this limitation. System logs save any failed messages. For details on Apple payload limitations, see the [Local and Remote Notification Programming Guide](https://developer.apple.com/library/content/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/APNSOverview.html#/apple_ref/doc/uid/TP40008194-CH8-SW1) for Apple developers.

## Procedure

1.  Navigate to **All** &gt; **System Logs** &gt; **Push Notifications**.

    By default, the messages that were created today appear. You can change the filter if necessary. The Type column can have these values:

    -   **failure**: The message could not be sent.
    -   **pending**: The message is queued for processing.
    -   **success**: The message was successfully sent, although not necessarily received by the mobile device.
2.  Put any failed messages back into the queue to be resent by selecting the check boxes next to the failed messages, and then selecting **Re-queue failed push notifications** from the choice list.

3.  If some push notifications continue to fail, consider increasing the value in the **glide.push.notification.ttl\_seconds** property.

    See [Push notification properties](../reference/r_PushNotificationProperties.md) for more information.


**Parent Topic:**[Push notifications](../concept/c_PushNotifications.md)

**Related topics**  


[Push notification system](../reference/r_PushMessageArchitecture.md)

[Activate push notifications](t_ActivatePushNotifications.md)

[Installed with push notifications](../reference/r_InstalledWithPushNotifications.md#)

[Push notification properties](../reference/r_PushNotificationProperties.md)

[Push notification setup with the ServiceNow mobile app](../reference/r_PushNotificationSetupSN.md)

[Push notification setup with a custom push application for ServiceNow mobile apps](../reference/r_PushNotificationSetupCustom.md)

[Push notification retention](../concept/push-notification-retention.md)

