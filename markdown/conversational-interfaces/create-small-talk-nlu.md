---
title: \(Legacy\) Create a small talk topic for NLU
description: Build small talk topics that let Virtual Agent engage in casual conversation with users. A small talk topic provides a response to a casual question that users might ask during a conversation, such as the time or date. A small talk topic can occur anytime within a conversation session and can be unrelated to the original conversation intent.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/create-small-talk-nlu.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Create an NLU topic, Build and deploy NLU conversations, \(Legacy\) Virtual Agent for NLU, Conversational Interfaces]
---

# \(Legacy\) Create a small talk topic for NLU

Build small talk topics that let Virtual Agent engage in casual conversation with users. A small talk topic provides a response to a casual question that users might ask during a conversation, such as the time or date. A small talk topic can occur anytime within a conversation session and can be unrelated to the original conversation intent.

## Before you begin

Define the corresponding intent in the appropriate NLU model.

Role required: virtual\_agent\_admin or admin

## About this task

Small talk topics are conversations that diverge from the original bot conversation, usually to provide answers or information to casual questions that end users might ask. For example, you can create small talk topics that provide the current weather or time of day. When users engage with the bot through a small talk topic, they can return to the original conversation topic.

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Virtual Agent** &gt; **Designer**.

2.  On the home page, select **Create**.

3.  For the Type, select **Small Talk**.

4.  Follow the steps for [creating a topic](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/create-virtual-agent-topic.md).

    **Note:**

    -   Fill in the following fields on the Properties page.

        |Field|Description|
        |-----|-----------|
        |NLU Model|Model that defines the intent for this small talk topic.|
        |Associated intent|Intent defined in the NLU model for this small talk topic.|

    -   When you complete your small talk topic, remember to publish it when you are ready to deploy it to your Virtual Agent clients.

**Parent Topic:**[\(Legacy\) Creating a Virtual Agent NLU topic](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/create-virtual-agent-topic-nlu.md)

