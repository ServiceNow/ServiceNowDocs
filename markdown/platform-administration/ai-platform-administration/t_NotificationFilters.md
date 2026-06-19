---
title: Create a notification filter
description: Notification filters enable a user to control the delivery of messages by creating special conditions on multiple tables in a single, reusable filter.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-administration/ai-platform-administration/t\_NotificationFilters.html
release: zurich
product: AI Platform Administration
classification: ai-platform-administration
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Subscription-based notifications, Preferences in Core UI, Notification Preferences, Notifications, Configure core features, Administer]
---

# Create a notification filter

Notification filters enable a user to control the delivery of messages by creating special conditions on multiple tables in a single, reusable filter.

## Before you begin

Role required: admin

## About this task

For example, you can create a filter that controls message delivery when active incidents, problems, and change requests for network issues reach a critical state. For Core UI, filters for notifications or channels are set through the Notifications tab of the System Settings window. For details, see [Apply notification conditions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-platform-administration/apply-notification-conditions.md).

**Note:** The system applies the user's filter conditions after the administrator's conditions have been evaluated. If the administrator's conditions fail, the system ignores notification filters.

## Procedure

1.  Navigate to **All** &gt; **System Notification** &gt; **Email** &gt; **Notification Filters** and create a record.

2.  In the Notification conditions related list of the new record, create and submit filter conditions on one or more tables.

3.  Repeat the procedure to create additional conditions on other tables for this filter.


-   **[Filter device notifications using a schedule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-platform-administration/t_FiltDeviceNotifUsingASchedule.md)**  
You can associate devices, such as Email, SMS, and Voice, to schedules that define when the devices can and cannot receive notifications.
-   **[Edit the schedule or filter of an existing notification message](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-platform-administration/t_EditSchedOrFiltNotifMessage.md)**  
You can update a schedule or filter that was previously created for an email notification.

**Parent Topic:**[Subscription-based notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-platform-administration/c_SubscriptionBasedNotifications.md)

