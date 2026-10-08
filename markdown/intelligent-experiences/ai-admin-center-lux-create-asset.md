---
title: Create an asset in AI Admin Center \(Lux UI\)
description: Use the asset library to create AI assets in your instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/ai-admin-center-lux-create-asset.html
release: brazil
topic_type: task
last_updated: "2026-10-02"
reading_time_minutes: 7
keywords: [AI Admin Center, Now Assist Center, AI, AI setup]
breadcrumb: [Managing AI assets, Setting up AI capabilities and configurations, AI Admin Center, Getting started with AI, Enable AI Experiences]
---

# Create an asset in AI Admin Center \(Lux UI\)

Use the asset library to create AI assets in your instance.

**Important:** Lux is the new user experience for AI Admin Center. For more information on the Lux experience, see [AI Admin Center user experience \(Lux UI\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/ai-admin-center-lux-user-experience.md).

The Next Experience AI Admin Center workspace is being prepared for deprecation in the November store release and will no longer be supported. For more information on the Next Experience UI, see [AI Admin Center workspace \(Next Experience UI\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-center-workspace.md).

In AI Admin Center version 6.1, the Next Experience and Lux user interfaces are both available.

## Before you begin

Role required: sn\_na\_center.nac\_admin

## About this task

Follow these steps to create an AI asset.

**Note:** This topic describes the AI Admin Center feature based on the Lux user interface \(UI\). If you're using the Next Experience UI for AI Admin Center, see the Next Experience UI version of this topic.

From the asset library, asset types are created by opening their respective application.

-   Create intents in AI Admin Center.
-   Create agents and agentic workflows with AI Agent Studio.

    For more information, see [AI Agent Studio overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/ai-agent-studio.md).

-   Create Virtual Agent assets with Assistant Designer, including topics, virtual assistants, subflows, and actions.

    For more information, see [Assistant Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/assistant-designer.md).

-   Create custom skills with AI Skill Kit.

    For more information, see [AI Skill Kit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-skill-kit/now-assist-skill-kit-landing.md).

-   Create datasets with AI Data Kit or in AI Admin Center.

    For more information, see [AI Data Kit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-data-kit/now-assist-data-kit-landing.md).

-   Create catalog items with Catalog Builder.

    For more information, see [Catalog Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/catalog-builder.md).

-   Create knowledge graphs with Knowledge Graph Designer.

    For more information, see [Knowledge Graph](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/knowledge-graph/knowledge-graph-landing.md).


## Procedure

1.  Navigate to **All** &gt; **AI Admin Center** &gt; **Home** or **Admin** &gt; **AI Admin Center**.

2.  Select **Asset library** \(\[Omitted image "icon-aiac-lux-nav-inventory.png"\] Alt text: Asset library icon.\) in the side navigation panel.

    The Asset library page opens showing tabs for the various asset types.

3.  Select the **Create asset** button.

    The Create asset box opens showing the following options for the asset type.

    \[Omitted image "ai-admin-center-lux-create-asset.png"\] Alt text: Create asset box showing options for the new asset type.

<table id="table_lux_create_asset"><thead><tr><th>

Asset type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

AI agent

</td><td>

Opens the New AI Agent form in AI Agent Studio.

 An AI agent is an autonomous digital worker that uses LLMs, tools, and workflows to complete tasks on behalf of users. They can reason, plan, and act independently or collaboratively.

 For more information on creating an AI agent in AI Agent Studio, see [Create an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/configure-next-best-action-agent.md).

</td></tr><tr><td>

Agentic workflow

</td><td>

Opens the New agentic workflow form in AI Agent Studio.

 An agentic workflow is a structured sequence of tasks executed by one or more AI agents with minimal human intervention to fulfill a business objective.

 For more information on AI Agent Studio, see [Create an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/configure-use-case-ai-agents.md).

</td></tr><tr><td>

Custom skill

</td><td>

Opens the AI Skill Kit home page.

 A skill is a self-contained unit of generative AI functionality that runs a prompt against a large language model \(LLM\) and returns a response.

 For more information, see [Create a skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-skill-kit/create-new-skill.md).

</td></tr><tr><td>

Intent

</td><td>

Opens the New intent form in AI Admin Center.

 An intent is a data record that captures and defines what a user is trying to accomplish in a chat request. Intent records help the system classify, understand, and route user input appropriately.

 For more information, see [Create an intent in AI Admin Center \(Lux UI\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/ai-admin-center-lux-create-intent.md).

</td></tr><tr><td>

Subflow

</td><td>

Opens the New Subflow form in Assistant Designer.

 A subflow is an automated process that is part of a larger automated process. It consists of reusable actions and flow logic, data inputs, and outputs.

 For more information on creating an asset with the Assistant Designer asset library, see [Build conversations in the Asset library in Assistant Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/conversation-designer-virtual-agent.md).

</td></tr><tr><td>

Action

</td><td>

Opens the New Action form in Assistant Designer.

 An action is a single step or task performed by an AI agent, a workflow, or a subflow.

 For more information on creating an asset with the Assistant Designer asset library, see [Build conversations in the Asset library in Assistant Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/conversation-designer-virtual-agent.md).

</td></tr><tr><td>

Virtual assistant

</td><td>

Opens the Create an assistant page in Assistant Designer.

 A virtual assistant is the container for the end-to-end administrative configuration for a chat or voice conversation.

 For more information on creating a virtual assistant in Assistant Designer, see [Assistants overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/configure-now-assist-va.md).

</td></tr><tr><td>

Topic

</td><td>

Opens the Create a topic form in Assistant Designer.

 A conversational topic is used to structure back-and-forth conversations between the virtual agent and the end user.

 For more information on creating an asset with the Assistant Designer asset library, see [Build conversations in the Asset library in Assistant Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/conversation-designer-virtual-agent.md).

</td></tr><tr><td>

Catalog item

</td><td>

Opens the Catalog Builder.

 A catalog item is used to publish a service to users in the Service Catalog.

 For more information on creating a catalog item in Catalog Builder, see [Catalog Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/catalog-builder.md).

</td></tr><tr><td>

Data asset

</td><td>

A custom dataset and data collection in AI Data Kit is used for evaluations in AI Skill Kit.

 Select **AI Data Kit** to go to the AI Data Kit home page. For more information on creating a dataset in AI Data Kit, see [Using AI Data Kit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-data-kit/using-now-assist-data-kit.md).

 Select **Data asset** to create the asset in AI Admin Center. For more information on creating a dataset with AI Admin Center, see [Create a data asset in AI Admin Center \(Lux UI\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/ai-admin-center-lux-create-data-asset.md).

</td></tr><tr><td>

Knowledge graph

</td><td>

Opens Knowledge Graph Designer home page.

 A knowledge graph is a graphical representation of real-world entities \(tables\) and their relationships. It's used to add context and meaning to information to enable intelligent search, insights, and AI-driven experiences.

 For more information on creating a knowledge graph in Knowledge Graph Designer, see [Using Knowledge Graph Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/knowledge-graph/using-knowledge-graph-designer.md).

</td></tr></tbody>
</table>4.  Select the type of asset you want to create.

    Depending on your selection, the application opens in a separate browser tab.

5.  Complete the form for the new asset and submit it.


## Result

An asset is created and can be seen in the related asset library list.

**Parent Topic:**[Managing AI assets in AI Admin Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-center-using-asset-inventory.md)

**Related topics**  


[View your AI assets in the asset inventory \(Next Experience UI\)]()

[View your AI assets in the asset library \(Lux UI\)]()

[Create an asset in the AI asset inventory \(Next Experience UI\)]()

[Create an intent in AI Admin Center \(Lux UI\)]()

[Edit an intent in AI Admin Center \(Lux UI\)]()

[Create a data asset in AI Admin Center \(Lux UI\)]()

