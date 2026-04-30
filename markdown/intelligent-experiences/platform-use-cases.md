---
title: Platform agentic workflows
description: You can use the available Now Assist AI agents Platform agentic workflows to achieve business outcomes with self-executing autonomous AI agents.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-09-17"
reading_time_minutes: 2
breadcrumb: [Now Assist agentic workflows, Now Assist AI assets, Enable AI experiences]
---

# Platform agentic workflows

You can use the available Now Assist AI agents Platform agentic workflows to achieve business outcomes with self-executing autonomous AI agents.

Use the following agentic workflows that are available with ServiceNow AI Platform.

<table><thead><tr><th>

Agentic workflow name

</th><th>

Description

</th><th>

Available AI agents

</th></tr></thead><tbody><tr><td>

Analyze task trends

</td><td>

Detects recurring patterns, predicts disruptions, and enables proactive resolutions with actionable recommendations.

</td><td>

Issue trend analysis AI Agent

</td></tr><tr><td>

Classify tasks

</td><td>

Triages tasks by updating fields, evaluating sentiment, and summarizing.

</td><td>

Record field value prediction AI agent

</td></tr><tr><td>

Generate my work plan

</td><td>

Provides a personalized work plan based on current work and historical data of previous work.

</td><td>

Prioritize work AI agent

</td></tr><tr><td>

Generate resolution plan

</td><td>

Analyzes tasks, generates resolution summaries, and updates comments or work notes.

</td><td>

-   Next best action recommendation AI agent
-   Resolution Action AI Agent

</td></tr><tr><td>

Help optimize team productivity

</td><td>

Identifies backlog items, evaluates team member performance on previous assignments, and allocates work based on similarity to those previous assignments.

</td><td>

Work Allocator AI Agent

</td></tr><tr><td>

Identify ways to improve service

</td><td>

Analyzes feedback, trends, and metrics and provides recommendations to help optimize processes.

</td><td>

Survey Analysis AI agent

</td></tr><tr><td>

Investigate problems

</td><td>

Provides insights from incident or problem details.

</td><td>

Problem investigation AI agent

</td></tr><tr><td>

Process images for tasks

</td><td>

Processes images and converts them to tasks.

</td><td>

-   Image Processor Agent
-   Document and visual insights AI agent

</td></tr><tr><td>

Propose survey responses

</td><td>

Suggests answers for survey questions.

</td><td>

-   Survey response suggestion AI agent
-   Survey filling data collection AI agent

</td></tr></tbody>
</table>**Important:** By default, all agentic workflows and AI agent records are read only.

To run the AI agents autonomously, you must either [activate the agentic workflow template](../task/activate-aia-use-case.md) or [duplicate the agentic workflow](../task/clone-aia-usecase.md), and then proceed with the following steps:

-   Activate the agentic workflow.
-   Activate all agents within the agentic workflow.
-   Activate the trigger to invoke the agentic workflow automatically. If you prefer to invoke it manually, activating the trigger isn’t necessary.

## Tools mapped to AI agents in agentic workflows

To find the tools mapped to AI agents used in the agentic workflows, you can perform the following steps:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**
2.  In the Agentic workflows tab, select the agentic workflow.
3.  In the **Describe and connect** step of the guided setup, select the AI agent you want to see the tools for.
4.  Go to the **Add tools and information** step.
5.  Review the tools mapped to the AI agent.
6.  Repeat for all AI agents in the agentic workflow.

## Agentic workflows and UI actions

To enable users to access agentic workflows with UI actions, you can open the agentic workflow in AI Agent Studio and navigate to the **Select channels and access** step. You can select a UI action as a possible way to access the workflow

If you don't see your UI actions after configuring it in AI Agent Studio, ensure that the property **com.glide.agentic\_processes\_view.enabled** is set to `true`.

Looking for an AI agent?

-   There might be AI agents installed with the Now Assist application that are not used in agentic workflows. To learn how to see all agents that are available on your instance, see [Find AI agents](../task/find-ai-agents.md).
-   To find agents that might not be installed on your instance, visit the [AI Agent Marketplace](https://store.servicenow.com/store/ai-marketplace) on the ServiceNow Store.

