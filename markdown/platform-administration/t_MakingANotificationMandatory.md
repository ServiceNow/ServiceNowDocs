---
title: Make a notification mandatory
description: To prevent users from turning off or deleting a subscription to a notification, make the notification mandatory.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Subscription-based notifications, Setting notification preferences in Core UI, Notification Preferences, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Make a notification mandatory

To prevent users from turning off or deleting a subscription to a notification, make the notification mandatory.

## Before you begin

Role required: admin

## About this task

When you make a notification mandatory, the notification is locked in user notification preferences, preventing the user from removing or unsubscribing to the notification, filtering it, or changing the schedule.

Users receive mandatory notifications even if they disable notifications.

**Note:** Mandatory notifications apply to only the primary device of the user. You cannot make a notification mandatory for secondary devices.

## Procedure

1.  Navigate to **All** &gt; **System Notification** &gt; **Email** &gt; **Notifications**.

2.  Open the appropriate notification.

3.  Configure the form and add the **Mandatory** field.

    **Note:** This field does not display by default.

    1.  Select the context menu icon \(![Context menu icon](../../form-administration/image/ContextMenu.png)\) and select **Configure** &gt; **Form Layout.**

    2.  Select the **Mandatory** field and the order in which you want the field to appear.

    3.  Select **Save**.

        For more information about configuring the form layout, see [Configuring the form layout](../../form-administration/concept/configure-form-layout.md#).

4.  Select the **Mandatory** check box.

    When a user checks their notification preferences, the control button for the mandatory notification is on and is read only.


**Parent Topic:**[Subscription-based notifications](../concept/c_SubscriptionBasedNotifications.md)

