---
title: Using Conversational SMS Integration with Twilio
description: Enable a requester to converse with an agent using the SMS conversations.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Conversational SMS Integration with Twilio, Integrating Virtual Agent with consumer messaging apps, Virtual Agent integration with messaging apps, Integrating Virtual Agent with other channels, Virtual Agent, Conversational Interfaces]
---

# Using Conversational SMS Integration with Twilio

Enable a requester to converse with an agent using the SMS conversations.

An administrator can configure the Conversational SMS Integration with Twilio application for integrating the SMS messaging app with a ServiceNow application.

A requester can initiate SMS conversations with a virtual agent or live agent.

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

**Note:** You accept a work item from the SMS conversation in your Agent Workspace Inbox when an administrator has configured the SMS service channel for transfer of chat conversations. For more information, see [Conversational SMS service channel](https://www.servicenow.com/docs/access?context=conversation-sms-service-channel-store-app&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

## Initiating SMS conversations

As a live agent, you can initiate an SMS conversation with a requester when the Agent-Initiated Messaging Interface application is configured for the SMS messaging channel. By default, the application is configured for agent to initiate SMS conversations with consumers and customer contacts. For more information, see [Initiate messaging conversations from the CSM Configurable Workspace](https://www.servicenow.com/docs/access?context=agent-init-messg-csm-cws&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US) and [Initiate SMS conversations from CSM Agent Workspace](https://www.servicenow.com/docs/access?context=agent-init-sms-csm-ws&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US).

