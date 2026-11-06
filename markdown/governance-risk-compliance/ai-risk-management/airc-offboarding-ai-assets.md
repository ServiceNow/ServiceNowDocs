---
title: Offboarding AI assets review
description: Offboarding AI systems, models, and datasets addresses governance, risk, and compliance requirements throughout assessment, preparation, and retirement. Activities include impact evaluation, residual risk management, documentation preservation, data-handling decisions, and audit traceability.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/governance-risk-compliance/ai-risk-management/airc-offboarding-ai-assets.html
release: australia
product: AI Risk Management
classification: ai-risk-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 6
keywords: [AI offboarding, AI model retirement, AI dataset retirement, AI Risk and Compliance, AI governance, AI Control Tower]
breadcrumb: [AI governance life cycle, Explore, AI Risk and Compliance, Governance, Risk, and Compliance]
---

# Offboarding AI assets review

Offboarding AI systems, models, and datasets addresses governance, risk, and compliance requirements throughout assessment, preparation, and retirement. Activities include impact evaluation, residual risk management, documentation preservation, data-handling decisions, and audit traceability.

## Offboarding responsibilities across AI Risk and Compliance and AI Control Tower

Offboarding AI system, models, and datasets involves both governance activities and technical life cycle actions. These responsibilities are typically shared between AI Risk and Compliance \(AIRC\) and AI Control Tower \(AICT\), with each product addressing different aspects of the offboarding process.

During offboarding, governance review may include assessing how retiring an AI asset affects users, business processes, and dependent systems. The review also determines whether continued use, reuse, or retirement of related models or datasets is appropriate. Additionally, assessments performed during offboarding confirm that governance requirements associated with the AI asset are fully addressed before retirement. These assessments do not introduce new ongoing monitoring or post‑retirement requirements.

AI Risk and Compliance is used to perform and document governance reviews associated with offboarding. AI Control Tower can be used to manage technical life-cycle workflows for AI assets based on governance outcomes. Offboarding is initiated when an AI asset owner \(sn\_ai\_asset\_mgmt.ai\_asset\_owner\) or steward \(sn\_ai\_governance.ai\_steward\) submits an offboarding request in the control, which then drives governance review activities in the AI Risk and Compliance Workspace. For more information, see [Create offboarding requests for AI assets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/create-ai-asset-offboarding-request.md).

## Governance activities in AI Risk and Compliance during offboarding

AI Risk and Compliance supports the governance aspects of AI asset offboarding. Through AIRC, organizations review and document risk, impact, and compliance considerations related to retiring AI models or datasets. When AI models or datasets servers are associated with a governed AI system, offboarding activities may be reviewed and tracked at the AI system level. This helps ensure complete governance coverage.

You can view AI assets and their governance status on the Operations tab in the AI Risk and Compliance Workspace. For more information, see [Operations tab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/governance-risk-compliance/ai-risk-management/operations-tab.md).

\[Omitted image "offboard-list.png"\] Alt text: List of AI assets in an offboarding-related state in the AI Risk and Compliance workspace.

For more information about the AI governance life cycle and how offboarding fits into the broader AI asset life cycle, see [AI governance life cycle](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/governance-risk-compliance/ai-risk-management/ai-gov-lifecycle.md) and [AI asset lifecycle](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-asset-lifecycle.md).

In AIRC, practitioners can perform activities such as reviewing regulatory risk classifications and completing or updating impact assessments. They can also conduct conformity or policy-alignment reviews as part of the AI life cycle.

For more information, see [Perform impact assessment on an AI use case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/governance-risk-compliance/ai-risk-management/perform-impact-assessment-of-ai-use-case.md) and [Initiate risk assessment on AI asset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/governance-risk-compliance/ai-risk-management/initiate-risk-assessment-on-ai-systems.md).

Offboarding is considered complete when required governance reviews are finished, related issues are resolved or formally accepted, and the AI asset life-cycle status is updated to retired.

For more information about resolving governance issues before asset retirement, see [Remediate an issue in AI Risk and Compliance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/governance-risk-compliance/ai-risk-management/remediate-an-issue-in-airc.md).

## Life cycle tasks executed during AI asset offboarding

Governance life cycle tasks support review, preparation, and retirement of AI systems, models, and datasets during offboarding. These tasks help ensure governance requirements are addressed and documented before an AI asset is fully retired.

<table id="table_qhc_scj_fkc"><thead><tr><th>

Task name

</th><th>

Purpose

</th><th>

Associated action

</th><th>

Role-specific action

</th><th>

Applicable to AI asset

</th></tr></thead><tbody><tr><td class="sub-head" colspan="5">

**Assess**

</td></tr><tr><td>

Decide and justify AI System retirement

</td><td>

Identifies users, workflows, and decisions that will be affected when the AI stops. To understand how turning off the AI will affect users, workflows, and decisions. This avoids disruption, unsafe manual workarounds, or gaps in critical decision-making processes.

</td><td>

-   Take assessment
-   View assessment

</td><td>

