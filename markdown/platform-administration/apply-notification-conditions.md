---
title: Apply notification conditions
description: Set various conditions and filters to control the notifications you receive. You can also enable or disable an email digest and the delivery of individual notifications by channel.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Setting notification preferences in Core UI, Notification Preferences, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Apply notification conditions

Set various conditions and filters to control the notifications you receive. You can also enable or disable an email digest and the delivery of individual notifications by channel.

## Before you begin

Role required: none

## About this task

-   Enable or disable an email digest if a digest is available for the notification. An [email digest](../concept/email-digests.md) is a single email that summarizes the activity for the notification during a time interval that you specify. Admins configure the email digest content for a notification.
-   Enable or disable a channel on which the notification is received.
-   Set preconfigured schedules and filters that determine when you receive your notifications.
-   Set more advanced filter conditions to limit the notifications delivered to you.

## Procedure

1.  Navigate to **User menu** &gt; **Preferences** &gt; **Notifications**.

2.  Select the notification:

    1.  In the Notifications By Category section, select the row or right arrow \(**&gt;**\) of the category that you want to view.

    2.  In the list of notifications for the category, select the row or right arrow \(**&gt;**\) next to the notification that you want to edit.

3.  Enable or disable an email digest for the notification, if an email digest is available:

    1.  Select the **Email Digest** switch.

        The email digest is enabled when the switch is green and turned off when the switch is grey.

    2.  To enable the digest, select the **Interval** \(length of time\) during which the notifications are accumulated.

    The interval begins with the first occurrence of notification activity during the specified interval. For example, if you selected the Daily interval and the first notification occurs at 07:00, the system begins accumulating notifications at 07:00 and stops at 07:00 the next day. Soon after the interval ends, the system sends the email digest instead of sending the individual notifications that were triggered during the digest interval. If you turned off the digest, the system immediately stops accumulating the notifications and doesn’t send the email digest.

4.  Toggle the channel switch enable or disable a channel on which the notification is received.

5.  To apply conditions for notification delivery, select the row or the right arrow \(**&gt;**\) next to the channel for the notification.

    1.  Fill the Apply Conditions form.

        |Field|Description|
        |-----|-----------|
        |Schedule|Determines when the notification can and can’t be received.|
        |Filter|Preconfigured filter with the criteria that determines when the notification can be sent. For example, you might select a filter whose conditions send notifications when an incident with a priority of **1 - Critical** is opened for a network issue.|
        |Advanced filter|Check box to use the condition builder to create additional criteria. When you select the check box, the **Table** and **Conditions** fields are displayed.|
        |Table|Table for the notification. For example, if you selected an incident-related notification, you might select the Incident \[incident\] table.|
        |Conditions|Define as many conditions as needed to limit the notifications you receive. For example, you can choose to be notified only when an incident communication plan is created for a specific configuration item.|

    2.  Select **Save**.


**Parent Topic:**[Setting notification preferences in Core UI](../concept/user-notification-preferences.md)

