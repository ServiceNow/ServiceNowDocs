---
title: Using Conversational SMS Integration with Twilio
description: Enable a requester to converse with an agent using SMS conversations with Twilio.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Conversational SMS Integration with Twilio, Integrate VA with messaging apps, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Using Conversational SMS Integration with Twilio

Enable a requester to converse with an agent using SMS conversations with Twilio.

An administrator can configure Conversational SMS Integration with Twilio with a ServiceNow application.

A requester can initiate SMS conversations with a virtual agent or a live agent.

A live agent can:

-   Accept SMS conversations as work items from their Agent Workspace Inbox to converse with a requester.
-   Initiate SMS chat conversations from interactions of type Chat from their Agent Workspace Inbox to converse with a requester.
-   For logged in customers, the system automatically identifies the customer by matching their phone number against the customer contact.

## Accepting SMS conversations

As a live agent interacting with a requester over the SMS service channel, you can:

-   Converse with the requester through text messages.
-   Share a knowledge article displayed as a link to the requester.
-   Share a record, for example, a customer service case.
-   Share any URLs as links.
-   Share any images as attachments.

**Note:** You accept a work item from the SMS conversation in your Agent Workspace Inbox when an administrator has configured the SMS service channel for transfer of chat conversations. For more information, see [Conversational SMS service channel](../../advanced-work-assignment/concept/conversation-sms-service-channel-store-app.md).

## Initiating SMS conversations

As a live agent, you can initiate an SMS conversation with a requester when the Agent-Initiated Messaging Interface application is configured for the SMS messaging channel. By default, the application is configured for agent to initiate SMS conversations with consumers and customer contacts. For more information, see [Initiate messaging conversations from the CSM Configurable Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/agent-init-messg-csm-cws.md) and [Initiate SMS conversations from CSM Agent Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/agent-init-sms-csm-ws.md).

**Parent Topic:**[Conversational SMS Integration with Twilio](sms-twilio-store-app.md)

