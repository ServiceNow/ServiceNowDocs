---
title: Configure critical notification
description: Configure the list of critical alerts that you want to receive when your mobile device is in Do Not Disturb mode.
locale: en-US
release: yokohama
product: ITSM Mobile Agent
classification: itsm-mobile-agent
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Enable Override do not disturb to receive critical alerts, Configure, ITSM Mobile Agent, IT Service Management]
---

# Configure critical notification

Configure the list of critical alerts that you want to receive when your mobile device is in Do Not Disturb mode.

## Before you begin

Role required: admin

## About this task

By default, the following notifications are set as critical:

-   Major Incident Promotion Notification
-   Major Incident- ICA SLA Breached
-   Major Incident- ICT SLA Warning

Set any notification as critical and receive alerts when your mobile device is in Do Not Disturb mode.

## Procedure

1.  Navigate to **All** &gt; **System notification** &gt; **Push** &gt; **Push Notification** and open the notification that you want to set as critical.

2.  In the selected notification record, select the **What to send** tab.

3.  Select the info icon \(![Info icon.](../../now-assist-itsm/image/icon-more-info.png)\) next to the **Push message** field.

4.  Select **Open record** from the **Push Notification Message** pop-up message.

5.  Set the **isCritical** attribute value to **true** to set the notification as critical.

    If the **isCritical** attribute value is set to **false**, the notification isn't treated as a critical alert.


