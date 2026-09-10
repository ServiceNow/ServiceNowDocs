---
title: Using agentic AI workflows
description: Use the Security Incident Response AI agentic workflows to complete security incident tasks.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/security-incident-response/using-now-assist-ai-agents-sir.html
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
keywords: [AI agents, agentic AI, agentic workflow]
breadcrumb: [Use, Security Incident Response Workspace, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Using agentic AI workflows

Use the Security Incident Response AI agentic workflows to complete security incident tasks.

Agentic workflows and their AI agents use [role masking](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aia-role-masking.md) to determine which users can access them. Ones installed with your applications have specific roles that come included with the application. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. For the instructions to change the security controls, see [Define security controls for an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/define-sec-controls-aw.md).

**Note:** Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents. For more information, see [ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-native-sku-overview.md).

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

For more information, see [AI agents, skills, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills-on-by-default.md).

<table id="table_fsq_52h_m2c"><thead><tr><th>

Agentic workflow name

</th><th>

Description

</th><th>

Available AI agents

</th></tr></thead><tbody><tr><td>

Wrap up security incident

</td><td>

This agentic workflow helps security analysts close a security incident using natural language in the ServiceNow Otto panel.

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

This agentic workflow helps security analysts identify a security incident resolution path. This workflow also helps security analysts close a security incident using natural language in the ServiceNow Otto panel.

</td><td>

-   Security incident resolution AI agent
-   Exchange Online integration handling AI agent
-   Security incident wrap-up generator AI agent
-   Observable analysis AI agent
-   Security incident activities handling AI agent
-   Endpoint detection and response \(EDR\) AI agent

</td></tr><tr><td>

Generate SIR Shift Handover Report

</td><td>

This agentic workflow adds details of a security incident to the shift handover report. The AI agent populates the different sections of the shift handover with details identified from the security incident.

</td><td>

Security incident shift handover AI agent

</td></tr><tr><td>



</td><td>

This agentic workflow helps security analysts and managers ask questions about security incident data in natural language in the ServiceNow Otto panel.

 The AI agent returns insights with links to the source records, and answers follow-up questions within the same chat.

</td><td>

Security incident data analysis AI agent

</td></tr></tbody>
</table>**Important:** By default, all agentic workflows and AI agent records are read-only.

To modify an agentic workflow, you must first [duplicate the agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/clone-aia-usecase.md). If required, you can add a trigger to invoke the workflow automatically.

There might be AI agents installed on your instance that are not used in agentic workflows. To learn how to see all agents that are available to you, see [Find AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/find-ai-agents.md).

-   **[Close security incidents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/now-assist-sir-close-incident-usecase.md)**  
The Wrap up security incident agentic workflow enables security analysts to close a security incident.
-   **[Resolve security incidents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/now-assist-sir-resolve-incident-ai-workflow.md)**  
Chat with an AI agent in the ServiceNow Otto panel to help you create a resolution plan for a security incident and to resolve it.
-   **[Analyze security incident data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/analyze-data-sir.md)**  
Analyze and get insights into your security incident data using available prompts or natural language queries from the ServiceNow Otto panel.
-   **[Analyze security operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/now-assist-sir-soc-efficiency-usecase.md)**  
The Analyze security operations metrics agentic workflow helps security operations center managers analyze the performance of their security teams.
-   **[Generate SIR Shift Handover Report](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/add-incidents-shifthandover-ai-agent.md)**  
Chat with an AI agent in the ServiceNow Otto panel to use the Generate SIR Shift Handover Report agentic workflow to help you add a security incident's detail to a shift handover report.

**Parent Topic:**[Using SIR Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/using-sir-workspace.md)

**Related topics**  


[Using ServiceNow Otto for Security Incident Response \(SIR\) generative AI skills]()

[Working with Security Incident Records]()

[Security Incident Playbook]()

[Prerequisites for the Playbooks]()

[Rebuilding existing playbooks in Workflow Studio]()

[Activity Definitions]()

[Sample Playbooks for SIR Workspace]()

[Working with MSI Records]()

[Working with Form UI actions]()

[Security Incident Closure workflow]()

[Handle security incidents using Advanced Work Assignment]()

