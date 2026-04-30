---
title: Configuring Now Assist for Security Incident Response
description: The Now Assist for Security Incident Response application is supported in the Security Incident Response Workspace and in the legacy Core UI \(UI16\). You can use the guided setup in the Now Assist Admin console to configure Now Assist for Security Incident Response.
locale: en-US
release: xanadu
product: Now Assist for Security Incident Response \(SIR\)
classification: now-assist-for-security-incident-response-sir
topic_type: concept
last_updated: "2025-05-19"
reading_time_minutes: 2
breadcrumb: [Now Assist for Security Incident Response, Security Operations]
---

# Configuring Now Assist for Security Incident Response

The Now Assist for Security Incident Response application is supported in the Security Incident Response Workspace and in the legacy Core UI \(UI16\). You can use the guided setup in the Now Assist Admin console to configure Now Assist for Security Incident Response.

## Configuration overview

By sharing data with the ServiceNow® AI development program, you provide relevant data to help improve prediction accuracy, user experience, tailor products to your business needs, and reduce hallucinations for your activated Now Assist skills.

You can choose to opt out of a ServiceNow instance from data sharing from the Now Assist Admin console if you don't want to participate. See [Opt out of data sharing for Now Assist](https://www.servicenow.com/docs/access?context=opt-out-of-data-sharing-for-now-assist&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US). Repeat the opt-out process for all instances that use the Now Assist functionality.

Use the Now Assist Admin console to configure Now Assist for Security Incident Response. This console contains everything that you must install the applications and configure the generative AI skills. For additional information, see [Configuring Now Assist settings and features](https://www.servicenow.com/docs/access?context=configuring-na-landing&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).

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

The AI Search application must be enabled so that the Recommended Actions skill works for security incidents. To verify AI Search is enabled on your instance, navigate to **All** &gt; **AI Search** &gt; **AI Search Status**. Contact support if the page indicates AI Search is not enabled.

Correlation insights supports security incidents in all states.

</td></tr><tr><td>

Post-incident analysis generation

</td></tr><tr><td>

Analyze security operations metrics for your remediation teams and get suggestions for improvement from an AI agent.

</td></tr></tbody>
</table>1.  [Install Now Assist plugins](https://www.servicenow.com/docs/access?context=install-now-assist-feature-plugins&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).

    **Note:** The Now Assist for Security Operations application in the ServiceNow® Store and in your ServiceNow AI Platform instance has changed to the Now Assist for Security Incident Response application starting with version 2.0.1.

    Install the Now Assist for Security Incident Response application \(sn\_sec\_gen\_ai\).

2.  [Configure and activate a skill for Now Assist for Security Incident Response.](../task/activate-skills-for-now-assist-security-incident.md)

    Configure and review the details for a skill. You activate a skill from the Guided Setup.


## Using Guided Setup to implement Now Assist for Security Incident Response

Guided Setup provides a sequence of tasks that help you configure Now Assist for Security Incident Response on your ServiceNow instance. To open the Guided Setup for Now Assist for Security Incident Response, navigate to **All** &gt; **Now Assist Admin** &gt; **Skills**.

For more information, see [Configure and activate a skill for Now Assist for Security Incident Response](../task/activate-skills-for-now-assist-security-incident.md).

