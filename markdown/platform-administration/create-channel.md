---
title: Create notification channels
description: You can add channels to receive your notifications. A notification channel is an email account or voice message system that you have access to.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Setting notification preferences in Core UI, Notification Preferences, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Create notification channels

You can add channels to receive your notifications. A notification channel is an email account or voice message system that you have access to.

## Before you begin

Role required: none

## About this task

Notification channels include email addresses, service providers for SMS messages, and mobile applications. You can create voice notification channels to support applications like Notify.

**Note:** If you are using the ServiceNow mobile application or a custom push application, you do not need to create a push channel for your mobile device. The system automatically creates a channel for the mobile app after you initially log in to your instance from your mobile device.

## Procedure

1.  Navigate to **User menu** &gt; **Preferences** &gt; **Notifications**.

2.  Select **Create Channel**.

3.  Complete the fields on the New Channel form.

<table id="table_k1q_lvk_rz"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

A descriptive name for the channel, such as the device or email account.

</td></tr><tr><td>

Type

</td><td>

The type of channel: -   **Email**: for email messages.

**Note:** All users with an email address have a primary email channel, which is created automatically after a notification is sent to them.

-   **SMS**: for SMS messages.
-   **Voice**: for phone messages.
-   **Instant Message**: for instant messages.
 If you are using the ServiceNow mobile application or a custom push application, the system automatically creates a channel for the mobile app after you initially log in to your instance from your mobile device.

</td></tr><tr><td>

Email address

</td><td>

The email address of the channel.

</td></tr><tr><td>

Phone number

</td><td>

The phone number for SMS messages or for voice messages.

</td></tr><tr><td>

Service provider

</td><td>

The service provider for SMS messages.

</td></tr></tbody>
</table>4.  Select **Save**.

    The system creates and enables the channel, and adds it to the list of notification channels.


## What to do next

To receive notifications on your new notification channel, you must enable the channel for individual notifications. After you enable the channel for a notification, you can set conditions to further control the notifications that you receive on the channel. For more information, see [Apply notification conditions](apply-notification-conditions.md).

**Parent Topic:**[Setting notification preferences in Core UI](../concept/user-notification-preferences.md)

