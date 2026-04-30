---
title: Call workflow activity
description: The Call activity makes outbound phone calls using a Notify workflow. This workflow activity can be added to any table.
locale: en-US
release: xanadu
product: Notify
classification: notify
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Notify workflow activities, Reference, Notify, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Call workflow activity

The **Call** activity makes outbound phone calls using a Notify workflow. This workflow activity can be added to any table.

## Input variables

Input variables determine the initial behavior of the activity.

|Variable|Description|
|--------|-----------|
|Notify Number|The Notify phone number to make the call from. When you initiate a call, the outgoing call workflow for the number group associated with this number runs.|
|Phone number to call|The E.164-compliant phone number to call.|
|Advanced|Select this check box to use a script to determine number to call, and the Notify number to call from instead of using the **Phone number to call** and **Notify Number** variables.|
|Script|Define a script that controls which number to call. This script should return a string listing the Notify number sys\_id, as well as the phone number to call, such as \{notify\_number: 'sys\_id', phone\_number: '+316...'\}|

## Conditions

The conditions determine which transition comes after this activity. The **call** activity does not specify any conditions by default.

You can add an error condition to this activity. The activity transitions through the error condition if the call could not be set up due to invalid data returned by the advanced script.

