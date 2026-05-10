---
title: View incident notifications
description: View incident notifications that are sent during specific events in an incident life cycle. These notifications are sent to various recipients including the ESS and the ITIL users.
locale: en-US
release: australia
product: Incident Management
classification: incident-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring Incident Management, Incident Management, IT Service Management]
---

# View incident notifications

View incident notifications that are sent during specific events in an incident life cycle. These notifications are sent to various recipients including the ESS and the ITIL users.

## Before you begin

Role required: admin

## About this task

Incident notifications use the email notification layout and template that are shipped with the Employee Experience Foundation plugin \(com.snc.sn\_ex\_emp\_fd\). The plugin delivers notifications that are consistent and built with the industry best practices for layouts.

**Note:** If you are an upgrade customer, to use the latest email layout, install the Employee Experience Foundation app \(com.snc.sn\_ex\_emp\_fd\) from the ServiceNow® Store. Activate the default incident notifications that use the latest template.

## Procedure

1.  Navigate to **All** &gt; **System Notification** &gt; **Email** &gt; **notifications**.

2.  Filter the list of notifications by **\[Table\] \[is\] \[incident\]**.

3.  View the list of default notifications for incidents.

4.  Click the notification name to view the details.


## What to do next

You can redirect the users to the incident or major incident record in Service Operations Workspace instead of opening in the UI16 interface of Incident Management or Major Incident Management. For more information, see [Email notification redirection for incident and major incident](../concept/email-notif-redirt-inci-major-inci.md).

To receive these notifications, the end user must enable notifications. For more information, see [Subscription-based notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/c_SubscriptionBasedNotifications.md).

-   **[Email notification redirection for incident and major incident](../concept/email-notif-redirt-inci-major-inci.md)**  
You can redirect the users to the incident or major incident record in Service Operations Workspace \(SOW\) instead of opening in the UI16 interface of Incident Management or Major Incident Management.

**Parent Topic:**[Configuring Incident Management](../concept/incident-configuration.md)

**Related topics**  


[Create an email notification](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_CreateANotification.md)

