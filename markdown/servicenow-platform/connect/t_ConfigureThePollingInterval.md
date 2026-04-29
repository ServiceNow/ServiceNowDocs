---
title: Configure the polling interval
description: The polling interval determines how frequently the system polls for new Connect messages.
locale: en-US
release: australia
product: Connect
classification: connect
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Connect administration, Connect, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure the polling interval

The polling interval determines how frequently the system polls for new Connect messages.

## Before you begin

Role required: admin

## About this task

The default interval is 10 seconds. You can change this value. The shorter the polling interval, the more frequently the system checks for new messages and the greater the impact on performance.

**Note:** This setting impacts Connect Chat and Connect Support.

## Procedure

1.  Navigate to **sys\_properties.list**.

2.  Locate the **collaboration.polling\_interval** property.

3.  Set the **Value** to a different number of seconds.

    Setting the polling interval to a value smaller than 2 is likely to tax the system too heavily, while a value greater than 10 is likely to result in a poor user experience.


