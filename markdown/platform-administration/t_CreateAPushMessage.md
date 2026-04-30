---
title: Create a push message
description: Before you create a push notification, create the push message with the actual message content for the notification.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Push notification setup with the ServiceNow mobile app, Push notifications, System notifications, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Create a push message

Before you create a push notification, create the push message with the actual message content for the notification.

## Before you begin

The [Push notification plugin](t_ActivatePushNotifications.md) must be active. The plugin is active by default.

Role required: admin

## About this task

The push message and notification must be for the same table.

## Procedure

1.  Navigate to **All** &gt; **System Notification** &gt; **Push** &gt; **Push Messages** and select **New**.

2.  Fill out the fields on the form \(see table\).

3.  Select **Submit**.

<table id="table_wdd_2rs_ks"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter a descriptive name for the message.

</td></tr><tr><td>

Push App

</td><td>

Select the ServiceNow mobile application.

</td></tr><tr><td>

Push Message Content

</td><td>

Select the JSON content to be included in the push notification payload.For example, you can specify predefined button pairs \(Yes/No, Approve/Reject, Accept/Decline\) as part of the push message content.

</td></tr><tr><td>

Message

</td><td>

Enter the message. You can add variables just as you would for other notifications. Any message you enter here overrides the message in the notification.

</td></tr><tr><td class="sub-head" colspan="2">

Related list

</td></tr><tr><td>

Push Message Attribute Values

</td><td>

Optional. Select the attributes that apply to this notification. For details, see [Create an attribute value or action for a push message](t_CreateAPushMessageAttributeValue.md).

</td></tr></tbody>
</table>
## What to do next

[Set up the push notification](t_CreatePushNotification.md) that contains the message created or update an existing push notification to use the push message.

