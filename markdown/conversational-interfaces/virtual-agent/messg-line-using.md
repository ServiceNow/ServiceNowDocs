---
title: Using Conversational Integration with LINE
description: Enable a requester to converse with an agent using the LINE chat conversations.
locale: en-US
release: zurich
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Conversational Integration with LINE, Integrate VA with messaging apps, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Using Conversational Integration with LINE

Enable a requester to converse with an agent using the LINE chat conversations.

An administrator can configure the Conversational Integration with LINE application for integrating the LINE messaging app with a ServiceNow application. For more information, see [Integrating the LINE messaging app with other applications](messg-line-integrating-apps.md).

The following options are available:

-   An administrator can configure system-initiated messages to be delivered as LINE chat conversations.
-   A live agent can initiate LINE chat conversations with a requester.
-   A requester can initiate LINE chat conversations with a virtual agent or live agent.
-   A live agent can accept LINE chat conversations as work items from their Agent Workspace Inbox to converse with a requester.

## Initiating LINE chat conversations

As a live agent, you can initiate LINE chat conversations with a requester in two ways:

-   Send a message from either an active interaction record, a contact record, or a consumer contact record.
-   Set up notifications to be sent to the requester when a business event occurs or when a record is updated. See [Create a provider notification](../../notification/task/create-provider-notification.md).

**Note:** The requester must subscribe and opt in to receive notifications.

## Accepting LINE chat conversations

As a live agent interacting with a requester over the LINE service channel, you can do the following:

-   Converse with the requester through text messages.
-   Share a knowledge article displayed as a link to the requester.
-   Share a record, for example, a customer service case.
-   Share any URLs as links.
-   Share any files as attachments.

**Note:** If an administrator has configured the Line service channel for transfer of chat conversations, then you can accept a work item from the LINE chat conversation in your Agent Workspace Inbox. For more information, see [Transfer LINE chat conversations to live agents](../task/messg-line-live-agent-conv.md) and [Service channels](../../advanced-work-assignment/concept/awa-service-channels.md).

-   **[Transfer LINE chat conversations to live agents](../task/messg-line-live-agent-conv.md)**  
Configure the Advanced Work Assignment application to transfer a LINE chat conversation initiated by a requester \(customer contact or consumer\) to a live agent.

**Parent Topic:**[Conversational Integration with LINE](messg-line.md)

