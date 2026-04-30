---
title: Dynamic Translation for Agent Chat overview
description: Dynamic Translation for Agent Chat \(DTAC\) translates chat conversations from one language to another. This translating enables agents and requesters to have chat conversations with each other without the need of a shared language.
locale: en-US
release: zurich
product: Agent Chat
classification: agent-chat
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Exploring Agent Chat, Agent Chat, Conversational Interfaces]
---

# Dynamic Translation for Agent Chat overview

Dynamic Translation for Agent Chat \(DTAC\) translates chat conversations from one language to another. This translating enables agents and requesters to have chat conversations with each other without the need of a shared language.

For example, a requester who speaks only French starts a chat conversation with a live agent who speaks only English. From the requester’s view, the entire conversation is conducted in French, while from the agent’s view, the entire conversation is conducted in English.

DTAC enables cross-locale support teams and merger and acquisition projects to save time and money by handling larger volumes of chat conversations from other regions.

**Note:**

-   DTAC is supported on Agent Workspace, not on Connect Support.
-   DTAC is currently not supported when autopilot is in progress. When the requester responds to prompts from autopilot topics, these responses are not translated for the agent, even if DTAC is turned on for that conversation. See [Conversation Autopilot](ci-agent-chat-using.md#) for more information.

## How DTAC works

DTAC uses [Dynamic translation](https://www.servicenow.com/docs/access?context=dynamic-translation&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US) and a translation service provider to translate chat conversations in real time. Available translation service providers include:

-   [Set up Google cloud translator service spoke](https://www.servicenow.com/docs/access?context=setup-google-translator&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)
-   [Microsoft Azure Translator Service spoke](https://www.servicenow.com/docs/access?context=microsoft-translation-spoke&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)
-   Microsoft Azure OEM

## Mobile clients

DTAC is available for requesters on Agent Chat in mobile for iOS and Android.

## Translation support limited to one language

DTAC can only support translation from one language to another therefore additional agents or managers joining chat sessions should speak the same language as the primary agent.

-   Agent chat transfers – Agents transferring a chat conversation should both speak the same language.
-   Managers joining chat conversation – Managers joining chat conversation to monitor or assist agents should speak the same language as the primary agent.

## Chat summarizations

DTAC also translates chat summarizations.

## Agent presence states

DTAC does not translate agent presence states.

## Attachments within DTAC

When inserting an attachment into a chat, DTAC does not translate the file name or the contents of the attachment.

