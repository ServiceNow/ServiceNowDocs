---
title: Offboarding AI assets review
description: Offboarding AI systems, models, and datasets addresses governance, risk, and compliance requirements throughout assessment, preparation, and retirement. Activities include impact evaluation, residual risk management, documentation preservation, data-handling decisions, and audit traceability.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/ai-risk-management/airc-offboarding-ai-assets.html
release: brazil
product: AI Risk Management
classification: ai-risk-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 3
keywords: [AI offboarding, AI model retirement, AI dataset retirement, AI Risk and Compliance, AI governance, AI Control Tower]
breadcrumb: [AI governance life cycle, Explore, AI Risk and Compliance, Governance, Risk, and Compliance]
---

# Offboarding AI assets review

Offboarding AI systems, models, and datasets addresses governance, risk, and compliance requirements throughout assessment, preparation, and retirement. Activities include impact evaluation, residual risk management, documentation preservation, data-handling decisions, and audit traceability.

## Offboarding responsibilities across AI Risk and Compliance and AI Control Tower

Offboarding AI system, models, and datasets involves both governance activities and technical life cycle actions. These responsibilities are typically shared between AI Risk and Compliance \(AIRC\) and AI Control Tower \(AICT\), with each product addressing different aspects of the offboarding process.

During offboarding, governance review may include assessing how retiring an AI asset affects users, business processes, and dependent systems. The review also determines whether continued use, reuse, or retirement of related models or datasets is appropriate. Additionally, assessments performed during offboarding confirm that governance requirements associated with the AI asset are fully addressed before retirement. These assessments do not introduce new ongoing monitoring or post‑retirement requirements.

AI Risk and Compliance is used to perform and document governance reviews associated with offboarding. AI Control Tower can be used to manage technical life-cycle workflows for AI assets based on governance outcomes. Offboarding is initiated when an AI asset owner \(sn\_ai\_asset\_mgmt.ai\_asset\_owner\) or steward \(sn\_ai\_governance\_ai\_steward\) submits an offboarding request in the control, which then drives governance review activities in the AI Risk and Compliance Workspace. For more information, see [Create offboarding requests for AI assets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/create-ai-asset-offboarding-request.md).

## Governance activities in AI Risk and Compliance during offboarding

AI Risk and Compliance supports the governance aspects of AI asset offboarding. Through AIRC, organizations review and document risk, impact, and compliance considerations related to retiring AI models or datasets. When AI models or datasets servers are associated with a governed AI system, offboarding activities may be reviewed and tracked at the AI system level. This helps ensure complete governance coverage.

You can view AI assets and their governance status on the Operations tab in the AI Risk and Compliance Workspace. For more information, see [Operations tab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-risk-management/operations-tab.md).

\[Omitted image "offboard-list.png"\] Alt text: List of AI assets in an offboarding-related state in the AI Risk and Compliance workspace.

For more information about the AI governance life cycle and how offboarding fits into the broader AI asset life cycle, see [AI governance life cycle](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-risk-management/ai-gov-lifecycle.md) and [AI asset lifecycle](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/ai-asset-lifecycle.md).

In AIRC, practitioners can perform activities such as reviewing regulatory risk classifications and completing or updating impact assessments. They can also conduct conformity or policy-alignment reviews as part of the AI life cycle.

For more information, see and .

Offboarding is considered complete when required governance reviews are finished, related issues are resolved or formally accepted, and the AI asset life-cycle status is updated to retired.

For more information about resolving governance issues before asset retirement, see .

## Life cycle tasks executed during AI asset offboarding

Governance life cycle tasks support review, preparation, and retirement of AI systems, models, and datasets during offboarding. These tasks help ensure governance requirements are addressed and documented before an AI asset is fully retired.

**Related topics**  


[AI governance life cycle](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-risk-management/ai-gov-lifecycle.md)

