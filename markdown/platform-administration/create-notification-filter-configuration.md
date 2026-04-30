---
title: Create notification filter configuration for notification preferences
description: Control the list of notifications that are displayed to the users under the advanced notification preferences page. This capability can help narrow down and show only relevant notifications based on user criteria.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Preferences in Next Experience, Notification Preferences, Notifications, Configure core features, Administer]
---

# Create notification filter configuration for notification preferences

Control the list of notifications that are displayed to the users under the advanced notification preferences page. This capability can help narrow down and show only relevant notifications based on user criteria.

## Before you begin

Role required: admin

## Procedure

1.  In the **Filter Navigator**, enter `sys_properties.list`.

2.  Create a property named `glide.notification.preference.apply_filter_config` and set it to **true**.

3.  Navigate to **All** &gt; **System Notification** &gt; **Emails** &gt; **Notification Filter Configuration**.

4.  Select **New**.

5.  Enter the **Name** and the **Order**, the notification filter configuration with the lowest order will take precedence.

6.  Select the User Criteria from the list of target records or create a new [user criteria](../reference/user-criteria-form-notifications.md).

7.  Select **Notification filters** tab to create and submit filter conditions for the selected user criteria.

8.  Specify filters for Classic Notifications and Provider Notifications to control which notifications appear on the preferences page.

9.  Select **Submit**.


**Parent Topic:**[System and custom notification and delivery channel preferences in Next Experience](../concept/advanced-notification-prefrences.md)

