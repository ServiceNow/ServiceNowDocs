---
title: Use agentic support for a chat assistant
description: Let the assistant use AI agents and agentic orchestration. AI agent skills are prompt-based and can perform complex tasks. Admins can choose between agentic or standard search Q&amp;A modes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/conversational-interfaces/now-assist-in-virtual-agent/use-agentic-support.html
release: zurich
product: Now Assist in Virtual Agent
classification: now-assist-in-virtual-agent
topic_type: task
last_updated: "2025-03-18"
reading_time_minutes: 1
breadcrumb: [Create a chat assistant, View assistants, Configuring assistants overview, Now Assist in Virtual Agent, Conversational Interfaces]
---

# Use agentic support for a chat assistant

Let the assistant use AI agents and agentic orchestration. AI agent skills are prompt-based and can perform complex tasks. Admins can choose between agentic or standard search Q&amp;A modes.

## Before you begin

See [Create a chat assistant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/now-assist-in-virtual-agent/create-assistant.md).

Agentic orchestration is a design approach that helps AI systems coordinate and manage multiple components such as AI agents, knowledge bases, and Q&amp;A modules to accomplish complex multi-step tasks. These components work together, make real-time decisions, and adapt workflows based on context, ensuring responses use the most relevant skills and content.

Role required: virtual\_agent\_admin or admin

## About this task

Select the operational mode of an assistant. For more information about agentic AI, see .

## Procedure

1.  Toggle on **Use AI agent skills and orchestration**.

    The option to toggle on **Use AI agent skills and orchestration** only appears for existing customers that previously had the AI agent skill turned off for the assistant. Turning on **Use AI agent skills and orchestration** is an irreversible action. Agentic orchestration is a prerequisite to assign AI agents to an assistant.

    \[Omitted image "NAinVA-agentic-support-122025.png"\] Alt text: Deselect check box if you don't want to prioritize AI agents during skills discovery.

2.  Select **Prioritize AI agents during skills discovery**.

    For new customers, when a new assistant is created, AI agent skills and orchestration are already turned on. However, you can opt out. When **Prioritize AI agents during skills discovery** is selected, all AI agents are prioritized over other assets for the assistant.

3.  Select **Save and continue.**


## What to do next

See [Assign search sources to a chat assistant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/now-assist-in-virtual-agent/add-info-sources-assistant.md).

