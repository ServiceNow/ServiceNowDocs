---
title: Forward to notify client workflow activity
description: The forward to notify client workflow activity connects a phone call to a Notify WebRTC client.
locale: en-US
release: zurich
product: Notify
classification: notify
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Notify workflow activities, Reference, Notify, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Forward to notify client workflow activity

The **forward to notify client** workflow activity connects a phone call to a Notify WebRTC client.

## Input variables

Input variables determine the initial behavior of the activity.

|Variable|Description|
|--------|-----------|
|User|Select the user to connect the call to.|
|Advanced|Select this check box to use a script to determine which client to connect to, instead of using the **User** variable.|
|Script|Define a script that controls which client to connect to. This script should return a GlideRecord for a single User \[sys\_user\] record.|
|Timeout \(in seconds\)|Enter the amount of time to wait for the call to be connected before hanging up.|
|Record|Select this check box to record the call.|

## Conditions

The conditions determine which transition comes after this activity. The **Forward to Notify Client** activity does not specify any conditions by default.

You can add an error condition to this activity. The activity transitions through the error condition if there is an issue with the Notify client.

**Parent Topic:**[Notify workflow activities](../concept/c_NotifyActivities.md)

