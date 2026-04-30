---
title: Platform agentic workflows
description: You can use the available Now Assist AI agents Platform agentic workflows to achieve business outcomes with self-executing autonomous AI agents.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2025-02-07"
reading_time_minutes: 3
breadcrumb: [Now Assist agentic workflows, Exploring Now Assist AI agents, Now Assist AI agents, Enable AI experiences]
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

Process emails for tasks

</td><td>

Processes emails and converts them to tasks.

</td><td>

-   Record management AI agent
-   Email action and information AI agent
-   Email to new Task Creation
-   Email on Existing Parent Lead

</td></tr><tr><td>

Suggest survey responses

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

-   **[Platform Analyze incident trends agentic workflow](incident-trends.md)**  
Use the Platform Analyze incident trends AI agents agentic workflow to detect recurring incident patterns so that you can flag and resolve them before they escalate.
-   **[Platform Classify tasks agentic workflow](classify-tasks.md)**  
Use the Platform Classify tasks AI agents agentic workflow to gather relevant information about tasks automatically and make decisions about priorities and assignments.
-   **[Platform Generate resolution plans agentic workflow](resolve-requests.md)**  
Use the Platform Generate resolution plans AI agents agentic workflow to fetch task record details, generate resolution summary steps, and update comments or work notes.
-   **[Platform Identify ways to improve services agentic workflow](service-improvement.md)**  
Use the Platform Identify ways to improve services AI agents agentic workflow to continuously analyze feedback, performance metrics, and historical trends that identify areas for service improvement.
-   **[Platform Investigate IT problems agentic workflow](problem-investigation.md)**  
Use the Platform Investigate IT problem AI agents agentic workflow to perform root cause and risk assessments so that you can create an actionable resolution plan for a problem.
-   **[Platform Process emails for tasks agentic workflow](email-task.md)**  
Use the Platform Process emails for tasks AI agents agentic workflow to process incoming emails and convert them to actionable tasks.
-   **[Platform Suggest survey responses agentic workflow](survey-suggest.md)**  
Use the Platform Suggest survey responses AI agents agentic workflow to assist requesters in filling out surveys for their requests.

**Parent Topic:**[Now Assist agentic workflows](sn-aia-use-cases-list.md)

