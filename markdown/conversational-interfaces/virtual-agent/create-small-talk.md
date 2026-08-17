---
title: Create a small talk topic
description: Build small talk topics that let Virtual Agent engage in casual conversation with users. A small talk topic provides a response to a casual question that users might ask during a conversation, such as the time or date. A small talk topic can occur anytime within a conversation session and can be unrelated to the original conversation intent.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/conversational-interfaces/virtual-agent/create-small-talk.html
release: zurich
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Create a Virtual Agent asset, Getting started with Assistant Designer Asset library, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Create a small talk topic

Build small talk topics that let Virtual Agent engage in casual conversation with users. A small talk topic provides a response to a casual question that users might ask during a conversation, such as the time or date. A small talk topic can occur anytime within a conversation session and can be unrelated to the original conversation intent.

## Before you begin

If you're creating an LLM small talk topic, ensure you are familiar with LLM descriptions and instructions. For more information, see [LLM description and instruction guidelines for Virtual Agent topics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/va-llm-instruction-guidelines.md).

If you're creating an NLU small talk topic, define the corresponding intent in the appropriate NLU model.

Role required: virtual\_agent\_admin or admin

## About this task

Small talk topics are conversations that diverge from the original bot conversation, usually to provide answers or information to casual questions that end users might ask. For example, you can create small talk topics that provide the current weather or time of day. When users engage with the bot through a small talk topic, they can return to the original conversation topic.

**Note:** If you have activated ServiceNow Otto for Virtual Agent, you can also create small talk filters to redirect the conversation if needed. For more information, see [Configure small talk filters](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/configure-small-talk-filters.md).

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Assistant Designer**.

2.  Select the **Asset library** tab.

3.  Set the topic discovery type toggle switch to **LLM** or **NLU/Keyword**, depending on which type you want to create.

4.  Select **Create asset** or **Create topic**, depending on which topic discovery type you selected.

5.  For the Type, select **Small Talk**.

6.  Follow the steps for [creating a topic](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/create-virtual-agent-topic.md).

    **Note:**

    -   If you're creating an NLU/keyword small talk topic, fill in the following fields on the Properties page.

        |Field|Description|
        |-----|-----------|
        |NLU Model|Model that defines the intent for this small talk topic.|
        |Associated intent|Intent defined in the NLU model for this small talk topic.|

    -   When you complete your small talk topic, remember to publish it when you are ready to deploy it to your Virtual Agent clients.

**Parent Topic:**[Create a Virtual Agent asset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/create-virtual-agent-topic.md)

