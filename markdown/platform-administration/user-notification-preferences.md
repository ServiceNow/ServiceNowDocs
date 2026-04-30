---
title: Setting notification preferences in Core UI
description: You can set your own notification preferences, including personal subscriptions and channels for receiving them. All users can set these preferences through the Notifications tab of the System Settings window.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Notification Preferences, Notifications, Configure core features, Administer]
---

# Setting notification preferences in Core UI

You can set your own notification preferences, including personal subscriptions and channels for receiving them. All users can set these preferences through the **Notifications** tab of the System Settings window.

With the **Notifications** tab, you can:

-   Search for a specific notification in the list of your notifications.
-   Use a global switch to enable or disable all your notifications.
-   Enable or disable a particular channel for receiving notifications, as well as create, edit, or delete channels.
-   Control the notifications that you receive and apply conditions to restrict notification delivery.
-   Create personal notifications, which are subscriptions to notifications that are important to you.

## Comparison between notification preferences in Core UI and earlier interfaces

In new and upgraded instances that use the Core UI interface, the System Settings window is the central location for managing your notification preferences for Next Experience. The Notification Preference User Interface plugin \(com.glide.notification.preference.ui\) is activated by default.

![Examples of notification preferences in Core UI System Settings window and UI15 and earlier interfaces](../image/NotifPrefsUI16UI15.png "Notification preferences in Core UI and UI15")

In UI15 and earlier interfaces:

-   Users set notification preferences through the **Notification Preferences** link in the User form \(**Self service** &gt; **My Notification Preferences**\).
-   Admins created user devices and set notification preferences for users through the **Notification Preferences** link in the User form, accessed through the User Administration module \(**User Administration** &gt; **Users**\).

    **Note:**

    Admins can revert to the UI15 notification preferences interface by setting the **glide.notification.preference.UI.enabled** property to false.


## Manage your notification preferences in Core UI

**Note:**

To switch to the Core UI from Next Experience, set the property **glide.ui.polaris.core.notification\_preference.enabled** to true.

To access your notification preferences, click the gear icon \(![gear icon](../image/IconUI16Gear.png)\) in the banner frame, and in the System Settings window, click the **Notifications** tab. You can also access the System Settings by navigating to **Self Service** &gt; **My Notification Preferences**.

![Notification settings in the System Settings window](../image/NotifiTabSystemSettings.png "Notifications tab in System Settings window")

In the **Notifications** tab, use the settings in the following table to manage your notifications.

<table id="table_tmx_zxp_vz"><thead><tr><th>

Setting

</th><th>

Description

</th></tr></thead><tbody><tr id="SearchUI16"><td>

Search

</td><td>

Search bar for finding notifications.To find a notification:

-   Enter the name of the notification you are searching for. When you type the first three characters, the system automatically returns a list of notifications matching the characters entered.
-   Enter two asterisks to return a list of all notifications in alphabetic order \(the notifications are not organized by category\).

</td></tr><tr id="AllowNotifications"><td>

Allow notifications

</td><td>

Global switch for enabling or disabling all notifications.

</td></tr><tr id="NotificationChannels"><td>

Notification channels

</td><td>

List of your channels for receiving notifications. Use this section to:-   Enable or disable a channel by using its toggle switch. If you disable a channel, notifications are not delivered through that channel.
-   [Add channels](../task/create-channel.md) using the **Create Channel** option.
-   [Modify channel information](../task/modify-notif-channel.md). Click the channel row or the right arrow \(**&gt;**\) next to the appropriate channel to edit or delete it.

</td></tr><tr id="NotificationsByCategory"><td>

Notifications by category

</td><td>

List of notification categories that identify and group related notifications. Each category contains the notifications that you can subscribe to. To view the notifications in a given category, click the category row or the right arrow \(**&gt;**\) next to the appropriate category. You can:

 -   Edit settings for a notification:
    -   Enable or disable channels for the selected notification.
    -   [Apply notification conditions](../task/apply-notification-conditions.md), such as schedules and filters, that affect the delivery of the notification.
-   [Create personal notifications](../task/create-personal-notifications.md), which are subscriptions to specific notifications that matter to you.

</td></tr></tbody>
</table>**Note:** Subscription-based notifications are not domain aware and cannot support domain-specific settings.

-   **[Subscription-based notifications](c_SubscriptionBasedNotifications.md)**  
Subscription-based notifications enable users to proactively subscribe to items that interest them and unsubscribe from messages that are not mandatory.
-   **[Create notification channels](../task/create-channel.md)**  
You can add channels to receive your notifications. A notification channel is an email account or voice message system that you have access to.
-   **[Modify notification channels](../task/modify-notif-channel.md)**  
You can update channel information for your notifications.
-   **[Delete a notification channel](../task/delete-notif-channel.md)**  
Delete a notification channel so that you no longer receive notifications through the channel.
-   **[Apply notification conditions](../task/apply-notification-conditions.md)**  
Set various conditions and filters to control the notifications you receive. You can also enable or disable an email digest and the delivery of individual notifications by channel.

**Parent Topic:**[Notification Preferences](preferences-landing.md)

