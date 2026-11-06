---
title: Create a small talk topic
description: Build small talk topics that let Virtual Agent engage in casual conversation with users. A small talk topic provides a response to a casual question that users might ask during a conversation, such as the time or date. A small talk topic can occur anytime within a conversation session and can be unrelated to the original conversation intent.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/virtual-agent/create-small-talk.html
release: brazil
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Creating a Virtual Agent topic, Build conversations, Virtual Agent, Conversational Interfaces]
---

# Create a small talk topic

Build small talk topics that let Virtual Agent engage in casual conversation with users. A small talk topic provides a response to a casual question that users might ask during a conversation, such as the time or date. A small talk topic can occur anytime within a conversation session and can be unrelated to the original conversation intent.

## Before you begin

Familiarize yourself with LLM descriptions and instructions. For more information, see [LLM description and instruction guidelines for Virtual Agent topics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/va-llm-instruction-guidelines.md).

Role required: virtual\_agent\_admin or admin

## About this task

Small talk topics are conversations that diverge from the original bot conversation, usually to provide answers or information to casual questions that end users might ask. For example, you can create small talk topics that provide the current weather or time of day. When users engage with the bot through a small talk topic, they can return to the original conversation topic.

**Note:** If you have activated ServiceNow Otto for Virtual Agent, you can also create small talk filters to redirect the conversation if needed. For more information, see [Configure small talk filters](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/configure-small-talk-filters.md).

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Assistant Designer**.

2.  Select the **Asset library** tab.

3.  In the Asset library, select **Create asset**.

4.  In the create a topic form, select **Small Talk** from the **Type** drop-down menu.

    \[Omitted image "small-talk.png"\] Alt text: Select Small Talk.

5.  Follow the steps for [creating a topic](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/create-virtual-agent-topic.md).

    When you complete your small talk topic, remember to publish it when you're ready to deploy it to your Virtual Agent clients.


**Parent Topic:**[Build conversations in the Asset library in Assistant Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/conversation-designer-virtual-agent.md)

