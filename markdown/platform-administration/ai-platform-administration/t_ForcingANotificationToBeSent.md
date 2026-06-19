---
title: Force a notification to be sent
description: To force a notification to be sent to the specified users, enable forced delivery.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-administration/ai-platform-administration/t\_ForcingANotificationToBeSent.html
release: zurich
product: AI Platform Administration
classification: ai-platform-administration
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Subscription-based notifications, Preferences in Core UI, Notification Preferences, Notifications, Configure core features, Administer]
---

# Force a notification to be sent

To force a notification to be sent to the specified users, enable forced delivery.

## Before you begin

Role required: admin

## About this task

Forcing a notification means that the relevant users receive the notification, even if they have not subscribed to the notification or have turned off the subscription. In addition, the users receive the notification even if the **Notification** field is set to **Disable**.

**Note:** Forced delivery applies to only the primary device of the user. You cannot force a notification to be sent to secondary devices.

## Procedure

1.  Navigate to **All** &gt; **System Notification** &gt; **Email** &gt; **Notifications**.

2.  Open the appropriate notification.

3.  Configure the form and add the **Force delivery** field.

    **Note:** This field does not appear by default.

    1.  Select the context menu icon \(\[Omitted image "ContextMenu.png"\] Alt text: Context menu icon\) and select **Configure** &gt; **Form Layout.**

    2.  Select the **Form delivery** field and the order in which you want the field to appear.

    3.  Select **Save**.

        For more information about configuring the form, see [Configuring the form layout](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-platform-administration/configure-form-layout.md).

4.  Select the **Force delivery** check box.

5.  Select **Update**.

    Unlike using the **Mandatory** option, forcing the delivery does not lock the user's preference or prevent the user from unsubscribing from the notification.


**Parent Topic:**[Subscription-based notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-platform-administration/c_SubscriptionBasedNotifications.md)

