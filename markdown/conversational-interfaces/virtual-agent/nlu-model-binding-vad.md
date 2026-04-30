---
title: NLU model mapping in Virtual Agent Designer
description: ServiceNow model groups help you to manage the localization of both topics and Natural Language Understanding \(NLU\) models more easily. You can map Virtual Agent topics to a new or existing model group directly from Virtual Agent Designer.
locale: en-US
release: zurich
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Create a Virtual Agent topic, Getting started with Virtual Agent Designer, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# NLU model mapping in Virtual Agent Designer

ServiceNow model groups help you to manage the localization of both topics and Natural Language Understanding \(NLU\) models more easily. You can map Virtual Agent topics to a new or existing model group directly from Virtual Agent Designer.

A topic is a Virtual Agent conversation. Users find the appropriate conversation using either keyword or NLU topic discovery. If you're using [NLU for topic discovery](advantages-nlu.md), this means that your topic is associated with an NLU intent, which contains potential user utterances and other information. When a topic is associated with an intent, it’s mapped to that intent. An NLU model is a group of related intents.

When you create or edit a topic and have ServiceNow NLU turned on, then you can do the following in Virtual Agent Designer:

-   Map the topic to an existing model and intent.
-   Map the topic to an existing model and create an intent.

    Mappings are created for all languages that have been activated in NLU Settings as well. For more information, see [Configure Natural Language Understanding in Virtual Agent](../task/configure-nlu-settings.md).

-   Create and map the topic to a new model and intent.

    If more than one language has been activated in NLU Settings, mappings are automatically created for secondary languages in the new model group. For more information, see [Topic mapping to a multilingual NLU model group](multilingual-nlu-model-group-topic-mapping.md).


For example, when creating a topic, you can select the NLU model and its associated intent. In the following Company email issues topic, the selected model from the NLU Model drop-down list is the **ITSM NLU for Virtual Agent \(11 languages\)** model. After selecting the NLU model, the intent list refreshes and you can select your preferred intent. This action maps the NLU intent to this topic. You can change the NLU model and intent selections later on through the topic's **Properties** tab, if needed.

![The Natural Language Understanding section displays on the Properties tab when NLU is enabled. Select an existing NLU model and associated intent or create new ones.](../images/nlu-language-mapping-intent-new.png)

**Parent Topic:**[Create a Virtual Agent topic](../task/create-virtual-agent-topic.md)

