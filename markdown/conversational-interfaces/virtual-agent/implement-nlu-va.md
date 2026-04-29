---
title: Implement NLU in Virtual Agent
description: Create and maintain NLU model groups and intents that map to your conversation topics in Virtual Agent. You can create and edit model groups in NLU Workbench or from topics in Virtual Agent Designer.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Natural Language Understanding \(NLU\) topic discovery in Virtual Agent, Explore, Virtual Agent, Conversational Interfaces]
---

# Implement NLU in Virtual Agent

Create and maintain NLU model groups and intents that map to your conversation topics in Virtual Agent. You can create and edit model groups in NLU Workbench or from topics in Virtual Agent Designer.

## Before you begin

Activate the plugins for [Glide Virtual Agent](activate-virtual-agent.md) and any [pre-built topics](../reference/prebuilt-topics-ITSM.md) that you want to use.

Role required: virtual\_agent\_admin or admin

## About this task

When authoring conversations for an NLU instance, be aware of the following guidelines:

-   Verify that you are in the appropriate application scope before you create or update a topic. For example, if you are creating ITSM topics, verify that you are in the **ITSM Virtual Agent Conversations** scope, and not the scope for the ITSM NLU Model for Virtual Agent Conversations.
-   Specify the **NLU Model** and **Associated Intent** for the topic in the [Topic Properties tab](../reference/conversation-designer-virtual-agent.md). If you want to allow topic switching in the conversation session, enable **Resume topic flow**.

    **Note:** A topic can map to only one intent in an NLU model. Once you select an intent for a topic, the intent is no longer available for use in other topics.

-   Set the NLU entity properties in the property sheet for each [input control](../reference/va-user-inputs.md) that you add to the conversation flow. The entity properties identify the entity associated with the node, a switch for allowing text input for the control \(prompt\), and another switch for confirming the slot-filled entity value that Virtual Agent extracts.

## Procedure

1.  [View the Virtual Agent General Settings, and change your NLU service provider, if needed.](configure-nlu-settings.md)

    If you're using a different NLU service provider supported by Virtual Agent, configure it as described in one of the following topics:

    -   [IBM Watson Assistant Intent and Entity integration](configure-watson-service-integration.md)
    -   [Google DialogFlow Essentials \(ES\) Intent and Entity integration](../concept/configure-dialogflow-es-integration.md)
2.  If you're supporting conversations in other languages, [enable NLU languages in Virtual Agent settings](enable-langs-va-gen-settings.md).

3.  Associate a model group and intent with each Virtual Agent topic in your instance.

    You can do this in the following ways:

    -   [Add NLU to an existing Virtual Agent keyword topic.](add-nlu-existing-keyword-topic.md)
    -   Create or map model groups and intents when you [create a new topic](create-virtual-agent-topic.md).
    -   [Preview](../reference/va-designer-testing.md) and test the pre-built ServiceNow topics in Virtual Agent Designer.

        Determine whether you want to use any of the topics, then [duplicate](duplicate-virtual-agent-topic.md) them as needed.

    -   [Run Topic Recommendations reports for your instance](../concept/va-topic-recommendations.md) to identify pre-built Virtual Agent topics and intents that you can quickly implement in your organization.
4.  [Test the topic](../reference/va-designer-testing.md).

5.  When you're ready to deploy a topic, [publish the topic](publish-virtual-agent-topic.md).


## Result

The topic state changes to **Active**.

