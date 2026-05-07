---
title: Create an AI asset in the asset inventory
description: Use the asset library to create AI assets in your instance.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-04-01"
reading_time_minutes: 3
keywords: [Now Assist, Now Assist Center, Gen AI, Generative AI]
breadcrumb: [Using the asset inventory, Use, Now Assist Center, Enable AI experiences]
---

# Create an AI asset in the asset inventory

Use the asset library to create AI assets in your instance.

## Before you begin

Role required: sn\_na\_center.nac\_admin

## About this task

Follow these steps to create an AI asset.

You can create agents and agentic workflows by opening AI Agent Studio from the asset library. For more information on AI Agent Studio, see [AI Agent Studio](../../now-assist-ai-agents/concept/ai-agent-studio.md).

Other asset types are created using Virtual Agent Assistant Designer. Virtual Agent conversations are built using topics. Conversations can also include subflows and actions. For more information on Assistant Designer, see [Assistant Designer](https://www.servicenow.com/docs/access?context=assistant-designer&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **Now Assist Center** or **Workspaces** &gt; **Now Assist Center**.

2.  Select **Asset inventory** \(![Asset inventory icon.](../image/icon-now-assist-center-nav-assets.png)\) in the side navigation bar.

    The Asset inventory tab opens.

3.  Select the **Create asset** button.

    The Create asset box opens showing the following options for the asset type.

    ![Create asset box showing options for the new asset type.](../image/now-assist-center-create-asset.png)

<table id="table_ctf_t5d_53c"><thead><tr><th>

Asset type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

AI agent

</td><td>

Opens the New AI Agent form in AI Agent Studio.

 An AI agent is an autonomous digital worker that uses LLMs, tools, and workflows to complete tasks on behalf of users. They can reason, plan, and act independently or collaboratively.

 For more information on creating an AI agent in AI Agent Studio, see [Create an AI agent](../../now-assist-ai-agents/task/configure-next-best-action-agent.md).

</td></tr><tr><td>

Agentic workflow

</td><td>

Opens the New agentic workflow form in AI Agent Studio.

 An agentic workflow is a structured sequence of tasks executed by one or more AI agents with minimal human intervention to fulfill a business objective.

 For more information on AI Agent Studio, see [Create an agentic workflow](../../now-assist-ai-agents/task/configure-use-case-ai-agents.md).

</td></tr><tr><td>

Topic

</td><td>

Opens the Create a topic form in Assistant Designer.

 A conversational topic is used to structure back-and-forth conversations between the virtual agent and the end user.

 For more information on creating an asset in Virtual Agent Designer, see [Getting started with Virtual Agent Designer](https://www.servicenow.com/docs/access?context=conversation-designer-virtual-agent&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US).

</td></tr><tr><td>

Subflow

</td><td>

Opens the New Subflow form in Assistant Designer.

 A subflow is an automated process that is part of a larger automated process. It consists of reusable actions and flow logic, data inputs, and outputs.

 For more information on creating an asset in Virtual Agent Designer, see [Getting started with Virtual Agent Designer](https://www.servicenow.com/docs/access?context=conversation-designer-virtual-agent&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US).

</td></tr><tr><td>

Action

</td><td>

Opens the New Action form in Assistant Designer.

 An action is a single step or task performed by a an AI agent, a workflow, or a subflow.

 For more information on creating an asset in Virtual Agent Designer, see [Getting started with Virtual Agent Designer](https://www.servicenow.com/docs/access?context=conversation-designer-virtual-agent&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US).

</td></tr></tbody>
</table>4.  Select the type of asset you want to create.

    Depending on your selection, the AI Agent Studio or Assistant Designer will open in a separate browser tab.

5.  Complete the form for the new asset and submit it.


## Result

An asset is created and can be seen in the related asset inventory list.

**Parent Topic:**[Using the asset inventory in Now Assist Center](../concept/now-assist-center-using-asset-inventory.md)

**Related topics**  


[View your AI assets in the asset inventory](now-assist-center-view-ai-assets.md)

