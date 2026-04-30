---
title: Forward call workflow activity
description: The Forward Call activity forwards a Notify call to an E.164-compliant phone number.
locale: en-US
release: zurich
product: Notify
classification: notify
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Notify workflow activities, Reference, Notify, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Forward call workflow activity

The **Forward Call** activity forwards a Notify call to an E.164-compliant phone number.

If the person receiving a forwarded call hangs up, the **forward call** activity completes and transitions to the next activity. Any further Notify activities in the workflow run for the caller only.

## Input variables

Input variables determine the initial behavior of the activity.

|Variable|Description|
|--------|-----------|
|Phone number to call|Enter the phone number to forward the call to.|
|Timeout \(in seconds\)|Enter the amount of time to wait for the call to be answered before hanging up.|
|Record|Select this check box to record the conversation.|

## Conditions

The conditions determine which transition comes after this activity.The **forward call** activity does not specify any conditions by default.

You can add an error condition to this activity. The activity transitions through the error condition if the phone number to call is invalid.

