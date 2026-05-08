---
title: Use agentic AI in Now Assist for ITOM
description: Use the IT Operations Management \(ITOM\) agentic workflows to complete tasks autonomously.
locale: en-US
release: australia
product: Now Assist for IT Operations Management
classification: now-assist-for-it-operations-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [AI Agents, Agentic AI]
breadcrumb: [Now Assist for ITOM, IT Operations Management]
---

# Use agentic AI in Now Assist for ITOM

Use the IT Operations Management \(ITOM\) agentic workflows to complete tasks autonomously.

**Note:** Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents. For more information, see ServiceNow product tiers.

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

</td></tr></tbody>
</table>**Important:** Some Now Assist skills, agents, and agentic workflows are turned on by default. For more information, see Now Assist skills, agents, and agentic workflows on by default.

## AI model providers

You can use Now LLM Service, Now LLM Long Term Stable models \(LTS\), Azure OpenAI, Google Gemini or Anthropic Claude on AWS as the AI model provider for all Now Assist skills and AI agents. Use the Configuration Controls in AI Control Tower to define which options are available, then set the skill-level preferences in the Now Assist Admin console. For more information, see Large language models on the ServiceNow AI Platform®.

## Security

Enable security settings to run AI agents and agentic workflows using Access Control Lists \(ACLs\) and user identities. You can configure and manage the ACLs in AI Agent Studio. See Implement access control in Now Assist AI agents for more information.

## Installed agents

There might be AI agents installed with the Now Assist application that are not used in agentic workflows. To learn how to see all agents that are available to you, see Find AI agents.

Visit the following links to learn about the Now Assist for ITOM agentic workflows.

