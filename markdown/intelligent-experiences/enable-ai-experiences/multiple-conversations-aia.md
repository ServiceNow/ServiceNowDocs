---
title: Multiple conversations in Now Assist AI agents
description: Multiple active conversations enable live agents to maintain separate conversations for different records. You can preserve the context of multiple conversations and enable multiple AI agents to interact at the same time through the Now Assist panel.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/enable-ai-experiences/multiple-conversations-aia.html
release: australia
product: Enable AI Experiences
classification: enable-ai-experiences
topic_type: concept
last_updated: "2026-06-21"
reading_time_minutes: 1
breadcrumb: [Configure, Now Assist AI agents, Enable AI experiences]
---

# Multiple conversations in Now Assist AI agents

Multiple active conversations enable live agents to maintain separate conversations for different records. You can preserve the context of multiple conversations and enable multiple AI agents to interact at the same time through the Now Assist panel.

## Multiple conversations between live agents and AI agents overview

Once configured, live agents can interact with multiple AI agent conversations through the Now Assist panel.

**Note:** By default, the Now Assist panel currently supports only a single conversation and it is required for you to enable the multiple conversation support if you intend to use it

## Enabling multiple conversations

Enable multiple conversations on a ServiceNow instance in the Messaging Channels \[sys\_cs\_channel.list\] table by setting the value of the **Supports Multiple Conversations** field on the Now Assist panel record to **true**. If you don’t see this field, make sure you are in the Global scope and are using the Default view. By saving the record and refreshing the instance, you can see the multiple active conversations features in the Now Assist panel.

\[Omitted image "support-multipe-convstns.png"\] Alt text: Now Assist panel enabled to support multiple conversations.

## Title for the conversation

With the multiple conversations feature enabled in the Now Assist panel, the first utterance from the live agent is set as the title for that conversation. For example, if the first utterance is `Explain change risk`, then Explain change risk is set as the title for that conversation in the Now Assist panel.

## Starting a conversation

Start a new conversation by selecting the plus icon \(\[Omitted image "new-nap-chat.png"\] Alt text: New Now Assist panel chat.\) and choosing a topic. See the conversation list by selecting the All chats icon \(\[Omitted image "all-chats-nap.png"\] Alt text: List of conversations.\), to see the Active chats and Closed chats.

## Unread chats on the conversation list

See the batch count of the unread chats on the conversation list icon \(\[Omitted image "nap-all-chats-conv-list.png"\] Alt text: Batch count on the conversations list representing the number of unread conversations.\). For example, if number 6 appears on the All chats icon \(\[Omitted image "nap-all-chats-conv-list.png"\] Alt text: Batch count on the conversations list representing the number of unread conversations.\), that means there's six unread conversations on the Now Assist panel.

