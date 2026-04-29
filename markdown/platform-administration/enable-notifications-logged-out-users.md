---
title: Enable push notifications for logged-out users
description: Enable push notifications for users when they're logged out to deliver timely critical updates.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Push notifications, System notifications, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Enable push notifications for logged-out users

Enable push notifications for users when they're logged out to deliver timely critical updates.

## Before you begin

**Important:** Avoid including sensitive information or actionable notifications in push notifications sent to logged-out users.

Role required: admin

## Procedure

1.  Install the Send Push Notifications to logged-out users \(com.glide.push.logged\_out.users\) plugin.

    This is a maint-only plugin. Request the plugin through the Now Support Service Catalog.

    1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

    2.  Select **Request plugin**.

    3.  On the form, fill in the fields.

<table id="table_h5k_mmr_m3c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

What is your target instance

</td><td>

The instance that you want to activate the plugin on.

</td></tr><tr><td>

Plugin Name

</td><td>

The value should be set to `Send Push Notifications to logged-out users (com.glide.push.logged_out.users)`.

</td></tr><tr><td>

Select Maintenance Date and Time

</td><td>

The date and time to activate the plugin.

</td></tr></tbody>
</table>    4.  Select **Submit**.

        After the Now Support maintenance window timeframe, the plugin will be installed on your instance.

    5.  Confirm the installation by viewing the applications listed in the **Installed** tab in the Application Manager.

2.  Navigate to **All** &gt; **System Notification** &gt; **Push** &gt; **Push Notifications**.

3.  From the list of notifications, select the notification that you want to enable for logged-out users.

4.  In the form, select the **Push to inactive users** check box.

    If the **Push to inactive users** check box is not visible, configure the form layout. For more information, see [Configuring the form layout](../../form-administration/concept/configure-form-layout.md#).

5.  Select **Update**.

6.  Configure the number of days users can receive notifications after they log out.

    1.  Navigate to **All** and enter `sys_properties.list` in the navigation filter.

    2.  Select **New**.

    3.  On the form, fill in the fields.

        |Field|Value|
        |-----|-----|
        |**Name**|`com.glide.push.logged_out.users.threshold_time.days`|
        |**Type**|String|
        |**Value**|The number of days up to which you want users to receive notifications after they log out. The default value of this property is 10.|

    4.  Select **Submit**.


**Parent Topic:**[Push notifications](../concept/c_PushNotifications.md)

**Related topics**  


[Push notification system](../reference/r_PushMessageArchitecture.md)

[Activate push notifications](t_ActivatePushNotifications.md)

[Installed with push notifications](../reference/r_InstalledWithPushNotifications.md#)

[Push notification properties](../reference/r_PushNotificationProperties.md)

[Push notification setup with the ServiceNow mobile app](../reference/r_PushNotificationSetupSN.md)

[Push notification setup with a custom push application for ServiceNow mobile apps](../reference/r_PushNotificationSetupCustom.md)

[Requeue failed push notification messages](t_HandlingFailedPushMessages.md)

[Push notification retention](../concept/push-notification-retention.md)

