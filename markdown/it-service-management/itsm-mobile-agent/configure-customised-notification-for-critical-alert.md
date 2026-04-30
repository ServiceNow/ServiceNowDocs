---
title: Configure a customized notification for critical alert
description: Set your custom notifications as critical for ITSM Mobile Agent
locale: en-US
release: xanadu
product: ITSM Mobile Agent
classification: itsm-mobile-agent
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Enable Override do not disturb to receive critical alerts, Configure, ITSM Mobile Agent, IT Service Management]
---

# Configure a customized notification for critical alert

Set your custom notifications as critical for ITSM Mobile Agent

## Before you begin

Ensure that the custom notification is listed in the notification table.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System notification** &gt; **Push** &gt; **Push Notification** and open the notification that you want to set as critical.

2.  In the selected notification record, select the **What to send** tab.

3.  Select the info icon \(![Info icon.](../../now-assist-itsm/image/icon-more-info.png)\) next to the **Push message** field and select **Open record** from the **Push Notification Message** pop-up message.

4.  Open the **Push Notification Message Content** table and paste the **return new sn\_itsm\_mobile\_agt.CriticalPushPayloadBuilder\(current, json, attributes\).buildJSON\(\);** attribute in the **Push Message Generation** field.

5.  Create a new **isCritical** attribute with the attribute type as `string`.

6.  Set the default value for the property as `False`.

7.  In the Push Notification Message table, add the **isCritical** attribute, and set the value as `true`.


