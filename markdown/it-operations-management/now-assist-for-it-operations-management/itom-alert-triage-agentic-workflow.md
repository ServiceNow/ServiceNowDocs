---
title: Triage and analyze alerts agentic workflow
description: Use the triage and analyze alerts agentic workflow to complete preliminary alert tasks and analysis for alerts.
locale: en-US
release: zurich
product: Now Assist for IT Operations Management
classification: now-assist-for-it-operations-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
keywords: [AI Agents, agentic AI]
breadcrumb: [Use agentic AI, Now Assist for ITOM, IT Operations Management]
---

# Triage and analyze alerts agentic workflow

Use the triage and analyze alerts agentic workflow to complete preliminary alert tasks and analysisfor alerts.

## Triage and analyze alerts agentic workflow overview

The triage and analyze alerts agentic workflow uses AI agents to support alert triage, investigation, and analysis. AI agents can perform the following functions:

-   Acknowledge alerts.
-   Assign alerts to individual users and assignment groups.
-   Summarize alert and alert group data to create a human-readable description and add technical analysis.
-   Investigate relevant past incidents to analyze the significance of the alert and present options for resolution.

**Note:** These functions can also be used for the origin alert of an incident when the workflow is accessed from the incident form or Express List using the Now Assist panel.

[Role masking](https://www.servicenow.com/docs/access?context=aia-role-masking&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) enables users to limit the roles and privileges of agentic workflows during tool execution. Agentic workflows and their AI agents that get installed with Now Assist applications are assigned pre-defined roles. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. Data access settings must also include these roles. For the instructions to change the security controls, see [Define security controls for an agentic workflow](https://www.servicenow.com/docs/access?context=define-sec-controls-aw&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

Use the information on this page to learn about the agents related to the triage and analyze alerts agentic workflow. To modify the triage and analyze alerts agentic workflow, you must duplicate it and adjust the settings according to your requirements. For more information, see [Duplicate an agentic workflow](https://www.servicenow.com/docs/access?context=clone-aia-usecase&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

**Important:** When you modify an agentic workflow, AI agent, or tool, make sure that you update all instructions accordingly.

## Triage and analyze alerts agentic workflow

Acknowledge, assign, and investigate current and past alerts to determine significance and possible resolutions.

To access the agentic workflow, use the Now Assist panel. For more information about using the agentic workflow in the Now Assist panel, see [Now Assist panel](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

## AI agents used in the triage and analyze alerts agentic workflow

The triage and analyze alerts agentic workflow uses a team of AI agents to perform preliminary tasks and support alert resolution.

|AI agent|AI agent role|
|--------|-------------|
|Alert handling AI agent|Assign, acknowledge, and maintain an up-to-date alert record.|
|Alert analysis AI agent|Perform alert analysis, and update alert description, when applicable.|
|Alert history analysis AI agent|Analyze past occurrences, assess its significance, and close the alert when applicable.|
|Related incidents analysis AI agent|Analyze past incidents and provide insights on common assignments and summarized resolution notes.|
|Alert verification AI agent|Assess data completeness and determine whether the alert is suitable for analysis.|

**Parent Topic:**[Use agentic AI in Now Assist for ITOM](now-assist-itom-ai-agent-workflows.md)

