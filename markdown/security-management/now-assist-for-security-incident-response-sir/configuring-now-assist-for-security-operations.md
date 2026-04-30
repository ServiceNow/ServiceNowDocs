---
title: Configuring Now Assist for Security Incident Response
description: The Now Assist for Security Incident Response application is supported in the Security Incident Response Workspace and in the legacy Core UI \(UI16\). Use the guided setup in the Now Assist Admin console to configure Now Assist for Security Incident Response.
locale: en-US
release: yokohama
product: Now Assist for Security Incident Response \(SIR\)
classification: now-assist-for-security-incident-response-sir
topic_type: concept
last_updated: "2026-01-15"
reading_time_minutes: 2
breadcrumb: [Now Assist for Security Incident Response, Security Operations]
---

# Configuring Now Assist for Security Incident Response

The Now Assist for Security Incident Response application is supported in the Security Incident Response Workspace and in the legacy Core UI \(UI16\). Use the guided setup in the Now Assist Admin console to configure Now Assist for Security Incident Response.

## Configuration overview

By sharing data with the ServiceNow® AI development program, you provide relevant data to help improve prediction accuracy, user experience, tailor products to your business needs, and reduce hallucinations for your activated Now Assist skills.

You can opt out of an ServiceNow instance from sharing data from the Now Assist Admin console. See [Opt out of data sharing for Now Assist](https://www.servicenow.com/docs/access?context=opt-out-of-data-sharing-for-now-assist&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US). Repeat the opt-out process for all instances that use the Now Assist functionality.

Use the Now Assist Admin console to configure Now Assist for Security Incident Response. This console contains everything to install the applications and configure the generative AI skills. For additional information, see [Configuring Now Assist settings and features](https://www.servicenow.com/docs/access?context=configuring-na-landing&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

**Note:** When you update the Now Assist for Security Incident Response applications, its dependency applications are automatically updated.

The following table lists the features and skills that you can access from the Now Assist Admin console.

<table id="table_igy_kpc_1cc"><thead><tr><th>

Now Assist Technology product

</th><th>

Security incident skills

</th></tr></thead><tbody><tr><td rowspan="5">

Now Assist for Security Incident Response

</td><td>

Security Incident summarization**Note:** The incident summarization supports security incidents in any state other than **Draft**.

</td></tr><tr><td>

Resolution notes generation.

</td></tr><tr><td>

Security incident recommended actionsThe security incident recommended actions skill supports security incidents in any state other than **Closed** and **Cancelled**.

**Note:**

The AI Search application must be enabled so that the Recommended Actions skill works for security incidents. To verify AI Search is enabled on your instance, navigate to **All** &gt; **AI Search** &gt; **AI Search Status**. Contact support if the page indicates that AI Search is not enabled.

Correlation insights support security incidents in all states.

</td></tr><tr><td>

Post-incident analysis

</td></tr><tr><td>

Security Incident Quality Assessment

</td></tr></tbody>
</table>1.  [Install Now Assist plugins](https://www.servicenow.com/docs/access?context=install-now-assist-feature-plugins&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

    Install the Now Assist for Security Incident Response application \(sn\_sec\_gen\_ai\) and Security Incident Response Core \[sn\_si\] applications.

    **Note:**

    When you update the Now Assist for Security Incident Response application, its dependency applications are automatically updated.

2.  [Configure a skill for Now Assist for Security Incident Response](../task/activate-skills-for-now-assist-security-incident.md)

    You can deactivate, configure, and reactivate generative AI skills and agentic workflows in the Guided Setup.


