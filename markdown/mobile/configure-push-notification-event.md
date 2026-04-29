---
title: Configure a push notification event
description: Configure when a push notification event is triggered and sends a mobile push notification to users.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Components, Push notifications, Before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Configure a push notification event

Configure when a push notification event is triggered and sends a mobile push notification to users.

## Before you begin

To create a push notification event and complete the mobile push notification, a push notification message is required. For more information, see [Configure a push notification message](configure-push-notification-message.md).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Notification** &gt; **Push** &gt; **Create Push Notification**.

2.  In the Push Notification form, complete the following fields:

<table id="table_tgb_j3s_wpb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The string value for this record. **Note:** This name is visible to users when they are managing their notification preferences in their personal user settings.

</td></tr><tr><td>

Table

</td><td>

Table selector to choose the table the message originates from. For example, if you want to send notifications when new incidents are created, select the Incident \[incident\] table.

</td></tr><tr><td>

Category

</td><td>

Select where to store notification records if a user manages their platform notification preferences in their personal user settings.

</td></tr></tbody>
</table>3.  In the **When to send** tab, complete the following fields:

<table id="table_il4_v1n_ypb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Inserted

</td><td>

When set to **true**, the notification is sent when a record is inserted into the specified table.

</td></tr><tr><td>

Updated

</td><td>

When set to **true**, the notification is sent when a record is updated.

</td></tr><tr><td>

Conditions

</td><td>

Condition builder for the specified table. When conditions are added, they must be set **true** for the notification to send. These conditions work with the **Inserted** and **Updated** fields.**Note:** If the **Inserted** field is set to **true**, the condition must also be set to **true** for the notification to send.

</td></tr></tbody>
</table>4.  In the **Who will receive** tab, complete the following fields:

    |Field|Description|
    |-----|-----------|
    |Users|List of users from the User \[sys\_user\] table who should receive this notification.|
    |Users/Groups in fields|Users or Groups from one of the fields on the specified table who should receive this notification|
    |Groups|List of groups from the Group \[sys\_user\_group\] table who should receive this notification.|

5.  In the **What to send** tab, select the desired **Push Message**.

6.  Click **Submit** to save the configuration record.


## Result

A push notification event is configured and paired with the push notification message. The mobile push notification is available to send to users.

## What to do next

You can add a push registration so that mobile users can receive this notification without requiring them to opt in. For more information, see [Register the standard push notification](sg-mobile-notif-register.md).

**Parent Topic:**[Mobile push notification components](../concept/configure-mobile-push-notifications.md)

