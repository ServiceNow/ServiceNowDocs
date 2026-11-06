---
title: Configure a critical notification
description: Specify which push notifications are sent as critical alerts so that agents receive them even when their mobile device is in Do Not Disturb mode.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/itsm-mobile-agent/configure-critical-notification.html
release: australia
product: ITSM Mobile Agent
classification: itsm-mobile-agent
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [Configure critical notification]
breadcrumb: [Enable critical alerts in Do Not Disturb mode, Configuring ITSM Mobile Agent, ITSM Mobile Agent, IT Service Management]
---

# Configure a critical notification

Specify which push notifications are sent as critical alerts so that agents receive them even when their mobile device is in Do Not Disturb mode.

## Before you begin

Role required: admin

## About this task

By default, the following notifications are set as critical:

-   Major Incident Promotion Notification
-   Major Incident- ICA SLA Breached
-   Major Incident- ICT SLA Warning

You can set any push notification as critical so that agents receive it even when their mobile device is in Do Not Disturb mode.

## Procedure

1.  Navigate to **All** &gt; **System notification** &gt; **Push** &gt; **Push Notification** and open the notification to set as critical.

2.  In the selected notification record, select the **What to send** tab.

3.  Select the info icon \[Omitted image "icon-more-info.png"\] Alt text: next to the **Push message** field.

4.  Select **Open record** from the **Push Notification Message** pop-up message.

5.  Set the **isCritical** attribute value to **true** to set the notification as critical.

    If the **isCritical** attribute value is set to **false**, the notification isn't treated as a critical alert.


