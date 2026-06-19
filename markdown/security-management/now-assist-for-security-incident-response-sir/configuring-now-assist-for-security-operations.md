---
title: Configuring Now Assist for Security Incident Response
description: The Now Assist for Security Incident Response application is supported in the Security Incident Response Workspace and in the legacy Core UI \(UI16\). Use the guided setup in the Now Assist Admin console to configure Now Assist for Security Incident Response.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/security-management/now-assist-for-security-incident-response-sir/configuring-now-assist-for-security-operations.html
release: zurich
product: Now Assist for Security Incident Response \(SIR\)
classification: now-assist-for-security-incident-response-sir
topic_type: concept
last_updated: "2026-03-06"
reading_time_minutes: 2
breadcrumb: [Now Assist for Security Incident Response, Security Operations]
---

# Configuring Now Assist for Security Incident Response

The Now Assist for Security Incident Response application is supported in the Security Incident Response Workspace and in the legacy Core UI \(UI16\). Use the guided setup in the Now Assist Admin console to configure Now Assist for Security Incident Response.

## Configuration overview

Role masking enables users to limit the roles and privileges of AI agents during tool execution. AI agents that get installed with Now Assist applications are assigned pre-defined roles. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. Data access settings must also include these roles. For the instructions to change the security controls, see Define security controls for an AI agent.

**Important:** Some Now Assist skills, agents, and agentic workflows are turned on by default. For more information, see .

By sharing data with the ServiceNow® AI development program, you provide relevant data to help improve prediction accuracy, user experience, tailor products to your business needs, and reduce hallucinations for your activated Now Assist skills.

You can opt out of a ServiceNow instance from sharing data from the Now Assist Admin console. See . Repeat the opt-out process for all instances that use the Now Assist functionality.

Use the Now Assist Admin console to configure Now Assist for Security Incident Response. This console contains everything to install the applications and configure the generative AI skills. For additional information, see .

**Note:** When you update the Now Assist for Security Incident Response applications, its dependency applications are automatically updated.

The following table lists the features and skills that you can access from the Now Assist Admin console.

<table id="table_igy_kpc_1cc"><thead><tr><th>

Now Assist Technology product

</th><th>

Security incident skills

</th></tr></thead><tbody><tr><td rowspan="8">

Now Assist for Security Incident Response

</td><td>

Security incident summarization**Note:** The incident summarization supports security incidents in any state other than **Draft**.

</td></tr><tr><td>

Resolution notes generation.

</td></tr><tr><td>

Security operations metrics analysis

</td></tr><tr><td>

Security incident recommended actionsThe security incident recommended actions skill supports security incidents in any state other than **Closed** and **Cancelled**.

**Note:**

The AI Search application must be enabled so that the Recommended Actions skill works for security incidents. To verify AI Search is enabled on your instance, navigate to **All** &gt; **AI Search** &gt; **AI Search Status**. Contact support if the page indicates that AI Search is not enabled.

Correlation insights support security incidents in all states.

</td></tr><tr><td>

Post-incident analysis

</td></tr><tr><td>

Generate content for shift handover

</td></tr><tr><td>

Security incident resolution plan

</td></tr><tr><td>

Security incident quality assessment

</td></tr></tbody>
</table>1.  .

    Install the Now Assist for Security Incident Response application \(sn\_sec\_gen\_ai\) and Security Incident Response Core \[sn\_si\] applications.

    **Note:**

    When you update the Now Assist for Security Incident Response application, its dependency applications are automatically updated.

2.  [Configure a skill for Now Assist for Security Incident Response](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/now-assist-for-security-incident-response-sir/activate-skills-for-now-assist-security-incident.md)

    You can deactivate, configure, and reactivate generative AI skills and agentic workflows in the Guided Setup.


