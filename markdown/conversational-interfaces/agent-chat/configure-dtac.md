---
title: Configuring Dynamic Translation for Agent Chat
description: Activate Dynamic Translation for Agent Chat \(DTAC\) so chat conversations can be translated from one language to another.
locale: en-US
release: zurich
product: Agent Chat
classification: agent-chat
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configuring Agent Chat, Agent Chat, Conversational Interfaces]
---

# Configuring Dynamic Translation for Agent Chat

Activate Dynamic Translation for Agent Chat \(DTAC\) so chat conversations can be translated from one language to another.

![Video link to Dynamic Translation.](../image/icon-video-link.png) [Dynamic Translation for Agent Chat](https://www.youtube.com/watch?v=IsRVDvjHqXw) Watch this video for more information on global support with Dynamic Translation for Agent Chat.

## Prerequisite steps

These tasks must be completed prior to activating DTAC:

-   [Integrate with a translation service provider](https://www.servicenow.com/docs/access?context=integrate-translation-service-provider&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)
-   [Migrate to version v3 of a translator configuration](https://www.servicenow.com/docs/access?context=migrate-v3-dynamic-translation&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)
-   [Translate a knowledge article](https://www.servicenow.com/docs/access?context=translate-knowledge-article&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)

## Activating DTAC

DTAC translates chat conversations from one language to another. The preferred languages for the agent and requester are based on their user profiles and a translation service translates the messages into the defined language of the other participant. Translation service providers support language detection for requesters who are not logged in to ServiceNow®, also referred to as guest users.

DTAC is inactive by default. Before activating DTAC, the following requirements must be completed:

-   [Dynamic translation](https://www.servicenow.com/docs/access?context=dynamic-translation&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)
-   [Set up Agent Chat](../task/ac-configure-agent-chat.md)
-   [Activate a language](https://www.servicenow.com/docs/access?context=t_ActivateALanguage&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)

Activate the Dynamic Translation for Agent Chat plugin \(com.glide.cs.dynamic.translation.agent.chat\).

This also activates these plugins:

-   Dynamic Translation \(com.glide.dynamic\_translation\)
-   Conversational Dynamic Translation \(com.glide.dynamic\_translation.va\_async\)

and these system properties:

-   true - sync
-   false - async
-   absence of this property - async

## Transferring from Virtual Agent to a live agent

Once an agent accepts a chat, they can see the chat history between the Virtual Agent and requester in their preferred language for more context.

Virtual Agent topics must be set up in the desired languages prior to using DTAC. To learn more about how to set up topics, see [Virtual Agent Designer](../../virtual-agent/reference/conversation-designer-virtual-agent.md).

![Transferring from virtual agent to live agent](../../dynamic-translation/image/transfer-va-live-agent.png)

## Translation support in chat conversations

When DTAC is enabled, these items are translated in chat conversations:

-   Users' messages
-   System messages
-   Virtual Agent chat history
-   Record card field values
-   Rich controls

    |Type|Rich Control|
    |----|------------|
    |User input|String|
    |User input|Static choice list|
    |User input|Reference choice|
    |User input|Boolean|
    |User input|Date time|
    |User input|File picker|
    |User input|Carousel|
    |Bot response|Text|
    |Bot response|Single link|
    |Bot response|Multiple links|
    |Bot response|Multi-flow output|
    |Bot response|Script output|
    |Bot response|Record card|


DTAC does not support record card labels. For this functionality to operate, system localization properties must be configured. Navigate to **System Properties** &gt; **System Localization**. For more information, see ServiceNow® product documentation on Localization settings.

![Messages and record card translation support](../../dynamic-translation/image/messages-translation-support.png)

## Analytical reports for DTAC

You can generate a report that counts the number of DTAC chats, to assess how many conversations use the DTAC option.

Monitor the number of true values in the Translated column in the Interaction table. For more information, see the ServiceNow® product documentation on [Interaction records in Workspace](https://www.servicenow.com/docs/access?context=interaction-message-agent-workspace&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US) Interaction records in Agent Workspace.

**Parent Topic:**[Configuring Agent Chat](ci-agent-chat-configuring.md)

