---
title: Configure asynchronous chat for the web channel
description: Set the chat widget as a messaging channel for asynchronous chat.
locale: en-US
release: xanadu
product: Conversational Interfaces
classification: conversational-interfaces
topic_type: task
last_updated: "2024-11-14"
reading_time_minutes: 1
breadcrumb: [Using Asynchronous Chat in messaging channels, Channels in Conversational Interfaces, Exploring Conversational Interfaces Console, Conversational Interfaces Console, Conversational Interfaces]
---

# Configure asynchronous chat for the web channel

Set the chat widget as a messaging channel for asynchronous chat.

## Before you begin

Role required: virtual\_agent\_admin or admin

## About this task

The base system web channel, mweb, is automatically configured as a chat channel for web and mobile clients. To use the web channel as a messaging channel, change the channel **Type** in the Messaging Channel \[sys\_cs\_channel\] table.

## Procedure

1.  Navigate to **All** and in the Navigation filter, enter `sys_cs_channel.list`.

2.  In the Messaging Channel form, select the mweb record and double click the **Type** field.

3.  Change the Type to Messaging.

4.  Save the value.


## Result

The mweb channel is set to messaging mode. To help manage long-running conversations, the system automatically performs certain messaging actions in messaging mode:

-   Requester message without agent response \(agent experience\): If an agent hasn't responded to a requester within 30 minutes, the agent receives a reminder that a message from an end user needs a response.
-   Agent message without requester response: If a requester hasn't responded to an agent message after two days, the conversation state in the Interaction record is automatically set to closed abandoned.

For more information on messaging actions, see [Configure messaging actions](https://www.servicenow.com/docs/access?context=configure-messaging-actions&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US). For details on Virtual Agent and Live Agent idle conversation timeouts and conversation states, see [Closing Virtual Agent and Agent Chat conversations](../concept/va-open-conversations.md) and [Virtual Agent interaction records](../concept/va-interactions.md).

**Parent Topic:**[Using Asynchronous Chat in messaging channels](../concept/async-chat.md)

