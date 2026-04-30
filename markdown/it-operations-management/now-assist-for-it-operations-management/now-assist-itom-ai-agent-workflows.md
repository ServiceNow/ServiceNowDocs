---
title: Using agentic workflows in Now Assist for IT Operations Management \(ITOM\)
description: Use the IT Operations Management \(ITOM\) agentic workflows to complete tasks autonomously.
locale: en-US
release: yokohama
product: Now Assist for IT Operations Management
classification: now-assist-for-it-operations-management
topic_type: concept
last_updated: "2025-08-21"
reading_time_minutes: 3
keywords: [AI Agents, Agentic AI]
breadcrumb: [Now Assist for ITOM, IT Operations Management]
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

</td></tr><tr><td>

Manage alerts autonomously

</td><td>

Investigates alerts, summarizes alert-related reports, and stores structured insights with key findings in the AI Agent Insight table.

</td><td>

Manage alerts AI agent

</td></tr></tbody>
</table>**Important:** Some Now Assist skills, agents, and agentic workflows are turned on by default. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

## AI model providers

You can use Now LLM Service, Now LLM Long Term Stable models \(LTS\), Azure OpenAI, Google Gemini or Anthropic Claude on AWS as the AI model provider for all Now Assist skills and AI agents. Use the Configuration Controls in [AI Control Tower](https://www.servicenow.com/docs/access?context=ai-model-providers&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) to define which options are available, then set the skill-level preferences in the [Now Assist Admin console](https://www.servicenow.com/docs/access?context=manage-large-language-models&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US). For more information, see [Large language models on the ServiceNow AI Platform®](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

## Security

Enable security settings to run AI agents and agentic workflows using Access Control Lists \(ACLs\) and user identities. You can configure and manage the ACLs in AI Agent Studio. See [Implement access control in Now Assist AI agents](https://www.servicenow.com/docs/access?context=aia-security-implementation&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) for more information.

## Installed agents

Looking for an AI agent?

-   There might be AI agents installed with the Now Assist application that are not used in agentic workflows. To learn how to see all agents that are available on your instance, see [Find AI agents](https://www.servicenow.com/docs/access?context=find-ai-agents&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).
-   To find agents that might not be installed on your instance, visit the [AI Agent Marketplace](https://store.servicenow.com/store/ai-marketplace) on the ServiceNow Store.

Visit the following links to learn about the Now Assist for ITOM agentic workflows.

1.  [Triage and analyze alerts agentic workflow](itom-alert-triage-agentic-workflow.md)  
Use the Triage and analyze alerts agentic workflow to complete preliminary alert tasks and analysisfor alerts.
2.  [Analyze alert impact agentic workflow](now-assist-itom-agentic-aia.md)  
Use the analyze alert impact agentic workflow to investigate an alert and get the context that you need to respond efficiently.
3.  [Analyze potential impact agentic workflow](now-assist-itom-analyze-potential-impact-workflow.md)  
The Analyze potential impact agentic workflow analyzes how a change request might impact servers and suggested services. This analysis helps you make informed decisions about the next steps regarding the change request.
4.  [Manage alerts autonomously agentic workflow](itom-autonomous-operator-workflow.md)  
Enhance IT operations with AI-driven, autonomous alert management using the manage alerts autonomously agentic workflow.

**Parent Topic:**[Now Assist for IT Operations Management \(ITOM\)](now-assist-itom.md)

