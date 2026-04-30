---
title: Create a standard notification
description: Create a standard notification on your instance using the platform notifications.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure actionable push notifications, Mobile push notifications, Considerations before implementation, ServiceNow Mobile Platform configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Create a standard notification

Create a standard notification on your instance using the platform notifications.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Notification** &gt; **Push** &gt; **Create Push Notification**.

2.  In the notification form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of your Notification. This name is not visible to your users.|
    |Active|Whether the notification is active. The instance does not send inactive notifications to your users.|
    |Table|The table containing the records relating to your notification. For example, notifications about new incidents would use the Incident \[incident\] table.|
    |Push Message Only|Whether the notification is a push message only. This field is read-only by default.|
    |Category|The category for your notification. This field value is **Uncategorized** by default.|

3.  Right-click the form header and select **Save**.

4.  Configure the push message for your standard notification.

    1.  Click to display the **What to Send** tab.

    2.  Click the lock icon \(![Lock icon](../image/lock-icon.png)\) next to the **Push Messages** field.

    3.  Click the reference icon \(![Reference icon](../image/reference-lookup-icon.png)\) to display the **Push Notification Messages** list.

    4.  Click **New**.

    5.  In the push notification message form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Name|Name of your push notification message record. This name is not visible to your users.|
        |Application|Scoped application associated with this record. This field defaults to the current application.|
        |Push App|Mobile app that uses your push notification.|
        |Table|The table containing the records relating to your notification. For example, a notification about new incidents would use the Incident \[incident\] table.|
        |Push Message Content|Select the record for the push message content you created in the previous section.|
        |Message|Text the user sees in the push notification. For example, `An incident has been assigned to you`.|

    6.  Click **Submit**.

5.  In the **Notification** form, click **Update**.


**Parent Topic:**[Configure actionable push notifications](../concept/actionable-push-notification.md)

