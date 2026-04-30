---
title: Use agentic support for a chat assistant
description: Let the assistant use AI agents and agentic orchestration. AI agent skills are prompt-based and can perform complex tasks. Admins can choose between agentic or standard search Q&amp;A modes.
locale: en-US
release: yokohama
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

See [Create a chat assistant](create-assistant.md).

Agentic orchestration is a design approach that helps AI systems coordinate and manage multiple components such as AI agents, knowledge bases, and Q&amp;A modules to accomplish complex multi-step tasks. These components work together, make real-time decisions, and adapt workflows based on context, ensuring responses use the most relevant skills and content.

Role required: virtual\_agent\_admin or admin

## About this task

Select the operational mode of an assistant. For more information about agentic AI, see [Exploring Now Assist AI agents](https://www.servicenow.com/docs/access?context=exploring-ai-agents&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

## Procedure

1.  Toggle on **Use AI agent skills and orchestration**.

    The option to toggle on **Use AI agent skills and orchestration** only appears for existing customers that previously had the AI agent skill turned off for the assistant. Turning on **Use AI agent skills and orchestration** is an irreversible action. Agentic orchestration is a prerequisite to assign AI agents to an assistant.

    ![Deselect check box if you don't want to prioritize AI agents during skills discovery.](../image/NAinVA-agentic-support-122025.png "Use AI agent skills and agentic orchestration")

2.  Select **Prioritize AI agents during skills discovery**.

    For new customers, when a new assistant is created, AI agent skills and orchestration are already turned on. However, you can opt out. When **Prioritize AI agents during skills discovery** is selected, all AI agents are prioritized over other assets for the assistant.

3.  Select **Save and continue.**


## What to do next

See [Assign search sources to a chat assistant](add-info-sources-assistant.md).

