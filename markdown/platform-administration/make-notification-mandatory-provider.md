---
title: Make a notification mandatory for provider framework
description: Enable admins to mark specific notifications as mandatory that their users cannot turn off.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create, Provider notifications, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Make a notification mandatory for provider framework

Enable admins to mark specific notifications as mandatory that their users cannot turn off.

## Before you begin

Role required: admin

When you make a notification mandatory, the toggle button for that notification is read only in the user notification preferences, preventing the user from unsubscribing or disabling that notification.

## Procedure

1.  Navigate to **All** &gt; **System Notification** &gt; **Provider** &gt; **Notifications**.

2.  Select and open the notification.

3.  Configure the form and add the **Mandatory** field.

    **Note:** This field does not display by default.

    1.  Select the context menu icon ![](../../contextual-search/image/additional-actions.png) and select **Configure** &gt; **Form Layout.**

    2.  Select the **Mandatory** field and the order in which you want the field to appear.

    3.  Select **Save**.

4.  Select the **Mandatory** check box.

    **Note:** To honor auto opt-in capability over mandatory notifications, add the property **glide.notification.provider.mandatory.honor\_auto\_opt\_in** and set it to `true`.


**Parent Topic:**[Create provider notification](../concept/create-provider-notification-using.md)

