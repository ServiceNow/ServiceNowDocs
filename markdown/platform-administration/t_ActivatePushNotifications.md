---
title: Activate push notifications
description: Several plugins must be activated to use push notifications. If you have the Mobile UI \(com.glide.ui.m\) plugin active, push notification plugins are automatically activated.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Push notifications, System notifications, Notifications, Configure core features, Administer]
---

# Activate push notifications

Several plugins must be activated to use push notifications. If you have the Mobile UI \(com.glide.ui.m\) plugin active, push notification plugins are automatically activated.

## Before you begin

Role required: admin

## About this task

Ensure the following plugins are active on your instance:

-   Push Notification: Provides the necessary components and REST APIs to send push notifications to mobile devices.
-   Notification System Push Addon: Adds support for push notifications to the existing notification system.
-   Push Feedback: Handles feedback from Apple on which devices are no longer valid so they do not keep receiving push notifications.

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  On the All Applications page, select **Request Plugin** to open the request form on Now Support.

3.  On Now Support, select the link to access the Now Support Service Portal Service Catalog.

    ![HI redirect to Service Catalog](../../../reuse/images/hi-redirect.png)

4.  Select your instance.

5.  Select **Actions &gt; Activate Plugin**.

6.  On the form, fill in the fields.

<table id="table_awx_bhf_ygb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr id="target-instance"><td>

Target Instance

</td><td>

Instance on which to activate the plugin.

</td></tr><tr><td>

Plugin Name

</td><td>

Name of the plugin to activate.

</td></tr><tr id="date-time"><td>

Specify the date and time you would like this plugin to be enabled

</td><td>

The date and time must be at least two business days from the current time.

 **Note:** Plugins are activated in two batches, once in the morning and once in the evening, on every business day in the US Pacific time zone. If the plugin must be activated at a specific time, enter the request in the **Reason/Comments** field.

</td></tr><tr id="reasons-comments"><td>

Reason/Comments

</td><td>

Information that would be helpful for the ServiceNow personnel who are activating the plugin. For example, if you need the plugin activated at a specific time instead of during one of the default activation windows, specify that in the comments.

</td></tr></tbody>
</table>7.  Select **Submit**.


**Parent Topic:**[Push notifications](../concept/c_PushNotifications.md)

**Related topics**  


[Push notification system](../reference/r_PushMessageArchitecture.md)

[Installed with push notifications](../reference/r_InstalledWithPushNotifications.md#)

[Push notification properties](../reference/r_PushNotificationProperties.md)

[Push notification setup with the ServiceNow mobile app](../reference/r_PushNotificationSetupSN.md)

[Push notification setup with a custom push application for ServiceNow mobile apps](../reference/r_PushNotificationSetupCustom.md)

[Requeue failed push notification messages](t_HandlingFailedPushMessages.md)

[Push notification retention](../concept/push-notification-retention.md)

