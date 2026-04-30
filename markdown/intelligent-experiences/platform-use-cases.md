---
title: Platform agentic workflows
description: You can use the available Now Assist AI agents Platform agentic workflows to achieve business outcomes with self-executing autonomous AI agents.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-02-07"
reading_time_minutes: 1
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

Analyze incident trends

</td><td>

Detects recurring patterns, predicts disruptions, and enables proactive resolutions.

</td><td>

Incident trends analyzer

</td></tr><tr><td>

Classify tasks

</td><td>

Triages tasks by updating fields, evaluating sentiment, and summarizing.

</td><td>

-   Record management AI agent
-   Record field value prediction AI agent

</td></tr><tr><td>

Generate resolution plans

</td><td>

Analyzes tasks, generates resolution summaries, and updates comments or work notes.

</td><td>

-   Next best action recommendation AI agent
-   Record management AI agent
-   Web research and recommendation AI agent

</td></tr><tr><td>

Identify ways to improve services

</td><td>

Analyzes feedback, trends, and metrics and provides recommendations to help optimize processes.

</td><td>

-   Survey requirement collector
-   Survey analyzer

</td></tr><tr><td>

Investigate IT problems

</td><td>

Provides insights from incident or problem details.

</td><td>

Problem investigator

</td></tr><tr><td>

Propose survey responses

</td><td>

Suggests answers for survey questions.

</td><td>

-   Survey filling answer suggester
-   Survey filling data collector

</td></tr></tbody>
</table>**Important:** By default, all agentic workflows and AI agent records are read only.

To run the AI agents autonomously, you must either [activate the agentic workflow template](../task/activate-aia-use-case.md) or [duplicate the agentic workflow](../task/clone-aia-usecase.md), and then proceed with the following steps:

-   Activate the agentic workflow.
-   Activate all agents within the agentic workflow.
-   Activate the trigger to invoke the agentic workflow automatically. If you prefer to invoke it manually, activating the trigger isn’t necessary.

## Tools mapped to AI agents in agentic workflows

To find the tools mapped to AI agents used in the agentic workflows, you can perform the following steps:

-   Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**
-   In the Agentic workflows tab, select the agentic workflow.
-   In the **Describe and connect** step of the guided setup, select the AI agent you want to see the tools for.
-   Go to the **Add tools and information** step.
-   Review the tools mapped to the AI agent.
-   Repeat for all AI agents in the agentic workflow.

