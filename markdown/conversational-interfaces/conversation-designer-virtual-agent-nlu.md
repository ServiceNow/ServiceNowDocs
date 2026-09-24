---
title: \(Legacy\) Getting started with Virtual Agent Designer for NLU
description: The Virtual Agent Designer is a diagram tool for creating and managing assets, which are blueprints for conversations between a Virtual Agent and a user. You can design topics that help your users resolve common work issues or guide them through self-service tasks.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/conversation-designer-virtual-agent-nlu.html
release: brazil
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 8
keywords: [virtual agent, designer, topic, controls]
breadcrumb: [Build and deploy NLU conversations, \(Legacy\) Virtual Agent for NLU, Conversational Interfaces]
---

# \(Legacy\) Getting started with Virtual Agent Designer for NLU

The Virtual Agent Designer is a diagram tool for creating and managing assets, which are blueprints for conversations between a Virtual Agent and a user. You can design topics that help your users resolve common work issues or guide them through self-service tasks.

Virtual Agent conversations are built using topics. When building an asset, there are various components \(controls\) that you can use to build the logic of a conversation, as well as the responses that the user sees.

Virtual Agent can use Natural Language Understanding \(NLU\) to match the user's request with the appropriate conversation or topic.

With NLU/keyword topic discovery, the topic author associates the topic with an intent within an NLU model. An intent describes what the user wants to achieve. User utterances are matched with intents to determine the most appropriate topic for the user. Associating a topic with a model and intent is called mapping.

If you're using ServiceNow NLU/keyword topic discovery, then Virtual Agent Designer integrates with NLU Workbench so that you can map topics to new or existing models and intents without leaving the interface. In addition, you can also modify utterances, test, train, and publish your models from within Virtual Agent Designer.

## Topic properties

Use the topic **Properties** tab to identify a Virtual Agent asset and how it’s used. The properties you can specify depend on the method of topic discovery used in your instance: NLU or keyword. If you have activated NLU, you can select **NLU/keyword** from the Type drop-down menu when you create a topic. The **Properties** tab includes fields for identifying the NLU model and intent for the topic.

Use the **Properties** tab to do the following:

-   Specify the name and type of asset, such as [topic](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/create-virtual-agent-topic-nlu.md), [topic block](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/topic-blocks-overview.md), [custom control](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/custom-controls.md), and so on.
-   Control who uses the topic and [what channels it can run in](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/integrate-virtual-agent.md).
-   Associate [live agent variables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/live-agent-chat-context-vars.md) with a topic.
-   Add keywords to the topic or map the topic to a ServiceNow NLU model and intent.

For more information, see [\(Legacy\) Topic Properties tab for NLU](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/vad-topic-properties-tab-nlu.md).

## Topic flow

When you create or update a topic, topic block, or custom control, you build the conversation flow on the **Flow** tab. In the default view, the flow looks like a diagram. Use the controls for user inputs, bot responses, and utilities to define the flow. The status of the topic and NLU/Keyword model \(if used\) appears in the upper-right corner of the window.

The **Table View** option in Virtual Agent Designer displays the nodes in your conversation flow as a table, rather than as a diagram. Each node is identified in a corresponding row in the table. You can add, change, or delete nodes using these table rows.

For example, instead of dragging controls and dropping them onto the canvas, you can select **Add new node** to insert a node into the appropriate row in the table. When you focus on a particular row \(node\), the corresponding property sheet for the node is displayed.

As you create or update your design, you might find it helpful to switch between the diagram view and the Table View using the **Table View** option. If your conversation contains many nodes, the Table View lets you review all the nodes in your conversation quickly. You can use the **Search table** option to quickly find a particular node or control.

Use the **Flow** tab to do the following:

-   Design your topic flow. For more information, see [\(Legacy\) Designing a Virtual Agent NLU topic](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/design-va-topic-nlu.md).
-   Add script variables. For more information, see [Define script variables for a topic](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/define-script-variables-topic.md).
-   Add entities to your topic. For more information, see [Use system-derived entities in your topic](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/use-system-entities-va-topic.md).
-   Add nodeless entities, if you’re creating a topic for [Add nodeless NLU entities to your topic flow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/add-nodeless-entities-input-vars.md).

For more information, see [Topic Flow tab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/vad-topic-flow-tab.md).

## NLU model and intent mappings

If you activated NLU on your instance, the **NLU Intent** tab is available for your topics in Virtual Agent Designer. Once you have bound the topic to a model and intent on the **Properties** tab, you can use the **NLU Intent** tab to do the following:

-   Review utterances used in your topic. For more information, see [Review and edit utterances and associated entities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/modify-nlu-utterances-va-topic.md).
-   Train your NLU models. For more information, see [Train, test, and publish your NLU model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/train-test-publish-nlu-model-vad.md).

    Test the topic model with user utterances to see if it triggers the appropriate intent and topic. You can also test entity recognition.


**Note:** The virtual\_agent\_admin role includes the nlu\_admin role, which enables topic authors to work on ServiceNow models.

For more information about this tab, see [\(Legacy\) Topic NLU Intent tab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/vad-topic-nlu-intent-tab.md).

## Topic languages

The **Languages** tab displays the topic's translation status for languages that have been activated on the instance for both LLM and NLU conversations. If you're using NLU/keyword, you can also review the language mappings for that topic.

Use the **Languages** tab to do the following:

-   View translation status for activated language plugins.
-   Test your topic with a given language. For more information, see [View and test the topic in a specific language](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/test-nlu-language-model.md).
-   Edit translations. For more information, see [Edit the topic translations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/edit-translations-va-topics.md).
-   Request translations. For more information, see [Request topic translations in additional languages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/use-lf-translate-va.md).
-   View and update NLU language and entity mapping. For more information, see [View or modify NLU language mappings and entity mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/map-nlu-language-model.md).

    For more information, see [\(Legacy\) NLU model mapping in Virtual Agent Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/nlu-model-binding-vad.md).


For more information about this tab, see [\(Legacy\) NLU Topic Languages tab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/vad-topic-languages-tab.md).

**Parent Topic:**[\(Legacy\) Building and deploying Virtual Agent for NLU](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/using-virtual-agent-nlu.md)

