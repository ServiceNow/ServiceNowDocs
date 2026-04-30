---
title: View incident notifications
description: View incident notifications that are sent during specific events in an incident life cycle. These notifications are sent to various recipients including the ESS and the ITIL users.
locale: en-US
release: xanadu
product: Incident Management
classification: incident-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure, Incident Management, IT Service Management]
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

In email notifications, you can decide where the links to an incident record are redirected. Instead of an incident record automatically opening in the classic UI16 interface in Incident Management, the incident record can be opened in Service Operations Workspace \(SOW\). The ITSM Notifications Redirection \(com.snc.itsm.notifications\_redirection\) plugin is installed and activated automatically to support this behavior. The incident record link in an email notification opens in SOW only if the following conditions are met:

-   The **Redirect SOW Email notification** \(**sow\_email\_notification\_redirect**\) system property is set to true.
-   The user selecting the incident record link has the sn\_sow\_user role.

To ensure consistency, the email notification template for incident is updated to send the notification from SOW in the same format as sent from classic UI16 interface. Also, the template theme is updated to match the Next Experience theme.

To receive these notifications, the end user must enable notifications. For more information, see [Subscription-based notifications](https://www.servicenow.com/docs/access?context=c_SubscriptionBasedNotifications&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

**Parent Topic:**[Configuring Incident Management](../concept/incident-configuration.md)

**Related topics**  


[Create an email notification](https://www.servicenow.com/docs/access?context=t_CreateANotification&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)

