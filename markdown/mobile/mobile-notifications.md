---
title: Mobile notifications
description: Mobile notifications appear as badges on your ServiceNow mobile app screen. The notifications alert you to required actions or events.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Using the mobile apps, Mobile Platform]
---

# Mobile notifications

Mobile notifications appear as badges on your ServiceNow mobile app screen. The notifications alert you to required actions or events.

**Important:** Notification badge count behavior can be inconsistent on Android devices. Specifically, the Samsung Galaxy S20 shows badges based on whether you have configured the device to show notification badges with numbers or dots. For more information, see the [Samsung documentation](https://www.samsung.com/hk_en/support/mobile-devices/android-o-os-app-icon-can-show-badges-with-numbers-or-dot-style-badges/). Also, Google Pixel devices do not show a notification count.

## Notification badge count behavior

The badges that appear on your device contain a number. This number shows how many unread notifications and unread Virtual Agent messages that a user has. Notification message counts and Virtual Agent message counts are added. A combined count displays on the ServiceNow mobile app icon on your device as shown in the following image:

![Shows how Virtual Agent messages and push notifications are added together to produce a total notification count on the ServiceNow mobile app notification badge.](../image/notification-badge-count-behavior.png "How badge numbers for Virtual Agent messages and push notifications are incremented")

After you read a notification, the badge notification count decreases. Notifications can be read, not read, or dismissed as described in the following situations:

-   If you don't read a notification, the badge count increases.
-   If you read a notification, the badge count decreases.
-   If you delete a notification without reading it, the badge count decreases.
-   If you delete a notification that has already been read, the badge count doesn't change.

Notification counts on badges are tracked per user, not per device. If you are connected to a ServiceNow instance using multiple devices, all devices show the same badge count. The following image shows the badge count of three different devices, which are connected to an instance by one user.

![Multiple devices connected to the same instance show the same notification badge count.](../image/notif-badges-per-user-not-device.png "Multiple devices connected to the same instance show the same notification badge count")

## Offline mode behavior

When a mobile client goes into offline mode, the client reflects the last number of notifications on the badge count before the device went offline. The read and unread status of notifications does not update while the device is offline.

