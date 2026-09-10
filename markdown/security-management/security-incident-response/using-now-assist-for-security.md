---
title: Using ServiceNow Otto for Security Incident Response \(SIR\) generative AI skills
description: Security analysts can close security incidents quickly from within their flow of work with the generative AI skills supported by ServiceNow Otto for Security Incident Response \(SIR\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/security-incident-response/using-now-assist-for-security.html
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Use, Security Incident Response Workspace, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Using ServiceNow Otto for Security Incident Response \(SIR\) generative AI skills

Security analysts can close security incidents quickly from within their flow of work with the generative AI skills supported by ServiceNow Otto for Security Incident Response \(SIR\).

## Skills in global domain reuse

By default, all skills exist in the global domain. When you use AI in a domain-separated environment, users are only able to access data in their domain. For example, if a user uses the summarization skill, AI only uses material that exists in the user's domain when generating that summary. Additionally, there is no co-mingling of data for domain-separated instances when using generative AI skills. The data resides only on the instance, and the shared services used for generative AI do not persist any requests \(prompts\) and responses. For more information, see [Domain separation in the AI Admin Hub console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/domain-separation-in-the-now-assist-admin-console.md). \(Note that global domain is not the same as global scope. For more information, see [Exploring Next Experience pickers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/next-experience-pickers.md).\)

AI agents use [role masking](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aia-role-masking.md) to determine which users can access them and what data they have access to. Ones installed with ServiceNow Otto applications have specific roles that come included with the application. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. Data access settings must also include these roles. For the instructions to change the security controls, see [Define security controls for an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/define-sec-controls-aia.md).

**Important:** Some generative AI skills, AI agents, and agentic workflows are turned on by default. For more information, see [AI agents, skills, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills-on-by-default.md).

**Note:** Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents. For more information, see [ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-native-sku-overview.md).

With generative AI skills with ServiceNow Otto for Security Incident Response \(SIR\), your security analysts have the option to:

-   Summarize security incident details and review the context quickly in a concise, easy-to-read format.
-   Generate closure \(resolution\) notes.
-   Generate recommended actions for a security incident
-   Generate post incident analysis data
-   Generate performance metrics for your remediation teams.

    This skill is activated for use with an AI agent. See [Analyze security operations metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/assess-metrics-sir-aiagent.md) for more information.

-   Generate correlation insights to speed up incident investigation.
-   Generate a quality assessment report of a security incident

Security managers and analysts can request security incident summaries and closure notes from the following locations:

-   Security incident records
-   Security Incident Response Workspace
-   The ServiceNow Otto panel.

    **Note:** The security incident recommended actions and post-incident analysis skills are not available from the ServiceNow Otto panel.


Security managers and analysts can generate recommended next steps and post-incident analysis data from the following locations:

-   Security incident records
-   Security Incident Response Workspace

Security managers and analysts can create remediation tasks from generated recommended actions only from security incidents in the Security Incident Response Workspace.

Security managers and analysts can request security incident summaries and closure notes from the following locations:

-   Security incident records
-   Security Incident Response Workspace
-   The ServiceNow Otto panel.

    **Note:** The security incident recommended actions and post-incident analysis skills are not available from the ServiceNow Otto panel.


Security managers and analysts can generate recommended next steps and post-incident analysis data from the following locations:

-   Security incident records
-   Security Incident Response Workspace

Security managers and analysts can create remediation tasks from generated recommended actions only from security incidents in the Security Incident Response Workspace.

1.  [Summarize a security incident](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/summarize-security-incident-now-assist-sec-incident.md)

    Generate a summary for a security incident that includes the underlying issue, incident details, related lists data \(observables\), and key actions already taken.

2.  [Generate recommended actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/generate-recommended-actions-now-assist-for-security.md)
3.  [Generate a post-incident analysis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/generate-pia-report-now-assist-security-incident.md)
4.  [Generate correlation insights in the ServiceNow Otto panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/generate-correlation-insights-now-assist-for-security.md)
5.  [Generate a quality assessment report](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/na-sir-generate-quality-assessment-report.md) for a security incident
6.  [Generate closure notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/generate-closure-notes-si-now-assist-sec-incident.md)

    Automatically generate the closure notes for a security incident.

7.  [Request generative AI skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/request-genai-from-now-assist-panel-now-assist-sec-incident.md)

    Generate summaries and closure notes from the ServiceNow Otto panel.

    **Note:** The security incident recommended actions and post-incident analysis skills are not available from the ServiceNow Otto panel.

8.  [Customize a skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/cust-now-assist-security-incident-skill.md)

    Customize the input fields of a skill to suit the requirements of your environment.


-   **[Summarize a security incident](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/summarize-security-incident-now-assist-sec-incident.md)**  
Understand the context of a security incident with the Security Incident summarization generative AI skill.
-   **[Generate closure notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/generate-closure-notes-si-now-assist-sec-incident.md)**  
Automatically generate a draft of the closure notes for a security incident when you close it. The draft is editable and will be reviewed before closing the security incident, and it can be used or modified as needed. Closure notes provide information about the resolution of a security incident to other analysts, managers, and key stakeholders.
-   **[Generate recommended actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/generate-recommended-actions-now-assist-for-security.md)**  
Automatically generate the next steps your analysts can take to help them close a security incident in the Security Incident Response Workspace. The recommended steps are based on existing security incidents and knowledge articles.
-   **[Generate a post-incident analysis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/generate-pia-report-now-assist-security-incident.md)**  
Automatically generate a post-incident analysis for a security incident that includes a root cause analysis, impact assessment, and learning and recommendations information.
-   **[Exploring correlation insights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/generating-insights-for-now-assist-for-security.md)**  
Generate correlation insights to avoid duplicating your investigation into affected users, configuration items, and observables and resolve the security incident that you're working on quickly. You select the criteria from a security incident that you want to base the correlation insights on.
-   **[Exploring Security incident quality assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/na-sir-quality-assessment.md)**  
Use generative AI to create a quality assessment report of a security incident. The reports are generated using a predefined, natural language rule set. The report provides an overall assessment summary followed by the detailed assessment for all the rules.
-   **[Request generative AI skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/request-genai-from-now-assist-panel-now-assist-sec-incident.md)**  
Request a security incident summary or closure notes from the ServiceNow Otto panel.

**Parent Topic:**[Using SIR Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/using-sir-workspace.md)

**Related topics**  


[Using agentic AI workflows]()

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

