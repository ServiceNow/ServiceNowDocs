---
title: Notify flows
description: Use Notify flows to manage the calls and SMS messages.
locale: en-US
release: zurich
product: Notify
classification: notify
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Reference, Notify, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Notify flows

Use Notify flows to manage the calls and SMS messages.

Starting Zurich, the following actions are available as flow actions and can be used when creating subflows:

<table id="table_ok2_ryf_xfc"><thead><tr><th>

Flow

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Join conference call

</td><td>

The **Join Conference Call** action connects an incoming or outgoing call to a Notify conference call.The action inputs are:

-   Notify Call
-   Notify Conference Call
-   Record
-   Muted
-   Start on enter
-   End on exit
-   Hangup on Star
-   Beep on enter
-   Beep on exit
-   Enable immediate input
-   Additional config

</td></tr><tr><td>

Call

</td><td>

The **Call** action makes outbound phone calls using a Notify flow. This action can be added to any table.The action inputs are:

-   Notify Number
-   Source Table
-   Source Sys Id
-   Phone number to call
-   Conference Call Record
-   User Sys Id
-   Group Sys Id
-   Extra Params

</td></tr><tr><td>

Send SMS

</td><td>

The **send SMS** workflow action sends short text messages using Notify to users' phones. This action can be added to any table.The action inputs are:

-   Recipients
-   Message

</td></tr><tr><td>

Forward call

</td><td>

The **Forward Call** action forwards a Notify call to an E.164-compliant phone number.The action inputs are:

-   Notify Call
-   Phone numbers to call
-   Timeout \(in seconds\)
-   Record

</td></tr><tr><td>

Input

</td><td>

The **Input** action creates a phone menu by presenting a list of options on a Notify call.The action inputs are:

-   Number of digits
-   Finish key
-   Timeout \(in seconds\)
-   IVR menulist
-   Say
-   Play
-   Notify Call

</td></tr><tr><td>

Hangup

</td><td>

The **Hangup** action disconnects an active Notify phone call.The action input is **Notify Call**.

</td></tr><tr><td>

Play

</td><td>

The **Play** action plays a sound file on a Notify call.The action inputs are:

-   URL
-   Loop
-   Notify Call

</td></tr><tr><td>

Record call

</td><td>

The **Record call** action records audio from a user on a Notify call.The action inputs are:

-   Notify Call
-   Max Duration \(in seconds\)
-   Timeout \(in seconds\)
-   Finish Key

</td></tr><tr><td>

Reject

</td><td>

The **Reject** action rejects an incoming Notify call.The action inputs are:

-   Reason
-   Notify Call

</td></tr><tr><td>

Say

</td><td>

The **say** action allows you to play a message, using text to speech, on a Notify call.The action inputs are:

-   Text to say
-   Language
-   Notify Call

</td></tr><tr><td>

Forward to notify client

</td><td>

The **forward to notify client** action connects a phone call to a Notify WebRTC client.The action inputs are:

-   User
-   Timeout \(in seconds\)
-   Record
-   Notify Call

</td></tr><tr><td>

Queue

</td><td>

The **Queue** action places an active Notify call in a queue.The action input is **Notify Call**.

</td></tr></tbody>
</table>You can build, and modify your own custom on-call scheduling flows in Workflow Studio with subflows for new instances. The following base system workflows have been migrated to subflows:

-   \(Re\)join Conference Call
-   Join Conference Call with muting
-   Join Conference Call with SMS

-   **[Create a custom Notify subflow](../task/modify-notify-flow.md)**  
Create your own custom flows to use in Notify using Workflow Studio.

**Parent Topic:**[Notify reference](notify-reference-section.md)

