---
title: Integrating scores from risk intelligence providers
description: Risk intelligence providers generate risk scores for a variety of third-party risk domains. Your organization can purchase services from providers that return data that is analogous to personal credit scores. The scores provide insight on how trustworthy and safe a particular third party can be.
locale: en-US
release: yokohama
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Integrate, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Integrating scores from risk intelligence providers

Risk intelligence providers generate risk scores for a variety of third-party risk domains. Your organization can purchase services from providers that return data that is analogous to personal credit scores. The scores provide insight on how trustworthy and safe a particular third party can be.

## Working with data from risk intelligence providers

**Note:** You can request risk data for third parties but not for engagements.

-   After you register a risk intelligence provider, you specify which of the provider's scoring or rating services you’ll use. You also specify how their scores or ratings map to your TPRM ratings. For more information, see [Register a risk intelligence provider](../task/tprm-riskintelprvdr-register.md), [Set up a risk intelligence provider service](../task/tprm-riskintelprvdr-set-up.md), and [Set up a request type for a provider](../task/tprm-riskintelprvdr-request-type.md).
-   You add a raw score from a provider to the provider service record for a third party. The system uses the mapping that you specified to normalize the value to the appropriate TPRM rating. For more information, see [Add a risk intelligence score to risk data for a third party](../task/tprm-riskintelprvdr-add-score.md).
-   A provider-based submission rule is a set of conditions and actions. In a rule, you can specify that an update to a rating from a risk intelligence provider is the condition that triggers the action that is specified in the rule. The action might be to create and send a third-party risk assessment, issue, task, or email. For more information, see [Automate actions upon risk intelligence updates](../task/tprm-riskintelprvdr-submissrule.md).

## Integration types

Here are some examples of the types of integrations supported by ServiceNow and ServiceNow partners:

-   Independent software vendor \(ISV\) integration types involve integrating ISV services such as EcoVadis or Black Kite.

-   Content integration types involve integrating external content sources such as regulatory databases or industry standards.

-   Data integration types involve integrating external data sources to gather and analyze relevant data such as data from financial systems, security tools, or vendor management systems.

-   Environmental, social, and governance \(ESG\) integration types involve incorporating ESG factors into the TPRM process.


## Integrations supported by ServiceNow

**Note:** You can find the integration apps on the ServiceNow Store.

|Provider|Product name|Content|Service provided|Type|
|--------|------------|-------|----------------|----|
|Shared Assessments|Standard information-gathering \(SIG\) questionnaire|Standard assessment|Industry standard questionnaire for use in assessments.|Content|
|EcoVadis|EcoVadis|Sustainability ratings|Sustainability scores in support of assessments and continuous monitoring.|ISV, data, ESG|

## Integrations supported by ServiceNow partners

**Note:** You can find the integration apps on the ServiceNow Store.

<table id="table_pvx_wsx_hyb"><thead><tr><th>

Provider

</th><th>

Product name

</th><th>

Content

</th><th>

Use case

</th><th>

Type

</th></tr></thead><tbody><tr><td>

BitSight

</td><td>

BitSight

</td><td>

Cyber risk ratings

</td><td>

Cyber risk scores in support of assessments and continuous third-party risk monitoring.

</td><td>

ISV, data

</td></tr><tr><td>

Security Scorecard

</td><td>

Security Scorecard

</td><td>

Cyber risk ratings

</td><td>

Cyber risk scores in support of assessments and continuous third-party risk monitoring.

</td><td>

ISV, data

</td></tr><tr><td>

RiskRecon

</td><td>

Risk Recon

</td><td>

Cyber risk ratings

</td><td>

Cyber risk scores in support of assessments and continuous third-party risk monitoring.

</td><td>

ISV, data

</td></tr><tr><td>

Upguard

</td><td>

Upguard Vendor Risk

</td><td>

Cyber risk

</td><td>

Cyber risk scores in support of assessments and continuous third-party risk monitoring.

</td><td>

ISV, data

</td></tr><tr><td>

Recorded Future

</td><td>

Recorded Future Intelligence

</td><td>

Cyber risk ratings

</td><td>

Cyber risk scores in support of assessments and continuous third-party risk monitoring.

</td><td>

ISV, data

</td></tr><tr><td>

Black Kite

</td><td>

Black Kite

</td><td>

Third-party risk management

</td><td>

Technical security, financial risk, ransomware susceptibility index, and compliance scores in addition to overall security ratings.

</td><td>

ISV

</td></tr><tr><td>

Interos

</td><td>

Interos

</td><td>

Supply chain and multiple domain ratings

</td><td>

Cyber, financial, ESG, geopolitical, operations, and restrictions ratings to support risk assessments and monitoring.

</td><td>

ISV, content

</td></tr><tr><td>

TruSight

</td><td>

TruSight

</td><td>

Third-party risk assessments

</td><td>

Access to TruSight-validated third-party risk assessments.

</td><td>

ISV

</td></tr><tr><td>

ISS Corporate Solutions

</td><td>

ISS ESG Cyber Risk Score for Vendor Risk Management

</td><td>

ESG ratings

</td><td>

Access to a comprehensive view of ISS Corporate Solutions' cyber risk management program through cyber risk and supply chain.

</td><td>

ISV

</td></tr><tr><td>

Securitybricks

</td><td>

CMMC - NIST-800-171 - Vendor Compliance Assessment

</td><td>

Template

</td><td>

Access to an automated assessment for Federal organizations.

</td><td>

data, content

</td></tr><tr><td>

Templarshield

</td><td>

HECVAT-Questionnaire for Higher Education

</td><td>

Content

</td><td>

Access to an automated questionnaire for Higher education organizations.

</td><td>

ISV, content

</td></tr></tbody>
</table>-   **[Register a risk intelligence provider](../task/tprm-riskintelprvdr-register.md)**  
Create a record for each risk intelligence provider from which you’ll request reports. The risk scores and ratings that risk intelligence providers generate are analogous to personal credit scores. The scores provide insight on how trustworthy and safe a particular third party can be.
-   **[Set up a risk intelligence provider service](../task/tprm-riskintelprvdr-set-up.md)**  
After you register a risk intelligence provider, you specify which of the provider's scoring or rating services you’ll use. You also specify how their scores or ratings map to your TPRM ratings.
-   **[Set up a request type for a provider](../task/tprm-riskintelprvdr-request-type.md)**  
After you register a risk intelligence provider and service, you specify the available request types that you and your organization will use.
-   **[Add a risk intelligence score to risk data for a third party](../task/tprm-riskintelprvdr-add-score.md)**  
You add a raw score from a provider to the provider service record for a third party. The system uses the mapping that you specified to normalize the value to the appropriate TPRM rating.
-   **[Automate actions upon risk intelligence updates](../task/tprm-riskintelprvdr-submissrule.md)**  
A provider-based submission rule is a set of conditions and actions. In a rule, you can specify that an update to a rating from a risk intelligence provider is the condition that triggers the action that is specified in the rule. The action might be to create and send a third-party risk assessment, issue, task, or email.

**Parent Topic:**[Integrating TPRM with other applications](integrating-with-tprm.md)

**Related topics**  


[Viewing risk intelligence scores](../../grc-workspace-vrm/reference/tprm-ws-tab-risk-intel-scores.md)

[Register a risk intelligence provider](../task/tprm-riskintelprvdr-register.md)

[Set up a risk intelligence provider service](../task/tprm-riskintelprvdr-set-up.md)

[Set up a request type for a provider](../task/tprm-riskintelprvdr-request-type.md)

