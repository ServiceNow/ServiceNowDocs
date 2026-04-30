---
title: Create a notification using a push message
description: Email administrators can create a notification that specifically sends a push notification.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Push notification setup with the ServiceNow mobile app, Push notifications, System notifications, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Create a notification using a push message

Email administrators can create a notification that specifically sends a push notification.

## Before you begin

Configure the [push message](t_CreateAPushMessage.md) before performing these steps.

Role required: admin

## About this task

You can associate a push message with a standard notification. A push message specifies the text the system sends as part of the push notification to the mobile device.

## Procedure

1.  Navigate to **All** &gt; **System Notification** &gt; **Create Push Notification**.

2.  Fill out the notification form as necessary \(see [Create an email notification](t_CreateANotification.md) for descriptions of the form fields.

3.  Select the **What it will contain** tab.

4.  Next to **Push Messages**, select the lock icon and select a push message.

    **Note:** The push message and notification must be for the same table.

5.  Select **Submit**.

    If the notification fails, the user is not notified. If the message fails to send because it exceeds the maximum payload, the instance logs the failure in the System Log.


## What to do next

[Add the push notification to the Push Defaults Registrations table](add-push-notif-reg-table.md) so that the push notification is listed in the notification preferences for users. Users can then select which notifications they want to receive for the ServiceNow mobile app.

