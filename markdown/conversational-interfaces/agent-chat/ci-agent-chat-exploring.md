---
title: Exploring Agent Chat
description: Agent Chat enables live agents to interact directly with end users through chat. Your end users can chat with a live agent to ask questions and receive information.
locale: en-US
release: australia
product: Agent Chat
classification: agent-chat
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Agent Chat, Conversational Interfaces]
---

# Exploring Agent Chat

Agent Chat enables live agents to interact directly with end users through chat. Your end users can chat with a live agent to ask questions and receive information.

## Agent Chat overview

The chat system starts with virtual chat, which is an autonomous chat powered by artificial intelligence. The requester can then ask to chat with a live agent using Agent Chat. Using Agent Chat, agents can communicate with requesters, create incident or case records, or transfer chats to another agent or queue.

Agent Chat uses a persistent widget for chat conversations on any portal page of the portal that you're using. You can establish assignment rules to enable chat conversations to reach the best agent available who has the capacity and skills to handle the job or the agent can transfer the chat to another agent. Agents can use response templates to enable reusable, consistent messages to requesters.

Virtual chat conducts a survey before and after the Agent Chat. The pre-survey gets preliminary information about the requester to aid in the chat session. The post-chat survey gets feedback on the requester's satisfaction with the agent who helped.

**Note:** Starting with the Quebec release, legacy Agent Workspace is no longer deployed, enhanced, or supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

## Agent Chat benefits

|Benefit|Feature|Users|
|-------|-------|-----|
|Agents and chat managers have a conversation without the requester knowing.|[Agent Whisper](ci-agent-whisper.md)|Agents, chat managers|
|Gather important information from end users through conversational questionnaires.|[Chat surveys](ci-conversational-chat-surveys.md)|Agents|
|Download a transcript of the conversation between the agent and the requester.|[Chat transcript downloads for requesters](ci-chat-transcripts.md)|Requester|
|Carry out a conversation in another language.|[Dynamic Translation for Agent Chat overview](ci-dtac-overview.md)|Agent, requester|
|Initiate conversations with requesters on a messaging app of the requester's choice.|[Agent-Initiated Messaging Interface](agent-init-messg-interface.md)|Agent, requester|
|Read a summarization of the chat \(this is available only if you have Now Assist installed\).||Agent|

## Routing chats

Requesters start chats with virtual chat. When they request to chat with a live agent on Agent Chat, their request goes into a queue controlled by Advanced Work Assignment \(AWA\), which routes chats to different agents based on availability, queue length, and expertise.

## Unfurling links

If an agent or requester enters a link during an Agent Chat conversation, the links are "unfurled" or displayed with a preview of the website's content. Links in Agent Chat conversations are unfurled in the same manner as Virtual Agent. For more information, see [Using link unfurling in Virtual Agent](../../virtual-agent/concept/va-link-unfurling.md).

## Cross-channel conversation history and cross-channel message-level sentiment

Agents can see cross-channel conversation history and cross-channel message-level sentiment in real time when an agent is having a live conversation with a requester in the chat panel in Agent Chat. For more information, see .

