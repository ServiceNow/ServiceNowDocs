---
title: Build conversations in the Asset library in Assistant Designer
description: The Assistant Designer Asset library includes a diagram tool for creating and managing assets, which are blueprints for conversations between a Virtual Agent and a user. You can design topics that help your users resolve common work issues or guide them through self-service tasks.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/virtual-agent/conversation-designer-virtual-agent.html
release: brazil
product: Virtual Agent
classification: virtual-agent
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 10
keywords: [virtual agent, designer, topic, controls]
breadcrumb: [Virtual Agent, Conversational Interfaces]
---

# Build conversations in the Asset library in Assistant Designer

The Assistant Designer Asset library includes a diagram tool for creating and managing assets, which are blueprints for conversations between a Virtual Agent and a user. You can design topics that help your users resolve common work issues or guide them through self-service tasks.

Virtual Agent conversations are built using topics. When building an asset, there are various components \(controls\) that you can use to build the logic of a conversation, and the responses that the user sees.

**Note:** Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents. For more information, see [ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/ai-native-sku-overview.md).

You can also view and manage the following in Assistant Designer:

-   Conversational subflows and actions for LLM-enabled conversations

    Virtual Agent conversations can include subflows and actions if they were made conversational in Workflow Studio or topics that include subflows and actions through the Action utility node.

    -   Conversational subflows and actions are available in Assistant Designer only if ServiceNow Otto for Virtual Agent has been configured.
    -   Conversational subflows and actions are also shown in Assistant Designer Asset library if the ServiceNow Otto panel is available. For more information, see [ServiceNow Otto panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-panel-overview.md).
    -   Conversational subflows and actions only appear to users during a conversation if the subflows and actions skill is turned on in AI Admin Hub.
-   Custom skills

    You can view custom skills created in AI Skill Kit through Assistant Designer. For more information, see [Managing custom skills in Assistant Designer Asset library](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/managing-custom-skills.md).

-   AI agents

    You can view AI agents created in AI Agent Studio through Assistant Designer. For more information, see [Managing AI agents in Assistant Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/managing-use-cases-ai-agents.md).


Virtual Agent uses large language models \(LLMs\) to match the user's request with the appropriate conversation or topic.

With LLM topic discovery, you can use generative AI through ServiceNow Otto for Virtual Agent to match the user's request with the desired conversation or topic. With ServiceNow Otto for Virtual Agent, you can test and publish your models from within Assistant Designer. ServiceNow Otto for Virtual Agent uses LLMs and generative AI skills to improve deflection rates. For more information, see [LLM topic discovery in Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/va-llm.md).

## Using the Asset library

When you open Assistant Designer, the Asset library lists the assets in your instance. These assets include topics, topic blocks, setup topics, small talk topics, custom controls, subflows, actions, and AI agents.

**Note:** Along with small talk topics, you can also set small talk filters to redirect conversations based on unexpected user statements. For more information, see [Configure small talk filters](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/configure-small-talk-filters.md).

In the Asset library, you can access and edit any of these assets, and create topics, topic blocks, setup topics, small talk topics, and custom controls.

\[Omitted image "vad-home-page.png"\] Alt text: The Asset library displays a list of all topics, topic blocks, AI agents, etc. that is currently available on your instance. Use the controls to filter the list.

**Note:**

-   Conversational subflows and actions are available in Assistant Designer if ServiceNow Otto for Virtual Agent has been configured. Conversational subflows and actions are also shown in Assistant Designer if the ServiceNow Otto panel is available. For more information on the ServiceNow Otto panel, see [ServiceNow Otto panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-panel-overview.md).
-   MCP Server capabilities that you add to an assistant are stored in the sys\_gen\_ai\_skills table at run time, the same underlying table used for other conversational assets. But they don't appear as an asset in the Asset library. MCP Servers aren't treated as a conversational asset, so you can only view and manage them from within the Assistant create/edit flow, in their own dedicated section. Because they don't appear in the Asset library, you can't update their Discoverable, Visible, or Promoted status.

You can test and preview active topics to verify that they work as intended. You can also sort and search for topics. When you have many assets, use the search bar \[Omitted image "search-icon.png"\] Alt text: and filter icon \[Omitted image "filter-icon.png"\] Alt text: to quickly organize and find your topics. For more information, see [Assistant Designer Asset library](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/vad-topics-page.md).

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

\[Omitted image "topic-tab-example.png"\] Alt text: Topic tab that displays the topic name, saved condition, and application scope.

When you open a subflow or action, a tab is displayed in the navigation header bar. This tab opens the subflow or action in Workflow Studio within the Assistant Designer environment.

## Assistants

For LLM topics, the **Select assistant** list enables you to filter the assets based on the LLM Virtual Agent \(assistant\) selected. By default the following assistants are available for Assistant Designer Asset library:

