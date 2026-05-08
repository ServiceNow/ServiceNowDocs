---
title: Getting started with Virtual Agent Designer
description: The Virtual Agent Designer is a diagram tool for creating and managing assets, which are blueprints for conversations between a Virtual Agent and a user. You can design topics that help your users resolve common work issues or guide them through self-service tasks.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: reference
last_updated: "2026-03-24"
reading_time_minutes: 16
keywords: [virtual agent, designer, topic, controls]
breadcrumb: [Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Getting started with Virtual Agent Designer

The Virtual Agent Designer is a diagram tool for creating and managing assets, which are blueprints for conversations between a Virtual Agent and a user. You can design topics that help your users resolve common work issues or guide them through self-service tasks.

Virtual Agent conversations are built using topics. When building an asset, there are various components \(controls\) that you can use to build the logic of a conversation, as well as the responses that the user sees.

**Note:** Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents. For more information, see ServiceNow product tiers.

You can also view and manage the following in Assistant Designer:

-   Conversational subflows and actions for LLM-enabled conversations

    Virtual Agent conversations can include subflows and actions if they were made conversational in Workflow Studio or topics that include subflows and actions through the Action utility node.

    -   Conversational subflows and actions are available in Assistant Designer only if Now Assist in Virtual Agent has been configured.
    -   Conversational subflows and actions are also shown in Assistant Designer if the Now Assist Panel is available. For more information on the Now Assist Panel, see Now Assist panel.
    -   Conversational subflows and actions only appear to users during a conversation if the Subflows and actions skill is turned on in Now Assist Admin. For more information, see [Now Assist in Virtual Agent](../../now-assist-in-va/concept/now-assist-in-va-landing.md).
    **Note:** Conversational subflows and actions are not applicable to the Virtual Agent Designer legacy topic cards page view.

-   Custom skills

    You can view custom skills created in Now Assist Skill Kit through Assistant Designer. For more information, see [Managing custom skills in Assistant Designer Asset library](../concept/managing-custom-skills.md).

-   AI agents

    You can view AI agents created in AI Agent Studio through Assistant Designer. For more information, see [Managing AI agents in Assistant Designer](../concept/managing-use-cases-ai-agents.md).


Virtual Agent can use either large language model \(LLM\) or Natural Language Understanding \(NLU\) to match the user's request with the appropriate conversation or topic.

With LLM topic discovery, you can use generative AI through Now Assist in Virtual Agent to match the user's request with the desired conversation or topic. With Now Assist in Virtual Agent, you can test and publish your models from within Virtual Agent Designer. Now Assist in Virtual Agent uses LLMs and generative AI skills to improve deflection rates and reduce the amount of time-consuming work that Natural Language Understanding \(NLU\) topic discovery requires. For more information, see [LLM topic discovery in Virtual Agent](../concept/va-llm.md).

With NLU/keyword topic discovery, the topic author associates the topic with an intent within an NLU model. An intent describes what the user wants to achieve. User utterances are matched with intents to determine the most appropriate topic for the user. Associating a topic with a model and intent is called mapping.

If you're using ServiceNow NLU/keyword topic discovery, then Assistant Designer integrates with NLU Workbench so that you can map topics to new or existing models and intents without leaving the interface. In addition, you can also modify utterances, test, train, and publish your models from within Virtual Agent Designer.

## Assistant Designer Asset library

**Note:** An updated Assistant Designer Asset library user interface is available when you install Now Assist in Virtual Agent and turn on the Now Assist Topics skill. This content assumes that you have activated this skill and can see the list view. If this skill is not activated, you see the legacy UI and topics page. For more information, see [Virtual Agent Designer legacy topics page](vad-prev-topics-page.md).

When you open Assistant Designer, the Asset library lists the assets in your instance. These assets include topics, topic blocks, setup topics, small talk topics, custom controls, subflows, actions, and AI agents.

**Note:** Along with small talk topics, you can also set small talk filters to redirect conversations based on unexpected user statements. For more information, see Configure small talk filters.

In the Asset library, you can access and edit any of these assets, and create topics, topic blocks, setup topics, small talk topics, and custom controls, in Virtual Agent Designer

![Assistant Designer Asset library page.](../images/vad-home-page.png)

**Note:** Conversational subflows and actions are available in Assistant Designer if Now Assist in Virtual Agent has been configured. Conversational subflows and actions are also shown in Assistant Designer if the Now Assist Panel is available. For more information on the Now Assist Panel, see Now Assist panel.

You can test and preview active topics to verify that they work as intended. You can also sort and search for topics. When you have many assets, use the search bar ![](../images/search-icon.png) and filter icon ![](../images/filter-icon.png) to quickly organize and find your topics. For more information, see [Assistant Designer Asset library](vad-topics-page.md).

Each topic list entry identifies the asset and provides the following information by default:

|Field|Description|
|-----|-----------|
|Name|Name of the topic. Template topics also contain `(Template)` in the name.|
|Type|Topic types include Topic, Topic Block, Setup Topic, Small Talk, Custom Input Control, Custom Response Control, Subflows, and Actions.|
|Status|Status types include Draft, Modified \(with unsaved changes\), or Published.|
|Active|Whether the topic is active or inactive.|
|Last modified|Time \(minutes, hours, days, or months\) that the topic was last modified.|
|Description|Description of the topic. For topics, this field is created and updated on the Properties tab.|

When you open a topic, a tab is displayed in the navigation header bar. The topic's name is shown on the tab, and a red dot appears if the topic has unsaved changes. Hover over the tab to view the scope in which the topic was created.

![Topic tab that displays the topic name, saved condition, and application scope.](../images/topic-tab-example.png)

When you open a subflow or action, a tab is displayed in the navigation header bar. This tab opens the subflow or action in Workflow Studio within the Assistant Designer environment.

## Assistants

For LLM topics, the **Select assistant** list enables you to filter the assets based on the LLM Virtual Agent \(assistant\) selected. By default the following assistants are available for Assistant Designer Asset library:

-   Now Assist in Virtual Agent \(default\)
-   Now Assist Panel - Platform \(default\)

    For the Now Assist Panel - Platform \(default\) assistant, if you want AI agents to be Discoverable, Visible, or Promoted, set the **Value** field in the system property **sn\_aia.enable\_aiagents\_discovery** to **True**. If the **Value** field is set to **False**, then AI agents can't be set as Discoverable, Visible, or Promoted. To enable this property, you must contact ServiceNow support.


![Select an assistant.](../images/vad-home-assist.png)

You can create assistants from **Conversational interfaces** &gt; **Assistants**. For more information about creating assistants, see [Create a chat assistant](../../now-assist-in-va/task/create-assistant.md).

For more information about LLM assistants, see [LLM assistants](../../now-assist-in-va/concept/llm-assistants.md).

## Topic properties

Use the topic **Properties** tab to identify a Virtual Agent asset and how it’s used. The properties you can specify depend on the method of topic discovery used in your instance: LLM or NLU/keyword. For example, if you have activated Now Assist and are working with an LLM topic, the **Properties** tab includes fields for what you want the topic to do and which assistants to use. If you have activated NLU, you can select **NLU/keyword** from the Type drop-down menu when you create a topic. The **Properties** tab includes fields for identifying the NLU model and intent for the topic.

Use the **Properties** tab to do the following:

-   Specify the name and type of asset, such as [topic](../task/create-virtual-agent-topic.md), [topic block](../concept/topic-blocks-overview.md), [custom control](../concept/custom-controls.md), and so on.
-   Specify the model type, purpose of the topic, and which assistants can run this topic for Now Assist customers.
-   Specify the model type, add a topic description, specify the purpose of the topic, and select which assistants can run this topic for Now Assist customers.
-   Control who uses the topic and [what channels it can run in](../concept/integrate-virtual-agent.md).
-   Associate [live agent variables](live-agent-chat-context-vars.md) with a topic.
-   Add keywords to the topic or map the topic to a ServiceNow NLU model and intent.

For more information, see [Topic Properties tab](vad-topic-properties-tab.md).

## Topic flow

When you create or update a topic, topic block, or custom control, you build the conversation flow on the **Flow** tab. In the default view, the flow looks like a diagram. Use the controls for user inputs, bot responses, and utilities to define the flow. The status of the topic and NLU/Keyword model \(if used\) appears in the upper-right corner of the window.

The **Table View** option in Virtual Agent Designer displays the nodes in your conversation flow as a table, rather than as a diagram. Each node is identified in a corresponding row in the table. You can add, change, or delete nodes using these table rows.

For example, instead of dragging controls and dropping them onto the canvas, you can select **Add new node** to insert a node into the appropriate row in the table. When you focus on a particular row \(node\), the corresponding property sheet for the node is displayed.

As you create or update your design, you might find it helpful to switch between the diagram view and the Table View using the **Table View** option. If your conversation contains many nodes, the Table View lets you review all the nodes in your conversation quickly. You can use the **Search table** option to quickly find a particular node or control.

Use the **Flow** tab to do the following:

-   Design your topic flow. For more information, see [Design the flow of your topic](../concept/design-va-topic.md).
-   Add script variables. For more information, see [Define script variables for a topic](../task/define-script-variables-topic.md).
-   Add entities to your topic. For more information, see [Use system-derived entities in your topic](../task/use-system-entities-va-topic.md).
-   Add nodeless entities, if you’re creating a topic for [Add nodeless NLU entities to your topic flow](../task/add-nodeless-entities-input-vars.md).

For more information, see [Topic Flow tab](vad-topic-flow-tab.md).

## NLU model and intent mappings

If you activated NLU on your instance, the **NLU Intent** tab is available for your topics in Virtual Agent Designer. Once you have bound the topic to a model and intent on the **Properties** tab, you can use the **NLU Intent** tab to do the following:

-   Review utterances used in your topic. For more information, see [Review and edit utterances and associated entities](../task/modify-nlu-utterances-va-topic.md).
-   Train your NLU models. For more information, see [Train, test, and publish your NLU model](../task/train-test-publish-nlu-model-vad.md).

    Test the topic model with user utterances to see if it triggers the appropriate intent and topic. You can also test entity recognition.


**Note:** The virtual\_agent\_admin role includes the nlu\_admin role, which enables topic authors to work on ServiceNow models.

For more information about this tab, see [Topic NLU Intent tab](vad-topic-nlu-intent-tab.md).

## Topic languages

The **Languages** tab displays the topic's translation status for languages that have been activated on the instance for both LLM and NLU conversations. If you're using NLU/keyword, you can also review the language mappings for that topic.

Use the **Languages** tab to do the following:

-   View translation status for activated language plugins.
-   Test your topic with a given language. For more information, see [View and test the topic in a specific language](../task/test-nlu-language-model.md).
-   Edit translations. For more information, see [Edit the topic translations](../task/edit-translations-va-topics.md).
-   Request translations. For more information, see [Request topic translations in additional languages](../task/use-lf-translate-va.md).
-   View and update NLU language and entity mapping. For more information, see [View or modify NLU language mappings and entity mapping](../task/map-nlu-language-model.md).

    For more information, see [NLU model mapping in Virtual Agent Designer](../concept/nlu-model-binding-vad.md).


For more information about this tab, see [Topic Languages tab](vad-topic-languages-tab.md).

-   **[Designing a Virtual Agent topic](../concept/design-va-topic.md)**  
Walk through the design of an example Virtual Agent topic that enables users to view incidents they submitted. The example highlights various design controls that can be used to build the conversation flow.
-   **[Creating a Virtual Agent topic](../task/create-virtual-agent-topic.md)**  
Use Virtual Agent Designer to create and modify Virtual Agent topics \(conversations\). Build your topic to meet a specific objective or goal, such as fulfilling a user's request or helping a user complete a task.
-   **[Migrating NLU/keyword Virtual Agent topics to LLM topics](../concept/llm-topic-migration.md)**  
The topic migration workflow enables you to migrate your existing Natural Language Understanding \(NLU\)/keyword topics into new large language model \(LLM\) topics.
-   **[Duplicating a Virtual Agent topic](../task/duplicate-virtual-agent-topic.md)**  
Create a topic or topic block by copying an existing Virtual Agent topic or topic block and customize it.
-   **[Testing assistants](../concept/testing-enhanced-chat-conversations.md)**  
Simulate and test assistant conversations from Asset library.
-   **[Testing LLM topics](test-llm-topics.md)**  
Preview, test, and debug topics that use large language models \(LLMs\) in the Assistant Designer chat window.
-   **[Testing NLU/Keyword topics](va-designer-testing.md)**  
Use the chat test window to preview, test, and debug Natural Language Understanding \(NLU\)/Keyword topics.
-   **[Debug a Virtual Agent topic](virtual-agent-troubleshooting-guide.md)**  
Investigate and resolve unexpected behavior in your custom Virtual Agent topics, topic blocks, and controls.
-   **[Publish a Virtual Agent topic](../task/publish-virtual-agent-topic.md)**  
Deploy an inactive topic or an updated topic to save it and make it available to users on Virtual Agent clients.
-   **[Delete a Virtual Agent topic](../task/delete-virtual-agent-topic.md)**  
Delete a Virtual Agent topic that is no longer needed.
-   **[Promote or demote LLM conversational subflows, actions, and topics in Assistant Designer](../task/promote-demote-va-topics.md)**  
Promote assets including conversational subflows, conversational actions, and topics in Assistant Designer, after associating them with a large language model \(LLM\) assistant, to have them suggested to the user by the LLM assistant.
-   **[Reorder promoted LLM conversational subflows, actions, and topics](../task/sort-promoted-va-topics.md)**  
Rearrange LLM assets like conversational subflows, conversational actions, and topics to the desired order after promoting them for recommendation by the Virtual Agent.
-   **[Conversational settings for Assets in the Asset library](../concept/asset-lib-conv-settings.md)**  
Manage asset settings from the Asset library for individual assets.
-   **[Add a condition builder to promoted assets](../task/add-condition-builder-promoted-topics.md)**  
You can define a condition for a given promoted Virtual Agent asset to bring it higher up on the list of promoted assets in a panel conversation.
-   **[Managing conversational subflows in Assistant Designer](../concept/managing-conversational-subflows.md)**  
View and manage conversational subflows through Assistant Designer.
-   **[Managing conversational actions in Assistant Designer](../concept/managing-conversational-actions.md)**  
View and manage conversational actions through Assistant Designer.
-   **[Managing custom skills in Assistant Designer Asset library](../concept/managing-custom-skills.md)**  
View custom skills through Assistant Designer Asset library.
-   **[Managing AI agents in Assistant Designer](../concept/managing-use-cases-ai-agents.md)**  
View AI agents created in AI Agent Studio through Assistant Designer.

**Parent Topic:**[Building and deploying Virtual Agent](../concept/using-virtual-agent.md)

