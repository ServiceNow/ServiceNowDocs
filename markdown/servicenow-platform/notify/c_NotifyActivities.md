---
title: Notify workflow activities
description: Notify workflow activities manage calls and SMS messages in Notify.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/notify/c\_NotifyActivities.html
release: australia
product: Notify
classification: notify
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Notify reference, Notify, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Notify workflow activities

Notify workflow activities manage calls and SMS messages in Notify.

All Notify workflows that manage a phone call must run on the notify\_call table. Call-related Notify activities can be added only to workflows where the **Table** field value is **Notify Call \[notify\_call\]**.

You can identify if an outbound call was answered by a human or by an answering machine from within a Notify workflow by evaluating the **current.is\_human** variable, such as with an **If** workflow activity. This variable is set by the telephony provider when an outbound call is answered. This variable is always true for inbound calls.

**Note:** Do not add a **Timer** activity between multiple Notify activities that interact with active phone calls.

**Important:** When creating a Notify workflow, set the workflow **If condition matches** field to **-- None --**. Notify controls which workflow to run based on the configured number groups.

-   **[Join conference call workflow activity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/notify/r_WflowActivJoinConfCall.md)**  
The **Join Conference Call** activity connects an incoming or outgoing call to a Notify conference call.
-   **[Call workflow activity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/notify/r_WorkflowActivityCall.md)**  
The **Call** activity makes outbound phone calls using a Notify workflow. This workflow activity can be added to any table.
-   **[Send SMS workflow activity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/notify/r_WorkflowActivitySendSMS.md)**  
The **send SMS** workflow activity to send short text messages using Notify to users' phones. This workflow activity can be added to any table.
-   **[Forward call workflow activity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/notify/r_WorkflowActivityForwardCall.md)**  
The **Forward Call** activity forwards a Notify call to an E.164-compliant phone number.
-   **[Input workflow activity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/notify/r_WorkflowActivityGather.md)**  
The **Input** activity creates a phone menu by presenting a list of options on a Notify call.
-   **[Hangup workflow activity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/notify/r_WorkflowActivityHangUp.md)**  
The **Hangup** activity disconnects an active Notify phone call.
-   **[Play workflow activity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/notify/r_WorkflowActivityPlay.md)**  
The **Play** activity plays a sound file on a Notify call.
-   **[Record workflow activity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/notify/r_WorkflowActivityRecord.md)**  
The **Record** workflow activity records audio from a user on a Notify call.
-   **[Reject workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/notify/r_WorkflowActivityRejectCall.md)**  
The **Reject** workflow activity rejects an incoming Notify call.
-   **[Say workflow activity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/notify/r_WorkflowActivitySay.md)**  
The **say** workflow activity allows you to play a message, using text to speech, on a Notify call.
-   **[Forward to notify client workflow activity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/notify/r_WflowActivConnNotifClient.md)**  
The **forward to notify client** workflow activity connects a phone call to a Notify WebRTC client.
-   **[Queue workflow activity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/notify/r_WorkflowActivityQueue.md)**  
The **Queue** activity places an active Notify call in a queue.
-   **[Notify activity event handlers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/notify/c_CustomizingNotifyActivities.md)**  
Notify workflow activities provide JavaScript functions that are invoked automatically when your telephony provider broadcasts certain events.
-   **[Creating Notify activities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/notify/c_CreatingNotifyActivities.md)**  
Default Notify workflow generally performs a single action, such as initiating a phone call. You can create custom Notify workflow activities to implement more complex functionality.
-   **[Notify languages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/notify/c_NotifyLanguages.md)**  
Notify supports multiple languages when using text-to-speech.
-   **[Available Notify activity event handlers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/notify/r_NotifyEventHandlerMatrix.md)**  
When creating Notify workflow activities, you can use event-handler functions to respond to events from a telephony provider.

**Parent Topic:**[Notify reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/notify/notify-reference-section.md)

**Related topics**  


[Using variables in Notify workflow activities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/workflow-activities/c_UsingVariablesInNotifyActivities.md)

