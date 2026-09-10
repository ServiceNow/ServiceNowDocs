---
title: Multiple conversations in Now Assist AI agents
description: Multiple active conversations enable live agents to maintain separate conversations for different records. You can preserve the context of multiple conversations and enable multiple AI agents to interact at the same time through the Now Assist panel.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/multiple-conversations-aia-new.html
release: australia
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Configure AI Agent Studio, AI Agent Studio, Enable AI experiences]
---

# Multiple conversations in Now Assist AI agents

Multiple active conversations enable live agents to maintain separate conversations for different records. You can preserve the context of multiple conversations and enable multiple AI agents to interact at the same time through the Now Assist panel.

## Multiple conversations between live agents and AI agents overview

Once configured, live agents can interact with multiple AI agent conversations through the Now Assist panel.

**Note:** By default, the ServiceNow Otto panel currently supports only a single conversation and it is required for you to enable the multiple conversation support if you intend to use it

## Enabling multiple conversations

You can enable multiple conversations on a ServiceNow instance in the Messaging Channels \[sys\_cs\_channel.list\] table by setting the value of the **Supports Multiple Conversations** field on the ServiceNow Otto panel record to **true**. If you don’t see this field, make sure you're in the Global scope and are using the **Default view**. If you still don't see the filed, you may have to add the filed to the table. By saving the record and refreshing the instance, you can see the multiple active conversations features in the ServiceNow Otto panel.

## Title for the conversation

With the multiple conversations feature enabled in the ServiceNow Otto panel, the first utterance from the live agent is set as the title for that conversation. For example, if the first utterance is `Explain change risk`, then Explain change risk is set as the title for that conversation in the ServiceNow Otto panel.

## Starting a conversation

Start a new conversation by selecting the plus icon and choosing a topic. See the conversation list by selecting the All chats icon, to see the Active chats and Closed chats.

## Unread chats on the conversation list

See the batch count of the unread chats on the conversation list icon. For example, if number 6 appears on the All chats icon, that means there's six unread conversations on the ServiceNow Otto panel.

