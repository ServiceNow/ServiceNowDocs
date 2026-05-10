---
title: Manage alerts autonomously agentic workflow
description: Enhance IT operations with AI-driven, autonomous alert management using the manage alerts autonomously agentic workflow.
locale: en-US
release: australia
product: Now Assist for IT Operations Management
classification: now-assist-for-it-operations-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [AI Agents, agentic AI]
breadcrumb: [Use agentic AI, Now Assist for ITOM, IT Operations Management]
---

# Manage alerts autonomously agentic workflow

Enhance IT operations with AI-driven, autonomous alert management using the manage alerts autonomously agentic workflow.

## Manage alerts autonomously agentic workflow overview

The manage alerts autonomously workflow introduces a unified AI-driven process that significantly streamlines alert management and reduces resolution times. This workflow supports alert management in the following ways:

-   Automates the triage
-   Impact analysis
-   Root cause investigation of IT alerts
-   Generates reports, summarizes key insights and possible next steps

For information on how to review key insights and data derived from the workflow in Express List, see [Review AI generated alert information and insights in Express List](../task/use-ai-insights-express-list.md).

For information about configuring this workflow, see [Configure the manage alerts autonomously agentic workflow](../task/configure-manage-alerts-autonomously-workflow.md).

Use the information on this page to learn about the actions related to the manage alerts autonomously agentic workflow. To modify the workflow, you must duplicate it and adjust the settings according to your requirements. For more information, see [Duplicate an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/clone-aia-usecase.md).

**Important:** When you modify an agentic workflow, AI agent, or tool, make sure that you update all instructions accordingly.

## Manage alerts autonomously agentic workflow

The manage alerts autonomously agentic workflow uses the manage alerts AI agent to perform alert management and resolution tasks.

|AI agent|AI agent role|
|--------|-------------|
|Manage alerts AI agent|Investigates alerts, summarizes alert-related reports, and stores structured insights with key findings.|

The manage alerts autonomously agentic workflow performs several actions in the course of the workflow. These actions may include the following:

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
    -   Analyzes non-primary log analytics alerts in an alert group to support investigation, including the following:
        -   Classifies alerts as proactive or reactive, indicating emerging risk or an active issue
        -   Assess if triage is required
        -   Provides contextual insights, including potential failure scenarios and what may occur if the alert isn't addressed
-   Summarizes and stores information
    -   Consolidates findings
    -   Generates a final summary
    -   Saves the summaries in the alert record, such as
        -   reasoning, evidence, and confidence level behind AI-driven investigation of alert significance and automatic closure of insignificant alerts, and
        -   summaries of Service Observability dashboards to provide health analysis of each service associated with an alert. For more information see, [Analyze service health in Service Observability](analyze-service-health-in-service-observability.md).
    -   Provides clear, actionable insights

**Important:** This agentic workflow is turned on by default. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills/now-assist-skills-on-by-default.md).

