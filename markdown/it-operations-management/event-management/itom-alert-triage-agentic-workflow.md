---
title: Triage and analyze alerts agentic workflow
description: Use the Triage and analyze alerts agentic workflow to complete preliminary alert tasks and analysis for alerts.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/event-management/itom-alert-triage-agentic-workflow.html
release: brazil
product: Event Management
classification: event-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [AI Agents, Agentic AI]
breadcrumb: [Responding to and working with alerts in Express List, Express List, Event Management, ITOM AIOps, IT Operations Management]
---

# Triage and analyze alerts agentic workflow

Use the Triage and analyze alerts agentic workflow to complete preliminary alert tasks and analysisfor alerts.

## Triage and analyze alerts agentic workflow overview

The Triage and analyze alerts agentic workflow uses AI agents to support alert triage, investigation, and analysis. AI agents can perform the following functions:

-   Acknowledge alerts.
-   Assign alerts to individual users and assignment groups.
-   Summarize alert and alert group data to create a human-readable description and add technical analysis.
-   Investigate relevant past incidents to analyze the significance of the alert and present options for resolution.

**Note:** These functions can also be used for the origin alert of an incident when the workflow is accessed from the incident form or Express List using the ServiceNow Otto panel.

Use the information on this page to learn about the agents related to the Triage and analyze alerts agentic workflow. To modify the Triage and analyze alerts agentic workflow, you must duplicate it and adjust the settings according to your requirements. For more information, see [Duplicate an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/clone-aia-usecase.md).

**Important:** When you modify an agentic workflow, AI agent, or tool, make sure that you update all instructions accordingly.

## Triage and analyze alerts agentic workflow

Acknowledge, assign, and investigate current and past alerts to determine significance and possible resolutions.

To access the agentic workflow, use the ServiceNow Otto panel. For more information about using the agentic workflow in the Now Assist panel, see [ServiceNow Otto panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-panel-overview.md).

## AI agents used in the Triage and analyze alerts agentic workflow

The Triage and analyze alerts agentic workflow uses a team of AI agents to perform preliminary tasks and support alert resolution.

|AI agent|AI agent role|
|--------|-------------|
|Alert handling AI agent|Assign, acknowledge, and maintain an up-to-date alert record.|
|Alert analysis AI agent|Perform alert analysis, and update alert description, when applicable.|
|Alert history analysis AI agent|Analyze past occurrences, assess its significance, and close the alert when applicable.|
|Related incidents analysis AI agent|Analyze past incidents and provide insights on common assignments and summarized resolution notes.|
|Alert verification AI agent|Assess data completeness and determine whether the alert is suitable for analysis.|

