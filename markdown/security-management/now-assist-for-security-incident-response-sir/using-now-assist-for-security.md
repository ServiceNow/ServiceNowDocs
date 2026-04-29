---
title: Using Now Assist for Security Incident Response generative AI skills
description: Security analysts can close security incidents quickly from within their flow of work with the generative AI skills supported by Now Assist for Security Incident Response.
locale: en-US
release: australia
product: Now Assist for Security Incident Response \(SIR\)
classification: now-assist-for-security-incident-response-sir
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Now Assist for Security Incident Response, Security Operations]
---

# Using Now Assist for Security Incident Response generative AI skills

Security analysts can close security incidents quickly from within their flow of work with the generative AI skills supported by Now Assist for Security Incident Response.

## Skills in global domain reuse

By default, all skills exist in the global domain. When you use Now Assist in a domain-separated environment, users are only able to access data in their domain. For example, if a user uses the summarization skill, Now Assist only uses material that exists in the user's domain when generating that summary. Additionally, there is no co-mingling of data for domain-separated instances when using generative AI skills. The data resides only on the instance, and the shared services used for generative AI do not persist any requests \(prompts\) and responses. For more information, see [Domain separation in the Now Assist Admin console](https://www.servicenow.com/docs/access?context=domain-separation-in-the-now-assist-admin-console&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US). \(Note that global domain is not the same as global scope. For more information, see [Exploring Next Experience pickers](https://www.servicenow.com/docs/access?context=next-experience-pickers&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).\)

AI agents use [role masking](https://www.servicenow.com/docs/access?context=aia-role-masking&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US) to determine which users can access them and what data they have access to. Ones installed with Now Assist applications have specific roles that come included with the application. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. Data access settings must also include these roles. For the instructions to change the security controls, see [Define security controls for an AI agent](https://www.servicenow.com/docs/access?context=define-sec-controls-aia&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

**Important:** Some Now Assist skills, agents, and agentic workflows are turned on by default. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

**Note:** Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents. For more information, see [ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

With generative AI skills with Now Assist for Security Incident Response, your security analysts have the option to:

-   Summarize security incident details and review the context quickly in a concise, easy-to-read format.
-   Generate closure \(resolution\) notes.
-   Generate recommended actions for a security incident
-   Generate post incident analysis data
-   Generate performance metrics for your remediation teams.

    This skill is activated for use with an AI agent. See [Analyze security operations metrics agentic workflow](../task/assess-metrics-sir-aiagent.md) for more information.

-   Generate correlation insights to speed up incident investigation.
-   Generate a quality assessment report of a security incident

Security managers and analysts can request security incident summaries and closure notes from the following locations:

-   Security incident records
-   Security Incident Response Workspace
-   The Now Assist panel.

    **Note:** The security incident recommended actions and post-incident analysis skills are not available from the Now Assist panel.


Security managers and analysts can generate recommended next steps and post-incident analysis data from the following locations:

-   Security incident records
-   Security Incident Response Workspace

Security managers and analysts can create remediation tasks from generated recommended actions only from security incidents in the Security Incident Response Workspace.

Security managers and analysts can request security incident summaries and closure notes from the following locations:

-   Security incident records
-   Security Incident Response Workspace
-   The Now Assist panel.

    **Note:** The security incident recommended actions and post-incident analysis skills are not available from the Now Assist panel.


Security managers and analysts can generate recommended next steps and post-incident analysis data from the following locations:

-   Security incident records
-   Security Incident Response Workspace

Security managers and analysts can create remediation tasks from generated recommended actions only from security incidents in the Security Incident Response Workspace.

1.  [Summarize a security incident with Now Assist for Security Incident Response](../task/summarize-security-incident-now-assist-sec-incident.md)

    Generate a summary for a security incident that includes the underlying issue, incident details, related lists data \(observables\), and key actions already taken.

2.  [Generate recommended actions for a security incident with Now Assist for Security Incident Response](../task/generate-recommended-actions-now-assist-for-security.md)
3.  [Generate a post-incident analysis for a security incident with Now Assist for Security Incident Response](../task/generate-pia-report-now-assist-security-incident.md)
4.  [Generate correlation insights in the Now Assist panel with Now Assist for Security Incident Response](../task/generate-correlation-insights-now-assist-for-security.md)
5.  [Generate a quality assessment report](../task/na-sir-generate-quality-assessment-report.md) for a security incident
6.  [Generate closure notes for a security incident with Now Assist for Security Incident Response](../task/generate-closure-notes-si-now-assist-sec-incident.md)

    Automatically generate the closure notes for a security incident.

7.  [Request generative AI skills in the Now Assist panel for Now Assist for Security Incident Response](../task/request-genai-from-now-assist-panel-now-assist-sec-incident.md)

    Generate summaries and closure notes from the Now Assist panel.

    **Note:** The security incident recommended actions and post-incident analysis skills are not available from the Now Assist panel.

8.  [Customize a Now Assist for Security Incident Response skill](../task/cust-now-assist-security-incident-skill.md)

    Customize the input fields of a skill to suit the requirements of your environment.


