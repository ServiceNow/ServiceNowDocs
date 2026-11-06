---
title: View incident notifications
description: View incident notifications that are sent during specific events in an incident life cycle. Recipients include employee self-service \(ESS\) users and users with the itil role.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/incident-management/t\_ViewIncidentNotification.html
release: australia
product: Incident Management
classification: incident-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Configuring Incident Management, Incident Management, IT Service Management]
---

# View incident notifications

View incident notifications that are sent during specific events in an incident life cycle. Recipients include employee self-service \(ESS\) users and users with the itil role.

## Before you begin

Role required: admin

## About this task

Incident notifications use the email notification layout and template that are shipped with the Employee Experience Foundation plugin \(com.snc.sn\_ex\_emp\_fd\). The plugin delivers notifications that are consistent and built with general guidelines for layouts.

**Note:** To use the latest email layout after an upgrade, install the Employee Experience Foundation app \(com.snc.sn\_ex\_emp\_fd\) from the ServiceNow® Store. Activate the default incident notifications that use the latest template.

## Procedure

1.  Navigate to **All** &gt; **System Notification** &gt; **Email** &gt; **Notifications**.

2.  Filter the list of email notifications by one of the following **Table** values to view the default incident, incident task, and incident alert notifications:

    -   **Incident \[incident\]**: The list of incident email notifications.
    -   **Incident Communication Plan \[incident\_alert\]**: The list of incident alert notifications for incident communication.
    -   **Incident Task \[incident\_task\]**: The list of incident task notifications.
3.  Select the notification name to view the details.


## What to do next

You can redirect the users to the incident or major incident record in Service Operations Workspace instead of opening in the UI16 interface of Incident Management or Major Incident Management. For more information, see [Email notification redirection for incidents and major incidents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/incident-management/email-notif-redirt-inci-major-inci.md).

To receive these notifications, the end user must enable notifications. For more information, see [Subscription-based notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/c_SubscriptionBasedNotifications.md).

-   **[Email notification redirection for incidents and major incidents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/incident-management/email-notif-redirt-inci-major-inci.md)**  
You can redirect users from email notification links to incident or major incident records in Service Operations Workspace \(SOW\) instead of the UI16 interface of Incident Management or Major Incident Management.

**Parent Topic:**[Configuring Incident Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/incident-management/incident-configuration.md)

**Related topics**  


[Create an email notification](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_CreateANotification.md)