-   ServiceNow Otto for Virtual Agent \(default\)
-   ServiceNow Otto Panel - Platform \(default\)

    For the ServiceNow Otto Panel - Platform \(default\) assistant, if you want AI agents to be Discoverable, Visible, or Promoted, set the **Value** field in the system property **sn\_aia.enable\_aiagents\_discovery** to **True**. If the **Value** field is set to **False**, then AI agents can't be set as Discoverable, Visible, or Promoted.


\[Omitted image "vad-home-assist.png"\] Alt text: Select an assistant.

You can create assistants from **Conversational interfaces** &gt; **Assistants**. For more information about creating assistants, see [Create a chat assistant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/create-assistant.md).

For more information about LLM assistants, see [Create LLM assistants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/llm-assistants.md).

## Topic properties

Use the topic **Properties** tab to identify a Virtual Agent asset and how it’s used.

Use the **Properties** tab to do the following:

-   Specify the name and type of asset, such as [topic](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/create-virtual-agent-topic.md), [topic block](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/topic-blocks-overview.md), [custom control](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/custom-controls.md), and so on.
-   Specify the purpose of the topic, and which assistants can run this topic for ServiceNow Otto customers.
-   Control who uses the topic and [what channels it can run in](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/integrate-virtual-agent.md).
-   Associate [live agent variables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/live-agent-chat-context-vars.md) with a topic.

For more information, see [Topic Properties tab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/vad-topic-properties-tab.md).

## Topic flow

When you create or update a topic, topic block, or custom control, you build the conversation flow on the **Flow** tab. In the default view, the flow looks like a diagram. Use the controls for user inputs, bot responses, and utilities to define the flow. The status of the topic and NLU/Keyword model \(if used\) appears in the upper-right corner of the window.

The **Table View** option displays the nodes in your conversation flow as a table, rather than as a diagram. Each node is identified in a corresponding row in the table. You can add, change, or delete nodes using these table rows.

For example, instead of dragging controls and dropping them onto the canvas, you can select **Add new node** to insert a node into the appropriate row in the table. When you focus on a particular row \(node\), the corresponding property sheet for the node is displayed.

As you create or update your design, you might find it helpful to switch between the diagram view and the Table View using the **Table View** option. If your conversation contains many nodes, the Table View lets you review all the nodes in your conversation quickly. You can use the **Search table** option to quickly find a particular node or control.

Use the **Flow** tab to do the following:

-   Design your topic flow. For more information, see [Design the flow of your topic](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/design-va-topic.md).
-   Add script variables. For more information, see [Define script variables for a topic](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/define-script-variables-topic.md).

For more information, see [Topic Flow tab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/vad-topic-flow-tab.md).

## Topic languages

The **Languages** tab displays the topic's translation status for languages that have been activated on the instance.

Use the **Languages** tab to do the following:

-   View translation status for activated language plugins.
-   Test your topic with a given language. For more information, see [View and test the topic in a specific language](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/test-nlu-language-model.md).

-   **[Designing a Virtual Agent topic](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/design-va-topic.md)**  
Walk through the design of an example Virtual Agent topic that enables users to view incidents they submitted. The example highlights the design controls that you can use to build the conversation flow.
-   **[Duplicating a Virtual Agent topic](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/duplicate-virtual-agent-topic.md)**  
Create a topic or topic block by copying an existing Virtual Agent topic or topic block and customize it.
-   **[Publish a Virtual Agent topic](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/publish-virtual-agent-topic.md)**  
Deploy an inactive topic or an updated topic to save it and make it available to users on Virtual Agent clients.
-   **[Delete a Virtual Agent topic](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/delete-virtual-agent-topic.md)**  
Delete a Virtual Agent topic that is no longer needed.
-   **[Promote or demote LLM conversational subflows, actions, and topics in Assistant Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/promote-demote-va-topics.md)**  
You can promote assets, including conversational subflows, conversational actions, and topics, after associating them with an assistant.
-   **[Conversational settings for assets in the Asset library](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/asset-lib-conv-settings.md)**  
Manage asset settings from the Asset library for individual active assets.
-   **[Managing asset library items](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/managing-asset-library-items.md)**  
The Assistant Designer Asset library supports assets that are created in other tools. Admins must either have privileges to work with those tools, or they must work with team members who do.
-   **[Testing assistants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/testing-enhanced-chat-conversations.md)**  
Simulate and test assistant conversations from Asset library.
-   **[Other Virtual Agent features](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/exploring-other-vad-features.md)**  
After creating topics with the basic Assistant Designer controls and scripting, you can also enhance conversation functionality and topic maintenance by using additional Virtual Agent features.
-   **[Migrating NLU/keyword Virtual Agent topics to LLM topics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/llm-topic-migration.md)**  
The topic migration workflow enables you to migrate your existing Natural Language Understanding \(NLU\)/keyword topics into new large language model \(LLM\) topics.

**Parent Topic:**[Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/virtual-agent-landing-page.md)

