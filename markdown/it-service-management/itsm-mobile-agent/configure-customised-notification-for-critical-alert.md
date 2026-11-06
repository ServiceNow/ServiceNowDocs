---
title: Configure a custom notification as a critical alert
description: Set your custom push notifications as critical alerts in ITSM Mobile Agent.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/itsm-mobile-agent/configure-customised-notification-for-critical-alert.html
release: australia
product: ITSM Mobile Agent
classification: itsm-mobile-agent
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Enable critical alerts in Do Not Disturb mode, Configuring ITSM Mobile Agent, ITSM Mobile Agent, IT Service Management]
---

# Configure a custom notification as a critical alert

Set your custom push notifications as critical alerts in ITSM Mobile Agent.

## Before you begin

The custom notification must be listed in the notification table.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System notification** &gt; **Push** &gt; **Push Notification** and open the notification to set as critical.

2.  In the selected notification record, select the **What to send** tab.

3.  Select the info icon \[Omitted image "icon-more-info.png"\] Alt text: next to the **Push message** field and select **Open record** from the **Push Notification Message** pop-up message.

4.  Open the Push Notification Message Content table and paste `return new sn_itsm_mobile_agt.CriticalPushPayloadBuilder(current, json, attributes).buildJSON();` into the **Push Message Generation** field.

5.  Create an **isCritical** attribute with the attribute type as `string`.

6.  Set the default value of the attribute to `False`.

7.  In the Push Notification Message table, add the **isCritical** attribute and set its value to `true`.