-   AI asset owner \[sn\_ai\_asset\_mgmt.ai\_asset\_owner\]: Can take assessments
-   AI Steward \[sn\_ai\_governance.ai\_steward\]: Can view response of the assessment

</td><td>

-   AI system
-   AI model
-   Dataset

</td></tr><tr><td>

Confirm accountability and oversight

</td><td>

Ensures clear ownership and independent oversight for the offboarding process. To clearly assign responsibility and independent oversight for the offboarding process. This ensures nothing is missed and that compliance expectations are met.

</td><td>

-   Accept Work
-   Ready for review

</td><td>

AI asset owner \[sn\_ai\_asset\_mgmt.ai\_asset\_owner\]:-   Can move the task to In progress state
-   Can move task to review state

</td><td>

-   AI system
-   AI model
-   Dataset

</td></tr><tr><td class="sub-head" colspan="5">

**Pre-offboarding**

</td></tr><tr><td>

Assess residual legal, ethical, and safety risks

</td><td>

Identifies risks that may still exist after the AI is turned off \(e.g., past decisions, bias\). To identify risks that may still exist after the AI is turned off, such as past decisions, bias impacts, or legal exposure. This ensures risks are documented and managed, not ignored.

</td><td>

-

</td><td>

AI Risk &amp; Compliance Analyst \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_analyst\]: Can update the state of the record

</td><td>

-   AI system
-   AI model
-   Dataset

</td></tr><tr><td>

Capture final technical and decision documentation

</td><td>

Preserves explanations, logs, and documentation for audits or investigations. To preserve explanations, logs, and documentation showing how the AI worked. This supports audits, investigations, and future accountability even after the AI is gone.

</td><td>

-   Accept Work
-   Ready for review

</td><td>

AI asset owner \[sn\_ai\_asset\_mgmt.ai\_asset\_owner\]:-   Can move the task to In progress state
-   Can move task to review state

</td><td>

-   AI system
-   AI model
-   Dataset

</td></tr><tr><td>

Prepare users and teams for AI shutdown

</td><td>

Ensures people know the AI is going away and how decisions will continue safely. To ensure people understand the AI is being retired and how decisions or processes will continue safely without it.

</td><td>

-   Accept Work
-   Ready for review

</td><td>

AI asset owner \[sn\_ai\_asset\_mgmt.ai\_asset\_owner\]:-   Can move the task to In progress state
-   Can move task to review state

</td><td>

-   AI system
-   AI model
-   Dataset

</td></tr><tr><td>

Prepare data retention, deletion, or anonymization plan

</td><td>

Ensures data is kept or deleted in line with privacy and legal requirements. To decide what data must be kept, deleted, or anonymized after retirement. This prevents unlawful data retention and reduces privacy and misuse risks.

</td><td>

-   Accept Work
-   Ready for review

</td><td>

AI asset owner \[sn\_ai\_asset\_mgmt.ai\_asset\_owner\]:-   Can move the task to In progress state
-   Can move task to review state

</td><td>

Dataset

</td></tr><tr><td class="sub-head" colspan="5">

**Offboard**

</td></tr><tr><td>

Disable AI system and model access

</td><td>

Ensures the AI can no longer run, respond, or influence decisions. To technically ensure the AI can no longer run, respond, or influence decisions. This prevents accidental or unauthorized continued use.

</td><td>

-   Accept Work
-   Ready for review

</td><td>

AI asset owner \[sn\_ai\_asset\_mgmt.ai\_asset\_owner\]:-   Can move the task to In progress state
-   Can move task to review state

</td><td>

-   AI system
-   AI model
-   Dataset

</td></tr><tr><td>

Archive AI artifacts and metadata

</td><td>

Preserves traceability of how the AI worked in the past. To retain models and records needed to explain past AI behavior to regulators, auditors, or internal reviewers.

</td><td>

-   Accept Work
-   Ready for review

</td><td>

AI asset owner \[sn\_ai\_asset\_mgmt.ai\_asset\_owner\]:-   Can move the task to In progress state
-   Can move task to review state

</td><td>

AI model

</td></tr><tr><td>

Update AI inventory and formally close risks \(If High/Critical/unacceptable risk classification\)

</td><td>

Confirms the AI is fully retired, risks are closed, and records are audit-ready. To confirm the AI is fully retired, risks are closed, and organizational records accurately reflect its end of life.

</td><td>

-   Take assessment
-   View assessment

</td><td>

-   AI asset owner \[sn\_ai\_asset\_mgmt.ai\_asset\_owner\]: Can take assessments
-   AI Steward \[sn\_ai\_governance.ai\_steward\]: Can view response of the assessment

</td><td>

-   AI system
-   AI model
-   Dataset

</td></tr></tbody>
</table>**Related topics**  


[AI governance life cycle](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/governance-risk-compliance/ai-risk-management/ai-gov-lifecycle.md)

[Remediate an issue in AI Risk and Compliance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/governance-risk-compliance/ai-risk-management/remediate-an-issue-in-airc.md)

[Perform impact assessment on an AI use case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/governance-risk-compliance/ai-risk-management/perform-impact-assessment-of-ai-use-case.md)

