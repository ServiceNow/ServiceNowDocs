---
title: Exploring Agent Chat
description: Agent Chat lets live agents chat directly with end users, who can ask questions and receive information.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/conversational-interfaces/agent-chat/ci-agent-chat-exploring.html
release: australia
product: Agent Chat
classification: agent-chat
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Agent Chat, Conversational Interfaces]
---

# Exploring Agent Chat

Agent Chat lets live agents chat directly with end users, who can ask questions and receive information.

## Agent Chat overview

The chat system starts with virtual chat, which is an autonomous chat powered by artificial intelligence. The requester can then ask to chat with a live agent using Agent Chat. Using Agent Chat, agents can communicate with requesters, create incident or case records, or transfer chats to another agent or queue.

Agent Chat uses a persistent widget for chat conversations on any page of your portal. You can set up assignment rules that route chats to an available agent who has the capacity and skills to help. Agents can also transfer a chat to another agent. Agents can use response templates to send reusable, consistent messages to requesters.

Virtual chat conducts a survey before and after the Agent Chat conversation. The pre-chat survey collects preliminary information about the requester to aid in the chat session. The post-chat survey collects feedback about the requester’s satisfaction with the agent who helped.

**Note:** Starting with the Quebec release, legacy Agent Workspace is no longer deployed, enhanced, or supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

## Agent Chat benefits

|Benefit|Feature|Users|
|-------|-------|-----|
|Talk privately with other agents and chat managers without the requester seeing the messages.|[Agent Whisper](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/conversational-interfaces/agent-chat/ci-agent-whisper.md)|Agents, chat managers|
|Gather important information from end users through conversational questionnaires.|[Chat surveys](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/conversational-interfaces/agent-chat/ci-conversational-chat-surveys.md)|Agents|
|Download a transcript of the conversation between the agent and the requester.|[Chat transcript downloads for requesters](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/conversational-interfaces/agent-chat/ci-chat-transcripts.md)|Requester|
|Carry out a conversation in another language.|[Dynamic Translation for Agent Chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/conversational-interfaces/agent-chat/ci-dtac-overview.md)|Agent, requester|
|Start conversations with requesters on the messaging app they choose.|[Agent-Initiated Messaging Interface](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/conversational-interfaces/agent-chat/agent-init-messg-interface.md)|Agent, requester|
|Read a summary of the chat. Available only if you have Now Assist installed.||Agent|

## Routing chats

Requesters start chats with virtual chat. When they request to chat with a live agent on Agent Chat, their request goes into a queue controlled by Advanced Work Assignment \(AWA\), which routes chats to different agents based on availability, queue length, and expertise.

## Unfurling links

If an agent or requester enters a link during an Agent Chat conversation, the system unfurls the link, displaying a preview of the website’s content. Links unfurl the same way as in Virtual Agent. For more information, see [Using link unfurling in Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/conversational-interfaces/virtual-agent/va-link-unfurling.md).

## Cross-channel conversation history and cross-channel message-level sentiment

Agents can see cross-channel conversation history and cross-channel message-level sentiment in real time during a live conversation with a requester in the chat panel in Agent Chat. For more information, see .

