---
title: Use agentic AI in Now Assist for ITOM
description: Use the IT Operations Management \(ITOM\) agentic workflows to complete tasks autonomously.
locale: en-US
release: zurich
product: Now Assist for IT Operations Management
classification: now-assist-for-it-operations-management
topic_type: concept
last_updated: "2025-08-21"
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
-   Dynatrace analysis AI agent
-   Dynatrace MCP server agent
-   Kentik analysis AI agent
-   New Relic analysis AI agent

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
</table>**Important:** Some Now Assist skills, agents, and agentic workflows are turned on by default. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

## AI model providers

You can use Now LLM Service, Now LLM Long Term Stable models \(LTS\), Azure OpenAI, Google Gemini or Anthropic Claude on AWS as the AI model provider for all Now Assist skills and AI agents. Use the Configuration Controls in [AI Control Tower](https://www.servicenow.com/docs/access?context=ai-model-providers&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) to define which options are available, then set the skill-level preferences in the [Now Assist Admin console](https://www.servicenow.com/docs/access?context=manage-large-language-models&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US). For more information, see [Large language models on the ServiceNow AI Platform®](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

## Security

Enable security settings to run AI agents and agentic workflows using Access Control Lists \(ACLs\) and user identities. You can configure and manage the ACLs in AI Agent Studio. See [Implement access control in Now Assist AI agents](https://www.servicenow.com/docs/access?context=aia-security-implementation&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) for more information.

## Installed agents

Looking for an AI agent?

-   There might be AI agents installed with the Now Assist application that are not used in agentic workflows. To learn how to see all agents that are available on your instance, see [Find AI agents](https://www.servicenow.com/docs/access?context=find-ai-agents&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).
-   To find agents that might not be installed on your instance, visit the [AI Agent Marketplace](https://store.servicenow.com/store/ai-marketplace) on the ServiceNow Store.

Visit the following links to learn about the Now Assist for ITOM agentic workflows.

-   **[Triage and analyze alerts agentic workflow](itom-alert-triage-agentic-workflow.md)**  
Use the triage and analyze alerts agentic workflow to complete preliminary alert tasks and analysisfor alerts.
-   **[Analyze alert impact agentic workflow](now-assist-itom-agentic-aia.md)**  
Use the analyze alert impact agentic workflow to investigate an alert and get the context that you need to respond efficiently.
-   **[Agent Client Collector \(ACC\) diagnostic workflow](../task/use-acc-diagnostic-workflow.md)**  
Enable and use AI agents to examine agent behavior through the Agent Client Collector \(ACC\) diagnostic workflow.
-   **[Analyze potential impact agentic workflow](now-assist-itom-analyze-potential-impact-workflow.md)**  
The analyze potential impact agentic workflow analyzes how a change request might impact servers and suggested services. This analysis helps you make informed decisions about the next steps regarding the change request.
-   **[Now Assist certificate renewal AI agent](../../it-operations-management/concept/now-assist-cert-renewal-ai-agent.md)**  
Using the Now Assist certificate renewal AI agent, see which certificates are about to expire and renew them. Choose a specific certificate and renew it on the spot.
-   **[Manage alerts autonomously agentic workflow](itom-autonomous-operator-workflow.md)**  
Enhance IT operations with AI-driven, autonomous alert management using the manage alerts autonomously agentic workflow.

**Parent Topic:**[Now Assist for IT Operations Management \(ITOM\)](now-assist-itom.md)

