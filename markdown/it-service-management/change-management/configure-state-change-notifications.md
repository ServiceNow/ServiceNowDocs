---
title: Modify the email notification for change request state changes
description: Modify the change request state change notification to specify when it's sent, who receives it, and what it contains. When active, the notification is sent when the state changes to Scheduled, Implement, Review, or Canceled.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/change-management/configure-state-change-notifications.html
release: australia
product: Change Management
classification: change-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Explore, Change Management, IT Service Management]
---

# Modify the email notification for change request state changes

Modify the change request state change notification to specify when it's sent, who receives it, and what it contains. When active, the notification is sent when the state changes to **Scheduled**, **Implement**, **Review**, or **Canceled**.

## Before you begin

Role required: admin

## About this task

By default, the notification is sent to the user who originally requested the change. Notifications are not sent to the user who updated the state on the change request.

## Procedure

1.  Navigate to **All** &gt; **System Notification** &gt; **Email** &gt; **Notifications**.

2.  If the **All** menu is not visible, use the navigation filter instead.

    **Note:** Enter `sysevent_email_action.list` in the navigation filter to open the notifications list directly.

3.  Locate and open **Change request state change notification**.

4.  On the form, modify the **When to send**, **Who will receive**, and **What it will contain** sections.

    For more information about email notifications and the fields in the form, see [Create an email notification](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_CreateANotification.md).

5.  Select **Update**.


**Parent Topic:**[Exploring Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/exploring-change-management.md)

