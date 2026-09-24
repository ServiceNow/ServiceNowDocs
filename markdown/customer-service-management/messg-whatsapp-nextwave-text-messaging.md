---
title: Exchange text messages through WhatsApp on NextWave
description: Send and receive text messages between ServiceNow and WhatsApp using the NextWave off-Glide architecture, with conversation threading and full interaction history.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/messg-whatsapp-nextwave-text-messaging.html
release: brazil
topic_type: task
last_updated: "2026-09-18"
reading_time_minutes: 1
keywords: [WhatsApp, text messaging, NextWave]
breadcrumb: [WhatsApp on NextWave, Integrating with consumer messaging apps, Integrate, Customer Service Management]
---

# Exchange text messages through WhatsApp on NextWave

Send and receive text messages between ServiceNow and WhatsApp using the NextWave off-Glide architecture, with conversation threading and full interaction history.

## Before you begin

Role required: **sn\_customerservice\_agent**

The WhatsApp Direct Integration channel must be configured and active in your Customer Service Management instance. See [Configure WhatsApp channel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/configure-whatsapp-channel.md).

## About this task

When a customer sends a text message through WhatsApp, the NextWave off-Glide pipeline receives the message and creates an interaction record in Customer Service Management. The message appears in the agent's CRM Workspace with the full conversation thread.

Agents respond directly from the workspace. Outbound messages are delivered to the customer's WhatsApp app through the NextWave pipeline, maintaining the same conversation thread.

## Procedure

1.  Open the CRM Workspace and locate the WhatsApp interaction in your queue.

    Inbound WhatsApp messages arrive as interactions with type **Messaging** and subtype **WhatsApp**.

2.  Accept the interaction to open the conversation thread.

    The conversation pane displays the customer's message along with any previous interaction history.

3.  Type your response in the message input field and send.

    The message is delivered to the customer's WhatsApp app through the NextWave off-Glide pipeline. Conversation threading and interaction history are maintained automatically.


## Result

Text messages flow between ServiceNow and WhatsApp through the NextWave off-Glide pipeline. Interaction history, including threading, is preserved and accessible in the interaction record.

