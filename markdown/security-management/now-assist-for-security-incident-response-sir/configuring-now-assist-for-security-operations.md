---
title: Configuring Now Assist for Security Incident Response
description: The Now Assist for Security Incident Response application is supported in the Security Incident Response Workspace and in the legacy Core UI \(UI16\). Use the guided setup in the Now Assist Admin console to configure Now Assist for Security Incident Response.
locale: en-US
release: australia
product: Now Assist for Security Incident Response \(SIR\)
classification: now-assist-for-security-incident-response-sir
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Now Assist for Security Incident Response, Security Operations]
---

# Configuring Now Assist for Security Incident Response

The Now Assist for Security Incident Response application is supported in the Security Incident Response Workspace and in the legacy Core UI \(UI16\). Use the guided setup in the Now Assist Admin console to configure Now Assist for Security Incident Response.

## Configuration overview

AI agents use [role masking](https://www.servicenow.com/docs/access?context=aia-role-masking&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US) to determine which users can access them. Ones installed with Now Assist applications have specific roles that come included with the application. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. For the instructions to change the security controls, see [Define security controls for an AI agent](https://www.servicenow.com/docs/access?context=define-sec-controls-aia&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

**Important:** Some Now Assist skills, agents, and agentic workflows are turned on by default. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

By sharing data with the ServiceNow® AI development program, you provide relevant data to help improve prediction accuracy, user experience, tailor products to your business needs, and reduce hallucinations for your activated Now Assist skills.

You can opt out of a ServiceNow instance from sharing data from the Now Assist Admin console. See [Opt out of data sharing for Now Assist](https://www.servicenow.com/docs/access?context=opt-out-of-data-sharing-for-now-assist&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US). Repeat the opt-out process for all instances that use the Now Assist functionality.

Use the Now Assist Admin console to configure Now Assist for Security Incident Response. This console contains everything to install the applications and configure the generative AI skills. For additional information, see [Configuring Now Assist Admin features](https://www.servicenow.com/docs/access?context=configuring-na-landing&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

**Note:** When you update the Now Assist for Security Incident Response applications, its dependency applications are automatically updated.

The following table lists the features and skills that you can access from the Now Assist Admin console.

**Note:** Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents. For more information, see [ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

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
</table>1.  [Install Now Assist plugins](https://www.servicenow.com/docs/access?context=install-now-assist-feature-plugins&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

    Install the Now Assist for Security Incident Response application \(sn\_sec\_gen\_ai\) and Security Incident Response Core \[sn\_si\] applications.

    **Note:**

    When you update the Now Assist for Security Incident Response application, its dependency applications are automatically updated.

2.  [Configure a skill for Now Assist for Security Incident Response](../task/activate-skills-for-now-assist-security-incident.md)

    You can deactivate, configure, and reactivate generative AI skills and agentic workflows in the Guided Setup.


