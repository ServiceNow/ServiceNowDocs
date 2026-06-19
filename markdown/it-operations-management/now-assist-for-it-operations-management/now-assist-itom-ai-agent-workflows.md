---
title: Use agentic AI in Now Assist for ITOM
description: Use the IT Operations Management \(ITOM\) agentic workflows to complete tasks autonomously.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/now-assist-for-it-operations-management/now-assist-itom-ai-agent-workflows.html
release: zurich
product: Now Assist for IT Operations Management
classification: now-assist-for-it-operations-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [AI Agents, Agentic AI]
breadcrumb: [Now Assist for ITOM, IT Operations Management]
---

# Use agentic AI in Now Assist for ITOM

Use the IT Operations Management \(ITOM\) agentic workflows to complete tasks autonomously.

<table id="table_n5f_g4v_v2c"><thead><tr><th>

Agentic workflow name

</th><th>

Description

</th><th>

Available AI agents

</th></tr></thead><tbody><tr><td>

Triage and analyze alerts

</td><td>

Triages alerts by updating assignments, analyzing alerts, detecting recurring patterns, and differentiating between noise and real alerts.

</td><td>

-   Alert handling AI Agent
-   Alert analysis AI agent
-   Alert history analysis AI agent
-   Related incidents analysis AI agent
-   Alert verification AI agent

</td></tr><tr><td>

Agent Client Collector \(ACC\) Diagnostic Workflow

</td><td>

Displays error analysis created by Now Assist using generative AI. Error analyses enable asking questions on a specific agent's error or error code.

</td><td>

Agent Client Collector \(ACC\) Diagnostic

</td></tr><tr><td>

Analyze alert impact

</td><td>

Investigates an alert and gives you the context that you need to respond efficiently.

</td><td>

-   Alert impact summary AI agent
-   Alert information retrieval AI agent
-   Observability agents

 For details about observability agents, see [Configure observability agents for Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/now-assist-for-it-operations-management/configure-integration-agents-for-now-assist.md).

</td></tr><tr><td>

Analyze potential impact

</td><td>

Analyzes the potential impact of a change request on relevant servers and suggested services.

</td><td>

Analyze Potential Impact

</td></tr><tr><td>

TLS Certificate renewal

</td><td>

View all certificates about to expire and renew then automatically all at once.

</td><td>

 

</td></tr><tr><td>

Alert grouping recommendations

</td><td>

Provides tag-based group recommendations for selected alerts.

</td><td>

Alert grouping recommendations AI agent

</td></tr><tr><td>

Manage alerts autonomously

</td><td>

Investigates alerts, summarizes alert-related reports, and stores structured insights with key findings in the AI Agent Insight table.

</td><td>

Manage alerts AI agent

</td></tr></tbody>
</table>**Important:** Some Now Assist skills, agents, and agentic workflows are turned on by default. For more information, see .

## AI model providers

You can use Now LLM Service, Now LLM Long Term Stable models \(LTS\), Azure OpenAI, Google Gemini or Anthropic Claude on AWS as the AI model provider for all Now Assist skills and AI agents. Use the Configuration Controls in AI Control Tower to define which options are available, then set the skill-level preferences in the Now Assist Admin console. For more information, see .

## Security

Enable security settings to run AI agents and agentic workflows using Access Control Lists \(ACLs\) and user identities. You can configure and manage the ACLs in AI Agent Studio. See  for more information.

## Installed agents

Looking for an AI agent?

-   There might be AI agents installed with the Now Assist application that are not used in agentic workflows. To learn how to see all agents that are available on your instance, see Find AI agents.
-   To find agents that might not be installed on your instance, visit the [AI Agent Marketplace](https://store.servicenow.com/store/ai-marketplace) on the ServiceNow Store.

Visit the following links to learn about the Now Assist for ITOM agentic workflows.

-   **[Triage and analyze alerts agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/now-assist-for-it-operations-management/itom-alert-triage-agentic-workflow.md)**  
Use the triage and analyze alerts agentic workflow to complete preliminary alert tasks and analysisfor alerts.
-   **[Analyze alert impact agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/now-assist-for-it-operations-management/now-assist-itom-agentic-aia.md)**  
Use the analyze alert impact agentic workflow to investigate an alert and get the context that you need to respond efficiently.
-   **[Agent Client Collector \(ACC\) diagnostic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/now-assist-for-it-operations-management/use-acc-diagnostic-workflow.md)**  
Enable and use AI agents to examine agent behavior through the Agent Client Collector \(ACC\) diagnostic workflow.
-   **[Analyze potential impact agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/now-assist-for-it-operations-management/now-assist-itom-analyze-potential-impact-workflow.md)**  
The analyze potential impact agentic workflow analyzes how a change request might impact servers and suggested services. This analysis helps you make informed decisions about the next steps regarding the change request.
-   **[Now Assist certificate renewal AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/now-assist-for-it-operations-management/now-assist-cert-renewal-ai-agent.md)**  
Using the Now Assist certificate renewal AI agent, see which certificates are about to expire and renew them. Choose a specific certificate and renew it on the spot.
-   **[Pattern diagnostic agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/now-assist-for-it-operations-management/pattern-diagnostic-agentic-workflow.md)**  
The Pattern diagnostic agentic workflow helps Discovery administrators investigate missing CI attributes. It identifies the gap, parses discovery logs, identifies the root cause, and suggests remediation — without manually navigating log files.
-   **[Manage alerts autonomously agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/now-assist-for-it-operations-management/itom-autonomous-operator-workflow.md)**  
Enhance IT operations with AI-driven, autonomous alert management using the manage alerts autonomously agentic workflow.

**Parent Topic:**[Now Assist for IT Operations Management \(ITOM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/now-assist-for-it-operations-management/now-assist-itom.md)

