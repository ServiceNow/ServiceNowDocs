---
title: Create a small talk topic
description: Build small talk topics that let Virtual Agent engage in casual conversation with users. A small talk topic provides a response to a casual question that users might ask during a conversation, such as the time or date. A small talk topic can occur anytime within a conversation session and can be unrelated to the original conversation intent.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/virtual-agent/create-small-talk.html
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Creating a Virtual Agent topic, Getting started with the Asset library in Assistant Designer, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Create a small talk topic

Build small talk topics that let Virtual Agent engage in casual conversation with users. A small talk topic provides a response to a casual question that users might ask during a conversation, such as the time or date. A small talk topic can occur anytime within a conversation session and can be unrelated to the original conversation intent.

## Before you begin

If you're creating an LLM small talk topic, ensure you're familiar with LLM descriptions and instructions. For more information, see [LLM description and instruction guidelines for Virtual Agent topics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/virtual-agent/va-llm-instruction-guidelines.md).

If you're creating an NLU small talk topic, define the corresponding intent in the appropriate NLU model.

Role required: virtual\_agent\_admin or admin

## About this task

Small talk topics are conversations that diverge from the original bot conversation, usually to provide answers or information to casual questions that end users might ask. For example, you can create small talk topics that provide the current weather or time of day. When users engage with the bot through a small talk topic, they can return to the original conversation topic.

**Note:** If you have activated ServiceNow® Otto for Virtual Agent, you can also create small talk filters to redirect the conversation if needed. For more information, see [Configure small talk filters](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configure-small-talk-filters.md).

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Assisant Designer**.

2.  Select the **Asset library** tab.

3.  Set the topic discovery toggle switch to **LLM** or **NLU/Keyword**depending on which type you want to create..

4.  Select **Create asset** if you're using LLM, or **Create topic** if you're using NLU/Keyword.

5.  For the Type, select **Small Talk**.

6.  Follow the steps for [creating a topic](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/virtual-agent/create-virtual-agent-topic.md).

    **Note:**

    -   If you're creating an NLU/keyword small talk topic, fill in the following fields on the Properties page.

        |Field|Description|
        |-----|-----------|
        |NLU Model|Model that defines the intent for this small talk topic.|
        |Associated intent|Intent defined in the NLU model for this small talk topic.|

    -   When you complete your small talk topic, remember to publish it when you are ready to deploy it to your Virtual Agent clients.

**Parent Topic:**[Creating a Virtual Agent topic](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/virtual-agent/create-virtual-agent-topic.md)

