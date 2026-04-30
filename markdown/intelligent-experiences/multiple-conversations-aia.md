---
title: Multiple conversations in Now Assist AI agents
description: Multiple active conversations enable live agents to maintain separate conversations for different records. You can preserve the context of multiple conversations and enable multiple AI agents to interact at the same time through the Now Assist panel.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2026-04-29"
reading_time_minutes: 1
breadcrumb: [Exploring Now Assist AI agents, Now Assist AI agents, Enable AI experiences]
---

# Multiple conversations in Now Assist AI agents

Multiple active conversations enable live agents to maintain separate conversations for different records. You can preserve the context of multiple conversations and enable multiple AI agents to interact at the same time through the Now Assist panel.

## Multiple conversations between live agents and AI agents overview

Once configured, live agents can interact with multiple AI agent conversations through the Now Assist panel.

**Note:** By default, the Now Assist panel currently supports only a single conversation and it is required for you to enable the multiple conversation support if you intend to use it

## Enabling multiple conversations

Enable multiple conversations on a ServiceNow instance in the Messaging Channels \[sys\_cs\_channel.list\] table by setting the value of the **Supports Multiple Conversations** field on the Now Assist panel record to **true**. If you don’t see this field, make sure you are in the Global scope and are using the Default view. By saving the record and refreshing the instance, you can see the multiple active conversations features in the Now Assist panel.

![Now Assist panel enabled to support multiple conversations.](../image/support-multipe-convstns.png)

## Title for the conversation

With the multiple conversations feature enabled in the Now Assist panel, the first utterance from the live agent is set as the title for that conversation. For example, if the first utterance is `Explain change risk`, then Explain change risk is set as the title for that conversation in the Now Assist panel.

## Starting a new conversation

Start a new conversation by selecting the plus icon \(![New Now Assist panel chat.](../image/new-nap-chat.png)\) and choosing a topic. See the conversation list by selecting the All chats icon \(![List of conversations.](../image/all-chats-nap.png)\), to see the Active chats and Closed chats.

## Unread chats on the conversation list

See the batch count of the unread chats on the conversation list icon \(![Batch count on the conversations list representing the number of unread conversations.](../image/nap-all-chats-conv-list.png)\). For example, if number 6 appears on the All chats icon \(![Batch count on the conversations list representing the number of unread conversations.](../image/nap-all-chats-conv-list.png)\), that means there's six unread conversations on the Now Assist panel.

