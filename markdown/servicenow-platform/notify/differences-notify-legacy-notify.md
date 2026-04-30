---
title: Differences between Notify and Legacy Notify
description: Describes the differences between the Notify and Legacy Notify applications, including architecture, workflows, Twilio support, and task-initiated conference calls.
locale: en-US
release: xanadu
product: Notify
classification: notify
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Activate Notify, Configure, Notify, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Differences between Notify and Legacy Notify

Describes the differences between the Notify and Legacy Notify applications, including architecture, workflows, Twilio support, and task-initiated conference calls.

|Legacy Notify \(com.snc.notifynow\)|Notify \(com.snc.notify\)|
|-----------------------------------|-------------------------|
|Is deprecated. Supported only telephony services.|Supports pure conferencing solutions such as Zoom in addition to the Telephony providers like Twilio.|
|Manage a single number from a Twilio account per instance.|Provides support for multiple numbers per Twilio account, especially cross-geographical scenarios.|
|Does not include support for customizable workflows for Voice and SMS incoming or outgoing scenarios.|Workflow-driven approach for handling incoming and outgoing Voice and SMS events, making the integration easy to customize.|
|Hard-coded join conference SMS and IVR prompts for joining a conference call.|Includes a configurable workflow for handling SMS and Voice IVR prompts.|
|Support for SMS-based answers.|Notify On Task support for sending SMS and initiating conference calls from any task.|

**Parent Topic:**[Activate Notify](../task/t_ActivateNotify.md)

