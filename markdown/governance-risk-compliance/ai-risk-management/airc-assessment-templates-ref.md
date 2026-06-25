---
title: Assessment templates reference
description: Reference table listing the assessment templates installed with AI Risk and Compliance. Templates are delivered in Draft state and must be published before use.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/ai-risk-management/airc-assessment-templates-ref.html
release: australia
product: AI Risk Management
classification: ai-risk-management
topic_type: reference
last_updated: "2026-05-28"
reading_time_minutes: 4
keywords: [assessment templates, FRIA, EU AI Act, NIST, AI Risk and Compliance]
breadcrumb: [Reference, AI Risk and Compliance, Governance, Risk, and Compliance]
---

# Assessment templates reference

Reference table listing the assessment templates installed with AI Risk and Compliance. Templates are delivered in Draft state and must be published before use.

## Assessment templates

The following table lists assessment templates installed with AI Risk and Compliance. Templates are delivered in **Draft** state. A user with the AI Risk and Compliance Admin \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_admin\] role publishes draft templates through the Assessment Workspace. For instructions, see [Assessment templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/ai-risk-management/airc-assessment-templates.md). AI case assessment templates are delivered as part of the AI Case Management application \(`sn_ai_case_mgmt`\) and are not included in AI Risk and Compliance base assessment templates. They are published through the same Assessment Workspace in a separate category.

**Note:**

**Note:**

The ServiceNow Risk products help customers address regulatory requirements under various jurisdictions. However, we do not guarantee compliance and customers are ultimately responsible for their own compliance with applicable regulations.

ServiceNow aims to provide software updates for new or updated major regulations and requirements within twelve to eighteen months of the regulation's publication. For regulations for which ServiceNow provides a level of support in the base system, ServiceNow aims to provide software updates for minor regulatory changes within 12 months and for major regulatory changes within up to 18 months depending on scope and impact. We differentiate between typical regulatory content updates, which do not require software updates or enhancements, and regulatory updates, which do require software updates or enhancements. Content updates are generally delivered on a shorter cadence than if software update or enhancement is required for the regulatory update or change.

|Name|Description|Applies to|Default state|When to use|
|----|-----------|----------|-------------|-----------|
|AI impact assessment|Evaluates the potential impact of an AI system on individuals, society, and the organization. Identifies risks related to privacy, non-discrimination, fairness, and other fundamental rights using a questionnaire-based approach. Responses can be configured to map to risk statements and control objectives through Post Assessment Actions. Automation rules that drive this mapping must be configured by your organization; no pre-configured mapping rules are included. Role required: AI asset owner or AI risk and compliance business user \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_business\_user\].|AI systems|Draft|After AI use case submission, during the Assess phase.|
|AI impact assessment for EU AI Act conformity assessment|Evaluates whether an AI system may be subject to the EU Artificial Intelligence Act \(AI Act\). Focuses on risk classification, fundamental rights, safety, and transparency requirements. Assessment results determine whether additional governance activities are required, such as a full EU AI Act Conformity Assessment or a Fundamental Rights Impact Assessment \(FRIA\). Role required: AI asset owner or AI risk and compliance business user \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_business\_user\].|AI systems|Draft|When an AI system may be subject to the EU AI Act, especially when high-risk classification is possible.|
|EU AI Act Conformity Assessment|Provides a comprehensive evaluation of whether a high-risk AI system meets applicable EU AI Act requirements, including risk management, data governance, technical documentation, transparency, human oversight, accuracy, and robustness. Role required: AI risk and compliance analyst \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_analyst\] or AI risk and compliance manager \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_manager\].|AI systems|Draft|After initial EU AI Act assessment classifies the system as high risk, and before pre-deployment review.|
|Fundamental Rights Impact Assessment \(FRIA\)|Evaluates how a high-risk AI system may affect fundamental rights such as privacy, non-discrimination, freedom of expression, access to justice, and human dignity. Complete the FRIA before deployment to document and mitigate potential adverse effects. Role required: AI risk and compliance analyst \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_analyst\] or AI risk and compliance business user \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_business\_user\].|AI systems|Draft|After conformity assessment identifies potential fundamental rights implications and before deployment.|
|High-risk AI assessment questionnaire|Captures detailed information for AI systems flagged as potentially high risk, including design, data handling, decision-making, and potential harms. Results determine which governance controls, monitoring requirements, and review processes apply throughout the AI system's life cycle. Role required: AI asset owner or AI risk and compliance business user \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_business\_user\].|AI systems|Draft|When an AI system is flagged as potentially high risk during intake screening or impact assessment.|
|AI Impact Assessment on AI asset inventory|Evaluates risks associated with a specific AI model independent of its parent AI system. Supports model-level governance when a model is shared across systems or has a distinct risk profile. Role required: AI asset owner or AI risk and compliance analyst \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_analyst\].|AI models|Draft|When a model requires independent governance evaluation \(for example, a shared model or one with distinct risk factors\).|
|AI case assessment questionnaire|Provides a standardized evaluation framework for AI cases reported through the AI Risk and Compliance Workspace, Employee Center, or email. Supports consistent evaluation, case prioritization, and root cause analysis. Delivered with AI Case Management \(`sn_ai_case_mgmt`\). Role required: AI case analyst \[sn\_ai\_case\_mgmt.ai\_case\_analyst\] or AI risk and compliance analyst \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_analyst\].|AI cases|Draft|During the investigation phase, after the case is triaged and assigned to an analyst.|

**Parent Topic:**[AI Risk and Compliance reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/ai-risk-management/ai-risk-and-compliance-reference.md)

**Related topics**  


[Assessment templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/ai-risk-management/airc-assessment-templates.md)

[Risk assessment methodologies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/ai-risk-management/airc-rams.md)

[Risk assessment methodologies reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/ai-risk-management/airc-rams-ref.md)

