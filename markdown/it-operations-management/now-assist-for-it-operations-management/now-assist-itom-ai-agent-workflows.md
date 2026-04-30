---
title: Using agentic workflows in Now Assist for IT Operations Management \(ITOM\)
description: Use the IT Operations Management \(ITOM\) agentic workflows to complete tasks autonomously.
locale: en-US
release: xanadu
product: Now Assist for IT Operations Management
classification: now-assist-for-it-operations-management
topic_type: concept
last_updated: "2025-03-31"
reading_time_minutes: 2
keywords: [AI Agents, Agentic AI]
breadcrumb: [Now Assist for IT Operations Management \(ITOM\), IT Operations Management]
---

# Using agentic workflows in Now Assist for IT Operations Management \(ITOM\)

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

Analyze alert impact

</td><td>

Investigates an alert and gives you the context that you need to respond efficiently.

</td><td>

-   Alert information retrieval AI agent
-   Alert impact verification AI agent
-   Business and technology management service impact analysis AI agent
-   Dynatrace analysis AI agent
-   Kentik analysis AI agent
-   New Relic analysis AI agent
-   Service instance impact analysis AI agent
-   User impact analysis AI agent

</td></tr></tbody>
</table>**Important:** By default, all agentic workflows and AI agent records are readonly.

## AI model providers

You can use Now LLM Service, Now LLM Long Term Stable models \(LTS\), Azure OpenAI, Google Gemini or Anthropic Claude on AWS as the AI model provider for all Now Assist skills and AI agents. Use the Configuration Controls in to define which options are available, then set the skill-level preferences in the [Now Assist Admin console](https://www.servicenow.com/docs/access?context=manage-large-language-models&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US). For more information, see .

## Security

Enable security settings to run AI agents and agentic workflows using Access Control Lists \(ACLs\) and user identities. You can configure and manage the ACLs in AI Agent Studio. See [Implement access control in Now Assist AI agents](https://www.servicenow.com/docs/access?context=aia-security-implementation&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US) for more information.

## Installed agents

Looking for an AI agent?

-   There might be AI agents installed with the Now Assist application that are not used in agentic workflows. To learn how to see all agents that are available on your instance, see [Find AI agents](https://www.servicenow.com/docs/access?context=find-ai-agents&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).
-   To find agents that might not be installed on your instance, visit the [AI Agent Marketplace](https://store.servicenow.com/store/ai-marketplace) on the ServiceNow Store.

Visit the following links to learn about the Now Assist for ITOM agentic workflows.

1.  [Triage and analyze alerts agentic workflow](itom-alert-triage-agentic-workflow.md)  
Use the Triage and analyze alerts agentic workflow to complete preliminary alert tasks and analysis.
2.  [Analyze alert impact agentic workflow](now-assist-itom-agentic-aia.md)  
Use the Analyze alert impact agentic workflow to investigate an alert and get the context that you need to respond efficiently.

**Parent Topic:**[Now Assist for IT Operations Management \(ITOM\)](now-assist-itom.md)

