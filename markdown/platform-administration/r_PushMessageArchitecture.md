---
title: Push notification system
description: The push notification system involves several key elements that manage the delivery of push messages and push notification responses.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Push notifications, System notifications, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Push notification system

The push notification system involves several key elements that manage the delivery of push messages and push notification responses.

-   **Customer instance**

    Your ServiceNow instance.

-   **Push proxy**

    An instance that collects all push notifications that go to the ServiceNow Classic mobile application and forwards them to the ServiceNow applications for Apple iOS or Android. If you create a custom push application, you do not use the push proxy.

-   **Push provider**

    The provider of push messages, which is the Apple Push Notification service \(APNs\) or Firebase Cloud Messaging \(FCM\) service, for the ServiceNow Classic mobile app or custom mobile apps.

-   **Push application on a mobile device**

    The application, such as the ServiceNow Classic mobile application. You can also build and customize your own push application.


## Push notification process

The push notification process is as follows:

1.  Activity on the instance triggers a push notification.
2.  The instance looks for who to send the notification to and checks the user notification preferences to find their push device settings.
3.  The instance sends the push notification to the push notification service, either the Apple Push Notification service \(APNs\) or Firebase Cloud Messaging \(FCM\) service. If you are using the ServiceNow Classic mobile app, the instance sends the notification through a push proxy instance, which then forwards the notification to the APNs or FCM service.
4.  The push notification service sends the notification to the user's push application. When the instance sends the notification to the push notification service, it includes message content along with the instance name and ID. This information ensures that a response to the notification is sent back to the correct instance. If the user can reply to the notification, such as sending an approval to a change request, the response is sent via REST message back to the instance.
5.  The instance identifies a script to run to handle the response.
6.  The script performs an action on the instance, such as marking a change request approved. If there is invalid JSON or if the script fails, an error response is sent back to the device.



## Push notification responses

With custom push applications, you can have your users act on records in the instance by responding to a push notification.

The actions that they can take are defined in a script that you associate with the notification message. The response is sent to the instance in this format:

```
https://{instance_name}/api/now/v1/push/{application Name}/action/{action}
```

The application name is the push application the user is using. The application name must match the application name in the Push Application \[sys\_push\_application\] table. The action is the Sys ID of the action in the Push Notifications Actions \[sys\_push\_notif\_act\_script\] table.

**Parent Topic:**[Push notifications](../concept/c_PushNotifications.md)

**Related topics**  


[Activate push notifications](../task/t_ActivatePushNotifications.md)

[Installed with push notifications](r_InstalledWithPushNotifications.md#)

[Push notification properties](r_PushNotificationProperties.md)

[Push notification setup with the ServiceNow mobile app](r_PushNotificationSetupSN.md)

[Push notification setup with a custom push application for ServiceNow mobile apps](r_PushNotificationSetupCustom.md)

[Requeue failed push notification messages](../task/t_HandlingFailedPushMessages.md)

[Push notification retention](../concept/push-notification-retention.md)

