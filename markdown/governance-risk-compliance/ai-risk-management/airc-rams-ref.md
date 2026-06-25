---
title: Risk assessment methodologies reference
description: Reference table listing the default risk assessment methodologies \(RAMs\) installed with AI Risk and Compliance. RAMs define the scoring frameworks, classification criteria, and contributing factors used to evaluate risks associated with AI assets.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/ai-risk-management/airc-rams-ref.html
release: australia
product: AI Risk Management
classification: ai-risk-management
topic_type: reference
last_updated: "2026-05-28"
reading_time_minutes: 2
keywords: [risk assessment methodologies, RAM, AI Risk and Compliance, risk classification, risk scoring]
breadcrumb: [Reference, AI Risk and Compliance, Governance, Risk, and Compliance]
---

# Risk assessment methodologies reference

Reference table listing the default risk assessment methodologies \(RAMs\) installed with AI Risk and Compliance. RAMs define the scoring frameworks, classification criteria, and contributing factors used to evaluate risks associated with AI assets.

## Risk assessment methodologies

The following table lists the default risk assessment methodologies \(RAMs\) installed with AI Risk and Compliance. RAMs define the scoring frameworks, classification criteria, and contributing factors used to evaluate risks associated with AI assets. Administrators can create custom RAMs to meet organizational requirements.

**Important:** Automated and advanced risk scoring behavior depends on RAM configuration. To enable risk score roll-up across AI assets, install the Advanced Risk application and enable the **Migrate to Advanced Risk Assessments** property. This is a one-way configuration change. RAMs are inactive by default. Implementers should review each RAM before activating it to confirm it meets organizational requirements. For more information, see [Set up Advanced Risk assessments properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/ai-risk-management/advanced-risk-assessments-properties-airc.md) and [Risk assessment methodologies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/ai-risk-management/airc-rams.md).

|RAM|Applies to|Purpose|When used|
|---|----------|-------|---------|
|Risk classification for AI system|AI systems|Classifies AI systems by regulatory risk level based on factors captured during intake or assessment.|During intake screening or early assessment to determine initial regulatory risk classification. When configured and applied to the AI use case request form, this RAM evaluates responses in the Use and Purpose section and assigns a risk classification such as High, Medium, Low, or Unacceptable. If the AI Risk and Compliance admin doesn't complete the required configuration steps, the classification defaults to **To Be Determined**.|
|Automated risk classification for AI system|AI systems|Automatically assigns an initial regulatory risk classification based on Use and Purpose responses.|During intake when automated screening is enabled.|
|Risk assessment for AI inventory|AI systems, models, datasets|Evaluates individual risks using likelihood, impact, and control effectiveness to calculate inherent and residual risk scores.|During asset-level and bulk risk assessment projects. Individual risk scores roll up to form an aggregated risk score visible on the AI asset record and the Risk and Compliance dashboard. This RAM is the default for bulk risk assessment projects. You can specify it as the default primary RAM using the `sn_grc_ai_gov.aisystem_primary_ram` property.|
|Risk classification for AI model or dataset|AI models, datasets|Classifies models and datasets by risk level based on characteristics, data sensitivity, and intended use.|When models or datasets require independent governance evaluation. Unlike AI system classification RAMs, this RAM is not applied through a global property — it is selected when initiating a risk assessment on an AI model or dataset.|

**Parent Topic:**[AI Risk and Compliance reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/ai-risk-management/ai-risk-and-compliance-reference.md)

**Related topics**  


[Risk assessment methodologies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/ai-risk-management/airc-rams.md)

[Assessment templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/ai-risk-management/airc-assessment-templates.md)

[Assessment templates reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/ai-risk-management/airc-assessment-templates-ref.md)

