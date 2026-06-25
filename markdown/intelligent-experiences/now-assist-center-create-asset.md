---
title: Create an AI asset in the asset inventory
description: Use the asset library to create AI assets in your instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/now-assist-center-create-asset.html
release: australia
topic_type: task
last_updated: "2026-06-04"
reading_time_minutes: 5
keywords: [Now Assist, Now Assist Center, Gen AI, Generative AI]
breadcrumb: [Using the asset inventory, Use, Now Assist Center, Enable AI experiences]
---

# Create an AI asset in the asset inventory

Use the asset library to create AI assets in your instance.

## Before you begin

Role required: sn\_na\_center.nac\_admin

## About this task

Follow these steps to create an AI asset.

From the asset inventory, asset types are created by opening their respective application.

-   Create agents and agentic workflows with AI Agent Studio.

    For more information, see [AI Agent Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-agent-studio.md).

-   Create Virtual Agent assets with Virtual Agent Assistant Designer, including topics, virtual assistants, subflows, and actions.

    For more information, see .

-   Create custom skills with Now Assist Skill Kit.

    For more information, see [Now Assist Skill Kit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skill-kit/now-assist-skill-kit-landing.md).

-   Create datasets with Now Assist Data Kit.

    For more information, see [Now Assist Data Kit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-data-kit/now-assist-data-kit-landing.md).

-   Create catalog items with Catalog Builder.

    For more information, see [Catalog Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/catalog-builder.md).

-   Create knowledge graphs with Knowledge Graph Designer.

    For more information, see [Knowledge Graph](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/knowledge-graph/knowledge-graph-landing.md).


## Procedure

1.  Navigate to **All** &gt; **Now Assist Center** or **Workspaces** &gt; **Now Assist Center**.

2.  Select **Asset inventory** \(\[Omitted image "icon-now-assist-center-nav-assets.png"\] Alt text: Asset inventory icon.\) in the side navigation bar.

    The Asset inventory tab opens.

3.  Select the **Create asset** button.

    The Create asset box opens showing the following options for the asset type.

    \[Omitted image "now-assist-center-create-asset-2.png"\] Alt text: Create asset box showing options for the new asset type.

<table id="table_ctf_t5d_53c"><thead><tr><th>

Asset type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

AI agent

</td><td>

Opens the New AI Agent form in AI Agent Studio.

 An AI agent is an autonomous digital worker that uses LLMs, tools, and workflows to complete tasks on behalf of users. They can reason, plan, and act independently or collaboratively.

 For more information on creating an AI agent in AI Agent Studio, see [Create an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configure-next-best-action-agent.md).

</td></tr><tr><td>

Agentic workflow

</td><td>

Opens the New agentic workflow form in AI Agent Studio.

 An agentic workflow is a structured sequence of tasks executed by one or more AI agents with minimal human intervention to fulfill a business objective.

 For more information on AI Agent Studio, see [Create an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configure-use-case-ai-agents.md).

</td></tr><tr><td>

Custom skill

</td><td>

Opens the Now Assist Skill Kit home page.

 A skill is a self-contained unit of generative AI functionality that runs a prompt against a large language model \(LLM\) and returns a response.

 For more information, see [Create a skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skill-kit/create-new-skill.md).

</td></tr><tr><td>

Subflow

</td><td>

Opens the New Subflow form in Assistant Designer.

 A subflow is an automated process that is part of a larger automated process. It consists of reusable actions and flow logic, data inputs, and outputs.

 For more information on creating an asset in Virtual Agent Designer, see .

</td></tr><tr><td>

Action

</td><td>

Opens the New Action form in Assistant Designer.

 An action is a single step or task performed by a an AI agent, a workflow, or a subflow.

 For more information on creating an asset in Virtual Agent Designer, see .

</td></tr><tr><td>

Virtual assistant

</td><td>

Opens the Create an assistant page in Assistant Designer.

 A virtual assistant is the container for the end-to-end administrative configuration for a chat or voice conversation.

 For more information on creating a virtual assistant in Assistant Designer, see .

</td></tr><tr><td>

Topic

</td><td>

Opens the Create a topic form in Assistant Designer.

 A conversational topic is used to structure back-and-forth conversations between the virtual agent and the end user.

 For more information on creating an asset in Virtual Agent Designer, see .

</td></tr><tr><td>

Catalog item

</td><td>

Opens the Catalog Builder.

 A catalog item is used to publish a service to users in the Service Catalog.

 For more information on creating a catalog item in Catalog Builder, see [Catalog Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/catalog-builder.md).

</td></tr><tr><td>

Data asset

</td><td>

Opens a **Create data asset** box.

 Choose one of the following options.

-   **Import and create data**

Opens the Create dataset form in Now Assist Data Kit.

-   **Generate synthetic data**

Opens the Now Assist Data Kit home page.

 A custom dataset and data collection in Now Assist Data Kit is used for evaluations in Now Assist Skill Kit.

 For more information on creating a dataset in Now Assist Data Kit, see [Using Now Assist Data Kit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-data-kit/using-now-assist-data-kit.md).

</td></tr><tr><td>

Knowledge Graph

</td><td>

Opens Knowledge Graph Designer home page.

 A knowledge graph is a graphical representation of real-world entities \(tables\) and their relationships. It is used add context and meaning to information to enable intelligent search, insights, and AI-driven experiences.

 For more information on creating a knowledge graph in Knowledge Graph Designer, see [Using Knowledge Graph Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/knowledge-graph/using-knowledge-graph-designer.md).

</td></tr></tbody>
</table>4.  Select the type of asset you want to create.

    Depending on your selection, theapplication will open in a separate browser tab.

5.  Complete the form for the new asset and submit it.


## Result

An asset is created and can be seen in the related asset inventory list.

**Parent Topic:**[Using the asset inventory in Now Assist Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-center-using-asset-inventory.md)

**Related topics**  


[View your AI assets in the asset inventory]()

