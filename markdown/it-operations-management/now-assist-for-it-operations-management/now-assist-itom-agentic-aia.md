---
title: Analyze alert impact agentic workflow
description: Use the analyze alert impact agentic workflow to investigate an alert and get the context that you need to respond efficiently.
locale: en-US
release: zurich
product: Now Assist for IT Operations Management
classification: now-assist-for-it-operations-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Use agentic AI, Now Assist for ITOM, IT Operations Management]
---

# Analyze alert impact agentic workflow

Use the analyze alert impact agentic workflow to investigate an alert and get the context that you need to respond efficiently.

## Analyze alert impact agentic workflow overview

The analyze alert impact agentic workflow uses AI agents to interact with observability tools, such as Dynatrace, Kentik, and New Relic. The agents surface information to help you do the following:

-   Understand the severity and impact of alerts.
-   Find potential root causes using insights, such as recent deployments.
-   Identify ownership by surfacing relevant services and responsible teams.
-   Support stakeholder communication with clear, actionable information.

Use the information on this page to learn about the agents related to the analyze alert impact agentic workflow. To modify the analyze alert impact agentic workflow, [duplicate it](https://www.servicenow.com/docs/access?context=clone-aia-usecase&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) and adjust the settings.

**Important:** When you modify an agentic workflow, AI agent, or tool, make sure that you update all instructions accordingly.

## Analyze alert impact agentic workflow

Investigate an alert and get insights into its severity, impact, ownership, and root causes.

To access the agentic workflow in AI Agent Studio:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.
2.  Select **Analyze alert impact**.

The Analyze alert impact page lets you manage the agentic workflow, including defining key requirements, defining security controls, and adding triggers.Navigate to Select channels and status to turn on the agentic workflow in the Now Assist panel.

## AI agents used in the analyze alert impact agentic workflow

The analyze alert impact agentic workflow uses observability AI agents to gather information from alerts and request insights. The observability AI agents require additional configuration. For more information, see [Configuring agents and skills for Now Assist for ITOM](itom-ai-agent-configuration.md).

**Important:** Before using the analyze alert impact agentic workflow, activate its AI agents. In AI Agent Studio, find the agents in Create and manage, and turn on the AI agents in the Select channels and status screen.

<table id="table_vyp_stk_x2c"><thead><tr><th>

AI agent

</th><th>

AI agent role

</th></tr></thead><tbody><tr><td>

Alert impact summary AI agent

</td><td>

Retrieves the alert impact summary for a specific alert.

</td></tr><tr><td>

Alert information retrieval AI agent

</td><td>

Gathers key observability details for a specific alert.

</td></tr><tr><td>

Dynatrace analysis AI agent

</td><td>

Gathers insights from Dynatrace about possible root causes, impacted entities, and impacted environments.

</td></tr><tr><td>

Dynatrace Model Context Protocol \(MCP\) server agent

</td><td>

Provides detailed analysis of Dynatrace alerts, including insights about logs, topology, recent changes, root causes, impacted entities, and environments.MCP is an open-source standard that lets AI models connect with other tools for deeper insights.

</td></tr><tr><td>

Kentik analysis AI agent

</td><td>

Gathers insights from Kentik about service network performance, connectivity, DDOS attacks, and anomalies.

</td></tr><tr><td>

New Relic analysis AI agent

</td><td>

Gathers insights from New Relic about alert impact, including service and user impact, root cause theories, and responsible teams.

</td></tr></tbody>
</table>## Generating the alert analysis

In the agentic workflow record:

1.  Review the information in the Define key requirements, Define security controls, and Add triggers screens, make the necessary updates, and then select **Continue**.
2.  In the Select channels and status screen:
    1.  Turn on the Now Assist panel display.
    2.  Select **Save and test**.
3.  Test the agentic workflow by asking a question, for example, `What is the impact of Alert0010056NR?`
4.  Select **Continue to Test Chat Response**.

    The page shows the chat responses, visualizes the AI agents involved, and lists the AI agent decision logs.


In AI Agent Studio, you get notified when the analysis is generated. You can then act on the information or ask more questions about the alert. For more information about using the agentic workflow in the Now Assist panel, see [Use the analyze alert impact agentic workflow](../task/now-assist-itom-use-aia.md).

-   **[Use the analyze alert impact agentic workflow](../task/now-assist-itom-use-aia.md)**  
Learn how to use the analyze alert impact agentic workflow in the Now Assist panel. The agentic workflow helps you investigate an alert and get the context that you need to respond efficiently.

**Parent Topic:**[Use agentic AI in Now Assist for ITOM](now-assist-itom-ai-agent-workflows.md)

