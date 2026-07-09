---
title: Mobile push notification components
description: Configure mobile push notifications to target a specific screen in one of the applications.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
---

# Mobile push notification components

Configure mobile push notifications to target a specific screen in one of the  applications.

This configuration determines the structure of the notification, the text the user receives, who should receive the message, and what triggers the delivery of a notification. Users tap the notification and the associated deep link then directs the user to the desired screen.

\[Omitted image "image.mobile-push-sample-content-and-message"\] Alt text: Mobile push notification with arrows pointing to the sample content and sample message.

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

 For more information on content configuration, see .

 Optionally, you can display up to three additional fields in a notification. These fields are visible within the **Notifications** navigation bar tab in a mobile app.

 **Note:**

Mobile UI styles are available for these additional fields. For more information around styling, see .

</td></tr><tr><td>

Push notification message

</td><td>

The push notification message contains the text that users see when they receive a notification. The message displays in the notification center on the device based on your configuration for the user and in the **Notifications** tab.

 For more information on message configuration, see .

</td></tr><tr><td>

Push notification event

</td><td>

The push notification event determines when the mobile push notification is sent and to whom it should be sent to.For more information on event configuration, see .

</td></tr></tbody>
</table>