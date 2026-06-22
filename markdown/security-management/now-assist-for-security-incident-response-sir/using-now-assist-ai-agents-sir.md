---
title: Using AI agentic workflows in Now Assist for Security Incident Response
description: Use the Security Incident Response AI agents to complete your tasks autonomously.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/security-management/now-assist-for-security-incident-response-sir/using-now-assist-ai-agents-sir.html
release: xanadu
product: Now Assist for Security Incident Response \(SIR\)
classification: now-assist-for-security-incident-response-sir
topic_type: concept
last_updated: "2025-02-25"
reading_time_minutes: 1
keywords: [AI Agents, Agentic AI]
breadcrumb: [Now Assist for Security Incident Response, Security Operations]
---

# Using AI agentic workflows in Now Assist for Security Incident Response

Use the Security Incident Response AI agents to complete your tasks autonomously.

<table id="table_fsq_52h_m2c"><thead><tr><th>

Agentic workflow name

</th><th>

Description

</th><th>

Available AI agents

</th></tr></thead><tbody><tr><td>

Close security incident

</td><td>

This agentic workflow helps the security analysts to close a security incident using natural language in the Now Assist panel.

</td><td>

Security incident wrap-up generator

</td></tr><tr><td>

Analyze security operations metrics

</td><td>

This agentic workflow helps a security operations center \(SOC\) manager analyze their security analysts' performance.

 Metrics are generated for security incident response \(SIR\) records for case volume, mean time to assign \(MTTA\), and mean time to resolve \(MTTR\).

</td><td>

-   Security incident retrieval AI agent
-   Security metrics analysis AI agent

</td></tr><tr><td>

Security incident resolution

</td><td>

This agentic workflow helps the security analysts to identify a security incident resolution path. This workflow also assist the security analysts to close a security incident using natural language in the Now Assist panel.

</td><td>

-   Security incident resolution AI agent
-   Exchange online integration handling AI agent
-   Security incident wrap up generator AI agent
-   Observable analysis AI agent
-   Security incident activities handling AI agent

</td></tr></tbody>
</table>**Important:** By default, all agentic workflows and AI agent records are read-only.

To modify an agentic workflow, you must first [Duplicate an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/intelligent-experiences/enable-ai-experiences/clone-aia-usecase.md), and then proceed with the following steps:

-   [Activate](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/security-management/now-assist-for-security-incident-response-sir/now-assist-sir-activate-agentic-workflow.md) the workflow.
-   Activate all the AI agents within the workflow.
-   If required, you can add a trigger to invoke the workflow automatically.

Looking for an AI agent?

-   There might be AI agents installed with the Now Assist application that are not used in agentic workflows. To learn how to see all agents that are available on your instance, see [Find AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/intelligent-experiences/enable-ai-experiences/find-ai-agents.md).
-   To find agents that might not be installed on your instance, visit the [AI Agent Marketplace](https://store.servicenow.com/store/ai-marketplace) on the ServiceNow Store.

