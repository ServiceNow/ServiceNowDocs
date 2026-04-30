---
title: Filter device notifications using a schedule
description: You can associate devices, such as Email, SMS, and Voice, to schedules that define when the devices can and cannot receive notifications.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Create a notification filter, Subscription-based notifications, Preferences in Core UI, Notification Preferences, Notifications, Configure core features, Administer]
---

# Filter device notifications using a schedule

You can associate devices, such as Email, SMS, and Voice, to schedules that define when the devices can and cannot receive notifications.

## Before you begin

Role required: admin

## About this task

Notifications that are triggered outside of the scheduled days and times for the device are not queued up for delivery at a later time. For example, if an administrator selects the **Weekdays** schedule for an email device, the device receives email notifications triggered between Monday and Friday. If notifications are triggered on Saturday, they are not delivered to the device.

## Procedure

1.  Define schedules as needed using **System Scheduler** &gt; **Schedules** &gt; **Schedules**.

2.  Add or edit a device.

3.  Configure the New Device for System Administrator form and add the **Schedule** field.

4.  In the **Schedule** field, select the schedule for the device.

5.  Select **Submit**.


**Parent Topic:**[Create a notification filter](t_NotificationFilters.md)

