---
title: Using agentic AI workflows in Now Assist for Security Incident Response
description: Use the Security Incident Response AI agentic workflows to complete your tasks autonomously.
locale: en-US
release: australia
product: Now Assist for Security Incident Response \(SIR\)
classification: now-assist-for-security-incident-response-sir
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [AI agents, agentic AI, agentic workflow]
breadcrumb: [Now Assist for Security Incident Response, Security Operations]
---

# Using agentic AI workflows in Now Assist for Security Incident Response

Use the Security Incident Response AI agentic workflows to complete your tasks autonomously.

Agentic workflows and their AI agents use [role masking](https://www.servicenow.com/docs/access?context=aia-role-masking&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US) to determine which users can access them. Ones installed with Now Assist applications have specific roles that come included with the application. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. For the instructions to change the security controls, see [Define security controls for an agentic workflow](https://www.servicenow.com/docs/access?context=define-sec-controls-aw&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

**Note:** Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents. For more information, see [ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

**Important:** Some Now Assist skills, agents, and agentic workflows are turned on by default. The default behavior works as follows:

-   **New customers**

    When you install a Now Assist product, designated skills, agents, or agentic workflows are turned on automatically.

-   **Existing customers who are upgrading \(starting with Australia Patch 4\)**

    There is no change to skills, agents, or agentic workflows that are currently enabled and customized.

    An AI asset is turned on if:

    -   The Now Assist plugin is installed, but the asset was never turned on.
    -   An admin has never adjusted roles for the skill.
    An AI asset is not turned on if:

    -   The asset was previously turned on, and then turned off again.
    -   An admin has adjusted roles for the asset.

<table id="table_fsq_52h_m2c"><thead><tr><th>

Agentic workflow name

</th><th>

Description

</th><th>

Available AI agents

</th></tr></thead><tbody><tr><td>

Wrap up security incident

</td><td>

This agentic workflow helps the security analysts to close a security incident using natural language in the Now Assist panel.

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

This agentic workflow helps the security analysts to identify a security incident resolution path. This workflow also assist the security analysts to close a security incident using natural language in the Now Assist panel.

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

To modify an agentic workflow, you must first [duplicate the agentic workflow](https://www.servicenow.com/docs/access?context=clone-aia-usecase&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US). If required, you can add a trigger to invoke the workflow automatically.

There might be AI agents installed with the Now Assist application that are not used in agentic workflows. To learn how to see all agents that are available to you, see [Find AI agents](https://www.servicenow.com/docs/access?context=find-ai-agents&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

