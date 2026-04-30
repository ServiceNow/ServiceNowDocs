---
title: Enable dynamic translation for email notifications
description: Enable dynamic translation for a notification to send dynamically translated emails to recipients in their preferred language.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Dynamic translation, Multilingual email notifications, Email and SMS notifications, System notifications, Notifications, Configure core features, Administer]
---

# Enable dynamic translation for email notifications

Enable dynamic translation for a notification to send dynamically translated emails to recipients in their preferred language.

## Before you begin

An email notification must exist. For more information, see [Create an email notification](t_CreateANotification.md).

You must activate the Glide Notification Translation \(com.glide.notification.translation\) plugin.

Set the system property for the dynamic translation. For more information see, [Enable dynamic translation](enable-email-notification-translation.md).

Role required: admin

## About this task

Notification recipients must be defined as active users in the User \[sys\_user\] table. They must also have a valid email address defined for their primary channel \(device\) in the Notification Device \[cmn\_notif\_device\] table.

## Procedure

1.  Navigate to **All** &gt; **System Notifications** &gt; **Email** &gt; **Notifications**.

2.  Select the name of the email notification you want to send.

3.  Select the **What it will contain** tab.

4.  If **Advanced view** is not already selected, select it.

5.  Select the **Enable Dynamic Translation** check box.


## What to do next

[Preview email notifications](t_PreviewingNotifications.md)

**Parent Topic:**[Dynamic translation](../concept/dynamic-translation.md)

**Related topics**  


[Enable dynamic translation](enable-email-notification-translation.md)

[Configure the note banner for translated emails](config-email-notification-banner.md)

