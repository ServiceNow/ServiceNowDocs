---
title: Risk assessment methodologies
description: The AI Risk and Compliance application uses risk assessment methodologies \(RAMs\) to define the scoring frameworks and classification criteria used during risk assessments.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/ai-risk-management/airc-rams.html
release: australia
product: AI Risk Management
classification: ai-risk-management
topic_type: concept
last_updated: "2026-06-09"
reading_time_minutes: 5
keywords: [risk assessment methodologies, RAM, AI Risk and Compliance, risk classification]
breadcrumb: [AI governance life cycle, Explore, AI Risk and Compliance, Governance, Risk, and Compliance]
---

# Risk assessment methodologies

The AI Risk and Compliance application uses risk assessment methodologies \(RAMs\) to define the scoring frameworks and classification criteria used during risk assessments.

## Risk assessment methodologies overview

RAMs define the scoring frameworks and classification criteria used during risk assessments.

## Risk assessment methodologies

Risk assessment methodologies \(RAMs\) define the scoring frameworks, classification criteria, and contributing factors used to evaluate risks associated with AI assets.

RAMs are used during intake, asset-level risk assessments, and bulk risk assessment projects. The content pack provides default RAMs, and administrators can create custom RAMs to meet organizational requirements.

<table><thead><tr><th>

RAM

</th><th>

Applies to

</th><th>

Purpose

</th><th>

When used

</th></tr></thead><tbody><tr><td>

Risk classification for AI system

</td><td>

AI systems

</td><td>

Classifies AI systems by regulatory risk level based on factors captured during intake or assessment.

</td><td>

During intake screening or early assessment to determine initial regulatory risk classification. When configured and applied to the AI use case request form, this RAM evaluates responses in the Use and Purpose section and assigns a risk classification such as High, Medium, Low, or Unacceptable.

 If the AI Risk and Compliance admin doesn't complete the required configuration steps, the classification defaults to **To Be Determined**.

</td></tr><tr><td>

Automated risk classification for AI system

</td><td>

AI systems

</td><td>

Automatically assigns an initial regulatory risk classification based on Use and Purpose responses.

</td><td>

During intake when automated screening is enabled.

</td></tr><tr><td>

Risk assessment for AI inventory

</td><td>

AI systems, models, datasets

</td><td>

Evaluates individual risks using likelihood, impact, and control effectiveness to calculate inherent and residual risk scores.

</td><td>

During asset-level and bulk risk assessment projects. Individual risk scores roll up to form an aggregated risk score visible on the AI asset record and the Risk and Compliance dashboard.

 This RAM is the default for bulk risk assessment projects. You can also specify it as the default primary RAM for all risk assessments using the `sn_grc_ai_gov.aisystem_primary_ram` property.

</td></tr><tr><td>

Risk classification for AI model or dataset

</td><td>

AI models, datasets

</td><td>

Classifies models and datasets by risk level based on characteristics, data sensitivity, and intended use.

</td><td>

When models or datasets require independent governance evaluation. Unlike AI system classification RAMs, this RAM isn't applied through a global property.

 It's selected when initiating a risk assessment on an AI model or dataset and evaluates characteristics such as data sensitivity, intended use, and associated risk factors.

</td></tr></tbody>
</table>For information about coordinating multiple risk assessments together, see [Risk assessment project in AI Risk and Compliance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/ai-risk-management/risk-assessment-project-airc.md).

**Important:** Automated and advanced risk scoring behavior depends on RAM configuration. To enable risk score roll-up across AI assets, install the Advanced Risk application and migrate to Advanced Risk Assessments. This is a one-way configuration change.

## Risk assessment methodology configuration

Administrators can configure which risk assessment methodologies \(RAMs\) are applied during intake, assessment, and risk evaluation workflows.

Configuration options include specifying default RAMs for AI systems, models, and datasets, and enabling automated or advanced risk calculation behavior.

To configure the default RAM for AI system risk classification at intake, set the `sn_grc_ai_gov.ai_system_risk_classification_ram` property.

To configure automated risk classification during intake, specify the `sn_grc_ai_gov.ai_system_automated_risk_classification_asmt_ram` property.

To define the default RAM used for risk assessments across AI systems, set the `sn_grc_ai_gov.aisystem_primary_ram` property.

For more information, see [Set up AI Risk and Compliance properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/ai-risk-management/configure-airc-properties.md).

**Important:** To enable risk score roll-up across AI assets, install the Advanced Risk application and set the Migrate to Advanced Risk Assessments property to Yes. This is a one-way configuration change that permanently transitions risk calculation and roll-up behavior to the Advanced Risk framework. See [Set up Advanced Risk assessments properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/ai-risk-management/advanced-risk-assessments-properties-airc.md).

## Automated risk classification workflow

Automated Risk Classification connects intake screening, assessments, and risk evaluation into a single governance flow. Information captured during the intake request, specifically responses provided by the Product Owner in the Use and Purpose section, is reused across subsequent assessments and contributes directly to how AI systems are classified as High, Medium, or Low risk.

Assessment templates, RAMs, and Post Assessment Actions work together to help ensure that qualitative context, regulatory impact, and quantitative risk scoring are consistently applied throughout the AI governance life cycle.

A typical assessment sequence for an AI system demonstrates how these components are interconnected:

1.  During intake, the Automated risk classification for AI system RAM evaluates responses captured in the Use and Purpose section of the AI use case request and assigns an initial regulatory risk classification.
2.  During the Assess phase, the risk assessment captures information about the system's potential impact on privacy, fairness, and other fundamental rights. Responses from the Use and Purpose section are carried forward to provide continuity and reduce duplicate data entry.
3.  Post Assessment Actions evaluate the risk assessment responses and automatically associate applicable risk statements and control objectives with the assessment record based on configured automation rules.
4.  An AI Risk and Compliance analyst reviews the prescribed list of generated risks and control objectives to validate accuracy, relevance, and applicability before governance records are finalized.
5.  After the assessment is marked as closed complete, the system generates risk and control records and maps them to the AI asset. The Risk assessment for AI inventory RAM then evaluates each identified risk using quantitative scoring to calculate inherent and residual risk scores.
6.  For AI systems subject to the EU AI Act, additional assessments such as the EU AI Act Conformity Assessment and the Fundamental Rights Impact Assessment \(FRIA\) provide specialized regulatory evaluation.

Throughout this progression, assessment outcomes and risk scores inform governance decisions about whether an AI system can advance to the next life-cycle phase. For an overview of how these activities align with life-cycle stages, see [AI governance life cycle](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/ai-risk-management/ai-gov-lifecycle.md).

**Note:** Automated risk classification provides early risk context only. It doesn't approve deployment, initiate life-cycle workflows, or replace downstream impact or risk assessments.

