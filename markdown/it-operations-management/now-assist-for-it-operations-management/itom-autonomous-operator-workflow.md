---
title: Manage alerts autonomously agentic workflow
description: Enhance IT operations with AI-driven, autonomous alert management using the manage alerts autonomously agentic workflow.
locale: en-US
release: yokohama
product: Now Assist for IT Operations Management
classification: now-assist-for-it-operations-management
topic_type: concept
last_updated: "2025-12-10"
reading_time_minutes: 3
keywords: [AI Agents, agentic AI]
breadcrumb: [Using agentic workflows in Now Assist for ITOM, Now Assist for ITOM, IT Operations Management]
---

# Manage alerts autonomously agentic workflow

Enhance IT operations with AI-driven, autonomous alert management using the manage alerts autonomously agentic workflow.

## Manage alerts autonomously agentic workflow overview

**Important:** This agentic workflow is turned on by default. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

The manage alerts autonomously workflow introduces a unified AI-driven process that significantly streamlines alert management and reduces resolution times. This workflow supports alert management in the following ways:

-   automates the triage
-   impact analysis
-   root cause investigation of IT alerts
-   generates reports, summarizes key insights and possible next steps.

For information on how to review key insights and data derived from the workflow in Express List, see [Review AI generated alert information and insights in Express List](../task/use-ai-insights-express-list.md).

For information about configuring this workflow, see [Configure the manage alerts autonomously agentic workflow](../task/configure-manage-alerts-autonomously-workflow.md).

Use the information on this page to learn about the actions related to the manage alerts autonomously agentic workflow. To modify the workflow, you must duplicate it and adjust the settings according to your requirements. For more information, see [Duplicate an agentic workflow](https://www.servicenow.com/docs/access?context=clone-aia-usecase&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

**Important:** When you modify an agentic workflow, AI agent, or tool, make sure that you update all instructions accordingly.

## Manage alerts autonomously agentic workflow

The manage alerts autonomously agentic workflow uses the manage alerts AI agent to perform alert management and resolution tasks.

|AI agent|AI agent role|
|--------|-------------|
|Manage alerts AI agent|Investigates alerts, summarizes alert-related reports, and stores structured insights with key findings.|

The manage alerts autonomously agentic workflow performs several actions in the course of the workflow. These actions may include:

-   Triages alerts
    -   Evaluates and categorizes alert
    -   Analyzes alert history to identify noise patterns
    -   Updates alert group description based on analysis
    -   Performs related incidents analysis to detect focal points and common closure patterns
-   Determines alert impact
    -   Evaluates impact on services
    -   Determines user impact by finding recent incidents or cases
    -   Uses observability skills for deeper service state validation
-   Investigates relevant information
    -   Retrieves and summarizes similar closed alerts
    -   Analyzes recent changes for causal relationships
    -   Summarizes related KB articles for relevant information
    -   Identifies trends or anomalies in related metrics
    -   Uncovers errors, exceptions, or warnings in related logs
-   Summarizes and stores information
    -   Consolidates findings
    -   Generates a final summary
    -   Saves the summary in the alert record
    -   Provides clear, actionable insights

**Important:** This agentic workflow is turned on by default. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

-   **[Review AI generated alert information and insights in Express List](../task/use-ai-insights-express-list.md)**  
Access alert information in Express List that is consolidated autonomously by AI skills and agents. Use the AI insights badge, column, and filter to monitor alert statuses and review of AI-generated insights.

**Parent Topic:**[Using agentic workflows in Now Assist for IT Operations Management \(ITOM\)](now-assist-itom-ai-agent-workflows.md)

**Previous topic:**[Use the Analyze potential impact agentic workflow to assess a change request](../task/use-now-assist-analyze-impact-agentic-workflow.md)

**Next topic:**[Review AI generated alert information and insights in Express List](../task/use-ai-insights-express-list.md)

