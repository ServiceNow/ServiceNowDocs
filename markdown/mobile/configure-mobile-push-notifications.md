---
title: Mobile push notification components
description: Configure mobile push notifications to target a specific screen in one of the ServiceNow Mobile Platform applications.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Push notifications, Considerations before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Mobile push notification components

Configure mobile push notifications to target a specific screen in one of the ServiceNow Mobile Platform applications.

This configuration determines the structure of the notification, the text the user receives, who should receive the message, and what triggers the delivery of a notification. Users tap the notification and the associated deep link then directs the user to the desired screen.

![Mobile push notification with arrows pointing to the sample content and sample message.](../image/mobile-push-sample-content-and-message.png "Example push notification content and message")

1.  Push notification message content
2.  Push notification message

Configure each component of the push notification because each component is dependent on the other. For example, you must configure push notification content to create a push notification message. Likewise, a push notification event requires a push notification message.

<table id="table_jms_tst_msb"><thead><tr><th>

Notification component

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Push notification message content

</td><td>

The push notification message content contains the location users are directed to when they tap on the notification, as well as the appearance and layout of the notification.

 For more information on content configuration, see [Configure push notification message content](../task/config-push-notification-message-content.md).

 Optionally, you can display up to three additional fields in a notification. These fields are visible within the **Notifications** navigation bar tab in a mobile app.

 **Note:**

Mobile UI styles are available for these additional fields. For more information around styling, see [Mobile UI styles](mobile-ui-styles.md).

</td></tr><tr><td>

Push notification message

</td><td>

The push notification message contains the text that users see when they receive a notification. The message displays in the notification center on the device based on your configuration for the user and in the **Notifications** tab.

 For more information on message configuration, see [Configure a push notification message](../task/configure-push-notification-message.md).

</td></tr><tr><td>

Push notification event

</td><td>

The push notification event determines when the mobile push notification is sent and to whom it should be sent to.For more information on event configuration, see [Configure a push notification event](../task/configure-push-notification-event.md).

</td></tr></tbody>
</table>-   **[Configure push notification message content](../task/config-push-notification-message-content.md)**  
Configure push notification message content and select which mobile application receives notifications. You can configure critical alert notifications, customize the message appearance, and determine the deep link used when users tap the notification.
-   **[Configure a push notification message](../task/configure-push-notification-message.md)**  
Configure the message displayed to users when they receive their push notification.
-   **[Configure a push notification event](../task/configure-push-notification-event.md)**  
Configure when a push notification event is triggered and sends a mobile push notification to users.
-   **[Configure sounds for push notifications](../reference/push-notif-sounds.md)**  
Add sounds and tones to push notifications to indicate to users if a message is urgent or just requires the users' attention.
-   **[Register the standard push notification](../task/sg-mobile-notif-register.md)**  
Register your standard push notification in a push application to use it in your mobile apps.

**Parent Topic:**[Mobile push notifications](sg-mobile-push-notifications.md)

