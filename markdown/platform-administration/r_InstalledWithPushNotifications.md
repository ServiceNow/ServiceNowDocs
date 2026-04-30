---
title: Installed with push notifications
description: Several types of components are installed with the push notifications plugins.These tables are installed with push notifications.These business rules are installed with push notifications.These outbound REST messages are installed with push notifications.These roles are installed with push notifications.These components are installed with push notifications.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Push notifications, System notifications, Notifications, Configure core features, Administer]
---

# Installed with push notifications

Several types of components are installed with the push notifications plugins.

**Parent Topic:**[Push notifications](../concept/c_PushNotifications.md)

**Related topics**  


[Push notification system](r_PushMessageArchitecture.md)

[Activate push notifications](../task/t_ActivatePushNotifications.md)

[Push notification properties](r_PushNotificationProperties.md)

[Push notification setup with the ServiceNow mobile app](r_PushNotificationSetupSN.md)

[Push notification setup with a custom push application for ServiceNow mobile apps](r_PushNotificationSetupCustom.md)

[Requeue failed push notification messages](../task/t_HandlingFailedPushMessages.md)

[Push notification retention](../concept/push-notification-retention.md)

## Tables installed with push notifications

These tables are installed with push notifications.

<table id="table_c5m_125_ls"><thead><tr><th>

Table name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Push Applications \[sys\_push\_application\]

</td><td>

Push applications registered to the instance to receive push messages.

</td></tr><tr><td>

Push Default Registrations \[sys\_push\_notif\_default\_reg\]

</td><td>

Contains all the notifications users are automatically subscribed to for a given push application. You can add notifications to this table on the Push Default Registrations related list on the Push Application form.

</td></tr><tr><td>

Push Feedbacks \[sys\_push\_feedback\]

</td><td>

Feedback from the APNs that tells the instance which push devices can no longer receive push messages. The feedback is handled either on the same instance where your notifications are triggered, or on a central instance that uses a REST call to tell your instance which push applications to deactivate.

</td></tr><tr><td>

Push Message Attribute Definitions \[sys\_push\_notif\_msg\_attr\_def\]

</td><td>

The attribute definitions used for push message content specification.

</td></tr><tr><td>

Push Message Attribute Values \[sys\_push\_notif\_msg\_attr\_val\]

</td><td>

The values associated with push messages.

</td></tr><tr><td>

Push Notifications \[sys\_push\_notification\]

</td><td>

The push notifications that the instance attempted to send to users.

</td></tr><tr><td>

Push Notification Actions \[sys\_push\_notif\_act\_script\]

</td><td>

The action scripts that the instance uses in response to an actionable push message.

</td></tr><tr><td>

Push Notification Installations \[sys\_push\_notif\_app\_install\]

</td><td>

The devices with push apps where users agreed to receive push notifications. This table lists the records by the token for the push app. The instance uses this information to know which push device and app to send notifications to. Records are created in this table when a user logs on an instance with the push app.The Mobile Devices \[sys\_mobile\_devices\] table, which is installed with the Mobile UI plugin, contains all the user devices that logged in to the instance with the ServiceNow mobile application.

</td></tr><tr><td>

Push Notification Messages \[sys\_push\_notif\_msg\]

</td><td>

Messages customized for push notifications. These messages can be associated with a notification.

</td></tr><tr><td>

Push Notification Message Contents \[sys\_push\_notif\_msg\_content\]

</td><td>

The entire content, including JSON, for push messages.

</td></tr><tr><td>

Push Platforms \[sys\_push\_platform\]

</td><td>

The platforms that are supported for push notifications, and the maximum payload size.

</td></tr></tbody>
</table>## Business rules installed with push notifications

These business rules are installed with push notifications.

|Business rule|Table|Description|
|-------------|-----|-----------|
|Build Device and Subscriptions|Push Installation \[sys\_push\_notification\_installation\]|Automatically creates a notification device on a user's notification preferences when the user registers a mobile application with the instance.|

## Outbound REST messages installed with push notifications

These outbound REST messages are installed with push notifications.

|REST message|Description|
|------------|-----------|
|ServiceNowMobileApp Push|The REST message that you can use with your custom iOS mobile app.|

## Roles installed with push notifications

These roles are installed with push notifications.

|Role|Description|
|----|-----------|
|push\_admin|Can create and modify push notifications.|

## Push components installed with push notifications

These components are installed with push notifications.

<table id="table_mjy_bcz_st"><thead><tr><th>

Push application

</th><th>

Description

</th></tr></thead><tbody><tr><td>

ServiceNowPushApp

</td><td>

The push application record for the ServiceNow ServiceNow mobile application. **Note:** The ServiceNow mobile app automatically subscribes users to several push notifications. You can see the list of these notifications in the Push Default Registrations related list on the ServiceNowPushApp application record.

</td></tr></tbody>
</table>|Message content|Description|
|---------------|-----------|
|ConnectMessageContent|The payload for ServiceNow connect messages.|
|Generic Approval \(Background\)|The payload that provides an approval and rejection option to the user receiving the push message.|
|Generic Approval \(Foreground\)|The payload that provides an approval and rejection option to the user receiving the push message.|
|Generic Record Payload|A generic payload that you can use to send push messages to users.|

|Push notification action|Description|
|------------------------|-----------|
|Approval - Approve|Allows an administrator to approve a request.|
|Approval - Reject|Allows an administrator to reject a request.|

|Push notifications|Table|Description|
|------------------|-----|-----------|
|ConnectMessagePushNotification|Live Feed Message \[live\_message\]|Sends a push notification when a new live feed message|

