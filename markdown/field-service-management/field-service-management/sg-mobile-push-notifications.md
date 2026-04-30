---
title: Mobile push notifications
description: Mobile push notifications are configurable pushed messages that appear directly in a mobile app. These push notifications are non-actionable or actionable, and are configured by administrators to meet the needs of their users.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
---

# Mobile push notifications

Mobile push notifications are configurable pushed messages that appear directly in a mobile app. These push notifications are non-actionable or actionable, and are configured by administrators to meet the needs of their users.

Non-actionable notifications are created by configuring a mobile push notification and then using the mobile deep link generator to generate links that navigate users into any screen type within a mobile app. To learn more about the mobile deep link generator, see .

Actionable push notifications require you to perform additional steps, such as mapping functions for each push action. For more information about actionable notifications, see .

Define push notifications as critical when you require users to be immediately alerted to an event. Critical alerts override Do Not Disturb or Silent mode settings on your users' mobile device. For more information, see .

You can target mobile push notifications for any of the specific  mobile apps.

## Push notifications structure overview

![image.SNMobileAppPushNotificationStructureOverview]

You must configure mobile push notifications in your  instance before they can be sent to users on their mobile devices.

## Add push notifications to mobile apps with 

In the  family release and later, you can now add push notifications to your mobile apps with :

![image.push-notif-in-mab]

Select **Mobile notifications** in the menu and then select the push notification you want to use. For more information about , see .

