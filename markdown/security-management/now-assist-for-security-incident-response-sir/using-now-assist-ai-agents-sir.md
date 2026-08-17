---
title: Using agentic AI workflows
description: Use the Security Incident Response AI agentic workflows to complete your tasks autonomously.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/security-management/now-assist-for-security-incident-response-sir/using-now-assist-ai-agents-sir.html
release: zurich
product: Now Assist for Security Incident Response \(SIR\)
classification: now-assist-for-security-incident-response-sir
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [AI agents, agentic AI, agentic workflow]
breadcrumb: [ServiceNow Otto for Security Incident Response \(SIR\), Security Operations]
---

# Using agentic AI workflows

Use the Security Incident Response AI agentic workflows to complete your tasks autonomously.

Agentic workflows and their AI agents use [role masking](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/aia-role-masking.md) to determine which users can access them. Ones installed with your applications have specific roles that come included with the application. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. For the instructions to change the security controls, see [Define security controls for an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/define-sec-controls-aw.md).

**Note:** Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents. For more information, see .

**Important:** Some generative AI skills, agents, and agentic workflows are turned on by default. The default behavior works as follows:

-   **New customers**

    When you install an AI product, designated generative AI skills, AI agents, or agentic workflows are turned on automatically.

-   **Existing customers who are upgrading \(starting with Zurich Patch 4\)**

    There is no change to skills, agents, or agentic workflows that are currently enabled and customized.

    An AI asset is turned on if:

    -   The AI plugin is installed, but the asset was never turned on.
    -   An admin has never adjusted roles for the skill.
    An AI asset is not turned on if:

    -   The asset was previously turned on, and then turned off again.
    -   An admin has adjusted roles for the asset.

For more information, see [AI agents, skills, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skills-on-by-default.md).

<table id="table_fsq_52h_m2c"><thead><tr><th>

Agentic workflow name

</th><th>

Description

</th><th>

Available AI agents

</th></tr></thead><tbody><tr><td>

Wrap up security incident

</td><td>

This agentic workflow helps the security analysts to close a security incident using natural language in the ServiceNow Otto panel.

</td><td>

Security incident wrap-up generator AI agent

</td></tr><tr><td>

Analyze security operations metrics

</td><td>

This agentic workflow helps a security operations center \(SOC\) manager analyze their security analysts' performance.

 Metrics are generated for security incident response \(SIR\) records for case volume, mean time to assign \(MTTA\), and mean time to resolve \(MTTR\).

</td><td>

-   Security incident retrieval AI agent
-   Security metrics analysis AI agent

</td></tr><tr><td>

Resolve security incident

</td><td>

This agentic workflow helps the security analysts to identify a security incident resolution path. This workflow also assist the security analysts to close a security incident using natural language in the ServiceNow Otto panel.

</td><td>

-   Security incident resolution AI agent
-   Exchange online integration handling AI agent
-   Security incident wrap up generator AI agent
-   Observable analysis AI agent
-   Security incident activities handling AI agent
-   EDR AI agent

</td></tr><tr><td>

Generate SIR Shift Handover Report

</td><td>

This agentic workflow adds details of a security incident to the shift handover report. The agent populates the different sections of the shift handover with appropriate content by identifying the relevant details from the security incident.

</td><td>

Security incident shift handover AI agent

</td></tr></tbody>
</table>**Important:** By default, all agentic workflows and AI agent records are read-only.

To modify an agentic workflow, you must first [duplicate the agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/clone-aia-usecase.md). If required, you can add a trigger to invoke the workflow automatically.

There might be AI agents installed on your instance that are not used in agentic workflows. To learn how to see all agents that are available to you, see [Find AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/find-ai-agents.md).

