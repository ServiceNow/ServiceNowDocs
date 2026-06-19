---
title: Using agentic workflows
description: Use AI agents to complete your tasks autonomously.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/security-management/security-operations/using-now-assist-ai-agents-vr.html
release: zurich
product: Security Operations
classification: security-operations
topic_type: concept
last_updated: "2026-05-26"
reading_time_minutes: 3
keywords: [AI agents, agentic AI]
breadcrumb: [Now Assist in Unified Security Exposure Management, Explore, Unified Security Exposure Management, Security Operations]
---

# Using agentic workflows

Use AI agents to complete your tasks autonomously.

To view and use the generative AI skills agentic workflows in the Unified Security Exposure Management you must upgrade to Unified Security Exposure Management. See  for more information.

<table id="table_lpw_nx2_r2c"><thead><tr><th>

Agentic workflow name

</th><th>

Description

</th><th>

Available AI agents

</th><th>

Supported workspaces

</th></tr></thead><tbody><tr><td>

Security Exposure 360

</td><td>

[Evaluate vulnerability exposure data with Security Exposure 360](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/security-operations/now-assist-review-vulnerability-exposure-data.md).Vulnerability analysts and remediation owners can enter questions in plain language and receive comprehensive answers about all types of findings that include host, container, and test results vulnerabilities.

</td><td>

Data Analysis AI Agent

</td><td>

Legacy and Unified Security Exposure Management \(USEM\)

</td></tr><tr><td>

Guardrails detector agentic workflow

</td><td>

[Manage potential AI exposures](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/security-operations/exploring-ai-security-exposure.md)Use the AI agent to ask about the guardrails that were identified by the AI skill component in the AI Guardrails Helper, automatically defer findings with existing mitigations in the form of guardrails, or create exception rules to auto-defer future findings.

</td><td>

Guardrails detector agentic workflow

</td><td>

Unified Security Exposure Management \(USEM\)

</td></tr><tr><td>

Assess vulnerability exposure

</td><td>

[Assess your vulnerability exposure](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/security-operations/assess-exposure-vr-aiagent.md)-   Determine if your configuration items \(CIs\) and business services are exposed to known vulnerabilities.
-   Determine the potential impact that a specific vulnerability might have throughout your environment.
-   Check CIs for any new Cybersecurity and Infrastructure Security Agency \(CISA\) exploitable \(zero-day\) vulnerabilities.
-   Create watch topics in the Vulnerability Manager workspace to remediate vulnerable items.

</td><td>

-   CISA vulnerability analysis AI agent
-   Vulnerability exposure analysis AI agent
-   Watch topic creation AI agent

</td><td>

Legacy and Unified Security Exposure Management \(USEM\)

</td></tr><tr><td>

Retrieve vulnerability and exposure data

</td><td>

[Retrieve Vulnerability and exposure data with generative AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/security-operations/retrieve-vr-data.md).Ask questions in natural language to help you quickly retrieve vulnerability and exposure data across legacy sources and Unified Security Exposure Management \(USEM\).

</td><td>

Retrieve VR data agent

</td><td>

Legacy and Unified Security Exposure Management \(USEM\)

</td></tr><tr><td>

Analyze vulnerability remediation status

</td><td>

[Analyze vulnerability remediation status](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/security-operations/sla-targets-vr-aiagent.md)-   Gain insights into your compliance metrics and statistics for how well you're meeting remediation target dates on vulnerable item \(VIT\) records.
-   View your monthly VIT record remediation totals and identify missed targets.
-   Break down remediation data on VITs by **Severity**, **Assignment group**, **Configuration item**, and **Vulnerability** for your monthly Service Level Agreement \(SLA\) compliance reviews.

</td><td>

Remediation compliance analysis AI Agent

</td><td>

Legacy and Unified Security Exposure Management \(USEM\)

</td></tr></tbody>
</table>**Important:** By default, all agentic workflows and AI agent records are read-only.

To modify an agentic workflow, you must first duplicate the agentic workflow, and then proceed with the following steps:

-   Activate the agentic workflow. The Now Assist for Vulnerability Response AI agents included with the application are activated by default.
-   If required, you can add a trigger to invoke the agentic workflow automatically.
-   See [Configure an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/security-operations/now-assist-vr-acticvate-agentic-workflow.md) for more information.

Looking for an AI agent?

-   There might be AI agents installed with the Now Assist application that are not used in agentic workflows. To learn how to see all agents that are available on your instance, see Find AI agents.
-   To find agents that might not be installed on your instance, visit the [AI Agent Marketplace](https://store.servicenow.com/store/ai-marketplace) on the ServiceNow Store.

