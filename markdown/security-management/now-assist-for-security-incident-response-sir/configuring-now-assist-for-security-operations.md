---
title: Configuring ServiceNow Otto for Security Incident Response \(SIR\)
description: The ServiceNow Otto for Security Incident Response \(SIR\) application is supported in the Security Incident Response Workspace and in the legacy Core UI \(UI16\). Use the guided setup in the AI Admin Hub console to configure ServiceNow Otto for Security Incident Response \(SIR\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/security-management/now-assist-for-security-incident-response-sir/configuring-now-assist-for-security-operations.html
release: zurich
product: Now Assist for Security Incident Response \(SIR\)
classification: now-assist-for-security-incident-response-sir
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [ServiceNow Otto for Security Incident Response \(SIR\), Security Operations]
---

# Configuring ServiceNow Otto for Security Incident Response \(SIR\)

The ServiceNow Otto for Security Incident Response \(SIR\) application is supported in the Security Incident Response Workspace and in the legacy Core UI \(UI16\). Use the guided setup in the AI Admin Hub console to configure ServiceNow Otto for Security Incident Response \(SIR\).

## Configuration overview

AI agents use [role masking](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/aia-role-masking.md) to determine which users can access them. Ones installed with your applications have specific roles that come included with the application. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. For the instructions to change the security controls, see [Define security controls for an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/define-sec-controls-aia.md).

**Important:** Some generative AI skills, AI agents, and agentic workflows are turned on by default. For more information, see [AI agents, skills, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skills-on-by-default.md).

By sharing data with the ServiceNow® AI development program, you provide relevant data to help improve prediction accuracy, user experience, tailor products to your business needs, and reduce hallucinations for your activated ServiceNow Otto skills.

You can opt out of a ServiceNow instance from sharing data from the AI Admin Hub console. See [Opt out of data sharing for Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/opt-out-of-data-sharing-for-now-assist.md). Repeat the opt-out process for all instances that use the ServiceNow Otto functionality.

Use the AI Admin Hub console to configure ServiceNow Otto for Security Incident Response \(SIR\). This console contains everything to install the applications and configure the generative AI skills. For additional information, see [Configuring AI skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/configuring-na-landing.md).

**Note:** When you update the ServiceNow Otto for Security Incident Response \(SIR\) applications, its dependency applications are automatically updated.

The following table lists the features and skills that you can access from the AI Admin Hub console.

**Note:** Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents. For more information, see .

<table id="table_igy_kpc_1cc"><thead><tr><th>

ServiceNow Otto product

</th><th>

Security incident skills

</th></tr></thead><tbody><tr><td rowspan="8">

ServiceNow Otto for Security Incident Response \(SIR\)

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
</table>1.  [Install plugins for ServiceNow Otto](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/install-now-assist-feature-plugins.md).

    Install the ServiceNow Otto for Security Incident Response \(SIR\) application \(sn\_sec\_gen\_ai\) and Security Incident Response Core \[sn\_si\] applications.

    **Note:**

    When you update the ServiceNow Otto for Security Incident Response \(SIR\) application, its dependency applications are automatically updated.

2.  [Configure a skill for ServiceNow Otto for Security Incident Response \(SIR\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/now-assist-for-security-incident-response-sir/activate-skills-for-now-assist-security-incident.md)

    You can deactivate, configure, and reactivate generative AI skills and agentic workflows in the Guided Setup.


