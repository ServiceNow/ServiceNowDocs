---
title: \(Legacy\) Using multiple active conversations in Virtual Agent
description: Virtual Agent for NLU features the ability to have multiple conversations at the same time, separated and directed by chosen context.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/c\_multiple-active-conversations-va.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Configure NLU, \(Legacy\) Virtual Agent for NLU, Conversational Interfaces]
---

# \(Legacy\) Using multiple active conversations in Virtual Agent

Virtual Agent for NLU features the ability to have multiple conversations at the same time, separated and directed by chosen context.

## Overview of Multiple active conversations for Virtual Agent

Virtual Agent messages commonly follow one conversation with a shared history that persists on all VA clients, and thus all portals. For example, if you’re conversing with Virtual Agent in a Service Portal \(SP\) portal context, the same conversation is shown in an Employee Service Center \(ESC\) portal. The multiple active conversations feature expands the reach of Virtual Agent by eliminating the one-conversation limit. By configuring their Virtual Agent conversations based on context, customers can choose to share or restrict any or all content between concurrent conversations on differing portals.

Each Virtual Agent conversation is fully independent, with no overlap between chats. For example, a conversation in SP will be entirely different from ESC. Each conversation also has its own transcript. You must set up context values for Natural Language Understanding \(NLU\) chats, while large language model \(LLM\) chats are automatically configured for multiple active conversations based on each portal. An administrator can activate an LLM assistant for each portal by using guided setup configurations.

## Benefits of multiple active conversations

Previously, if a user was engaged in a conversation with a virtual agent, the chat would take place in a single context. Switching contexts involved a risk of exposing sensitive information by carrying over the entire chat history to the other portal. For example, if you have an HR conversation in the HR portal, then brought up an IT request, the chat continues in the IT portal. However, this request also brings the HR conversation history into the IT portal with it. Alternatively, admins can activate the **skip\_load\_history** system parameter to avoid exposure risk, but the initial conversation closes when the chat continues on the IT portal.

To exclude conversation history between portals, use the following procedure:

1.  Navigate to **All** &gt; **Service Portal** &gt; **Agent Chat**.
2.  Select the Agent Chat Configuration for which you want to set the context value.
3.  In the Server Script window, add the line `skip_load_history: true` to load conversations without the conversation history.

**Note:** The script syntax may differ depending on the configuration.

The multiple active conversations feature bypasses the skip\_load\_history method, and enables continuous engagement with Virtual Agent chat, by routing selected notifications and topics to their configured contexts only. Users don’t need scripting or extensive customization, and they can conduct conversations without interruption or information exposure in the wrong context. With portals and notification contexts aligned, users receive information appropriate to their context, including incident updates and other relevant data.

## Considerations for using multiple active conversations

Implementing multiple active conversations should happen in the following order: Admins should define portal consumer context values, set or update a default context, activate the multiple active conversations system, and finally, configure notifications sent to portals. However, if the delivered Service Portal context is sufficient, admins can skip configuring and setting values.

Topics can be created within a portal context. If the portal context maps to consumer account context, then topics map to consumer account contexts.

