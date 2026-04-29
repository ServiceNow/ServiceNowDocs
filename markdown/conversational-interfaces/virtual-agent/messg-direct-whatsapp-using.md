---
title: Using Conversational Integration with WhatsApp \(WhatsApp Cloud API\)
description: Enable a requester to converse with an agent at their convenience using the WhatsApp chat conversations through Virtual Agent.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2026-04-29"
reading_time_minutes: 2
breadcrumb: [Conversational Integration with WhatsApp \(WhatsApp Cloud API\), Integrate VA with messaging apps, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Using Conversational Integration with WhatsApp \(WhatsApp Cloud API\)

Enable a requester to converse with an agent at their convenience using the WhatsApp chat conversations through Virtual Agent.

An administrator can configure the Conversational Integration with WhatsApp \(WhatsApp Cloud API\) application for integrating the WhatsApp messaging app with a ServiceNow application. For more information, see [Integrating the WhatsApp messaging app with other applications](messg-whatsapp-integrating-apps.md).

Agents and requesters can do the following:

-   A live agent can initiate WhatsApp chat conversations with a requester.
-   A requester can initiate WhatsApp chat conversations with a Virtual Agent or live agent.
-   A live agent can accept WhatsApp chat conversations as work items from their Agent Workspace Inbox to converse with a requester.
-   For logged in customers, the system automatically identifies the customer by matching their phone number against the customer contact.

## Initiating WhatsApp chat conversations

As a live agent, you can initiate WhatsApp chat conversations with a requester in two ways:

-   Send a message from either an active interaction record, a contact record, or a consumer contact record.
-   Set up notifications to be sent to the requester when a business event occurs or when a record is updated. See [Create a provider notification](../task/direct-whatsapp-create-a-provider-notification.md).

**Note:** The requester must subscribe and opt in to receive notifications.

## Accepting WhatsApp chat conversations

As a live agent interacting with a requester over the WhatsApp service channel, you can do the following:

-   Converse with the requester through text messages.
-   Share a knowledge article displayed as a link to the requester.
-   Share a record. For example, a customer service case.
-   Share any URLs as links.
-   Share any files as attachments.

**Note:** If an administrator has configured the WhatsApp service channel for transfer of chat conversations, then you can accept a work item from the WhatsApp chat conversation in your Agent Workspace Inbox. For more information, see [Transfer WhatsApp chat conversations to live agents](../task/messg-direct-whatsapp-live-agent-conv.md) and [Service channels](../../advanced-work-assignment/concept/awa-service-channels.md).

-   **[Enable WhatsApp channel notifications](../task/enable-direct-whatsapp-channel-notifications.md)**  
Turn on notifications for the WhatsApp channel to send system-generated messages and automated communications.
-   **[Create a provider notification](../task/direct-whatsapp-create-a-provider-notification.md)**  
Execute the following steps to create a provider notification for Virtual Agent and Workspace providers.
-   **[Transfer WhatsApp chat conversations to live agents](../task/messg-direct-whatsapp-live-agent-conv.md)**  
Configure the Advanced Work Assignment application to transfer a WhatsApp chat conversation initiated by a requester to a live agent.
-   **[Capturing information from a user in a WhatsApp chat conversation](messg-direct-whatsapp-capture-info.md)**  
Use the collection of input controls provided by the Virtual Agent Designer to prompt and capture information from a requester in a WhatsApp chat conversation.

**Parent Topic:**[Conversational Integration with WhatsApp \(WhatsApp Cloud API\)](messg-direct-whatsapp.md)

