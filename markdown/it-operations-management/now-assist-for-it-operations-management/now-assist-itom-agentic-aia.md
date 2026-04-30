---
title: Analyze alert impact agentic workflow
description: Use the Analyze alert impact agentic workflow to investigate an alert and get the context that you need to respond efficiently.
locale: en-US
release: xanadu
product: Now Assist for IT Operations Management
classification: now-assist-for-it-operations-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
keywords: [AI Agents, Agentic AI]
breadcrumb: [Using agentic workflows in Now Assist for IT Operations Management \(ITOM\), Now Assist for IT Operations Management \(ITOM\), IT Operations Management]
---

# Analyze alert impact agentic workflow

Use the Analyze alert impact agentic workflow to investigate an alert and get the context that you need to respond efficiently.

## Analyze alert impact agentic workflow overview

The Analyze alert impact agentic workflow uses AI agents to interact with observability tools, such as Dynatrace, Kentik, and New Relic. It also includes AIOps AI agents that analyze service, user, and business impact. Together, the agents surface information to help you do the following:

-   Understand the severity and impact of alerts.
-   Find potential root causes using insights, such as recent deployments.
-   Identify ownership by surfacing relevant services and responsible teams.
-   Support stakeholder communication with clear, actionable information.

Use the information on this page to learn about the agents related to the Analyze alert impact agentic workflow. To modify the Analyze alert impact agentic workflow, [duplicate it](https://www.servicenow.com/docs/access?context=clone-aia-usecase&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US) and adjust the settings.

**Important:** When you modify an agentic workflow, AI agent, or tool, make sure that you update all instructions accordingly.

## Analyze alert impact agentic workflow

Investigate an alert and get insights into its severity, business and service impact, ownership, and root causes.

To access the agentic workflow in AI Agent Studio:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.
2.  Select **Analyze alert impact**.

The Analyze alert impact page lets you manage the agentic workflow, including defining key requirements, adding a preferred trigger, and selecting a UI display. Navigate to Select a UI display to turn on the agentic workflow in the Now Assist panel.

## AI agents used in the Analyze alert impact agentic workflow

The Analyze alert impact agentic workflow uses AIOps and observability AI agents to gather information from alerts and request insights. Only the observability AI agents require additional configuration. For more information, see [Configuring AI agents for Now Assist for ITOM](itom-ai-agent-configuration.md).

**Important:** Before using the Analyze alert impact agentic workflow, activate its AI agents. In AI Agent Studio, find the AI agents in Create and manage, and turn on the AI agents in the Define key requirements screen.

|AI agent|AI agent role|
|--------|-------------|
|Alert impact verification AI agent|Validates the user’s question and extracts a single alert to analyze.|
|Alert information retrieval AI agent|Gathers key observability details for a specific alert.|
|Business and technology management service impact analysis AI agent|Analyzes impact by mapping application services to business and technical services using Service Portfolio data.|
|Dynatrace analysis AI agent|Gathers insights from Dynatrace about possible root causes, impacted entities, and impacted environments.|
|Kentik analysis AI agent|Gathers insights from Kentik about service network performance, connectivity, DDOS attacks, and anomalies.|
|New Relic analysis AI agent|Gathers insights from New Relic about alert impact, including service and user impact, root cause theories, and responsible teams.|
|Service instance impact analysis AI agent|Analyzes how the alert affects the associated service instance.|
|User impact analysis AI agent|Identifies issues linked to the affected services and presents a summarized overview to the user.|

## Generating the alert analysis

In the agentic workflow record:

1.  Review the information in the Describe key requirements screen and Add a preferred trigger screen, make the necessary updates, and then select **Continue**.
2.  In the Select a UI display screen:
    1.  Turn on the Now Assist panel display.
    2.  Select **Save and test**.
3.  Test the agentic workflow by asking a question, for example, `What is the impact of Alert0010007?`
4.  Select **Start test**.

    **Example of an Analyze alert impact agentic workflow output in the ServiceNow AI Agent Studio**![Analyze alert impact output shows chat responses and visualizes the AI agents involved.](../image/Analyze-alert-updated-output.png)


In the AI Agent Studio, you get notified when the analysis is generated. You can then act on the information or ask more questions about the alert. For more information about using the agentic workflow in the Now Assist panel, see [Use the Analyze alert impact agentic workflow](../task/now-assist-itom-use-aia.md).

-   **[Use the Analyze alert impact agentic workflow](../task/now-assist-itom-use-aia.md)**  
Learn how to use the Analyze alert impact agentic workflow in the Now Assist panel. The agentic workflow helps you investigate an alert and get the context that you need to respond efficiently.

**Parent Topic:**[Using agentic workflows in Now Assist for IT Operations Management \(ITOM\)](now-assist-itom-ai-agent-workflows.md)

**Previous topic:**[Triage and analyze alerts agentic workflow](itom-alert-triage-agentic-workflow.md)

**Next topic:**[Use the Analyze alert impact agentic workflow](../task/now-assist-itom-use-aia.md)

