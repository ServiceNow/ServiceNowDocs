---
title: Offboarding AI assets review
description: Offboarding AI systems, models, and datasets helps ensure that governance, risk, and compliance requirements are addressed throughout assessment, preparation, and retirement of AI assets, including impact evaluation, residual risk management, documentation preservation, data‑handling decisions, and audit traceability.
locale: en-US
release: australia
product: AI Risk Management
classification: ai-risk-management
topic_type: concept
last_updated: "2026-05-07"
reading_time_minutes: 6
keywords: [AI offboarding, AI model retirement, AI dataset retirement, AI Risk and Compliance, AI governance, AI Control Tower]
breadcrumb: [AI governance life cycle, Explore, AI Risk and Compliance, Governance, Risk, and Compliance]
---

# Offboarding AI assets review

Offboarding AI systems, models, and datasets helps ensure that governance, risk, and compliance requirements are addressed throughout assessment, preparation, and retirement of AI assets, including impact evaluation, residual risk management, documentation preservation, data‑handling decisions, and audit traceability.

## How offboarding is handled across AI Risk and Compliance and AI Control Tower

Offboarding AI models and datasets involves both governance activities and technical life cycle actions. These responsibilities are typically shared between AI Risk and Compliance \(AIRC\) and AI Control Tower \(AICT\), with each product addressing different aspects of the offboarding process.

During offboarding, governance review may include assessing how retiring an AI asset affects users, business processes, and dependent systems, as well as determining whether continued use, reuse, or retirement of related models or datasets is appropriate.

Assessments performed during offboarding are intended to confirm that governance obligations associated with the AI asset are fully addressed before retirement, rather than to introduce new ongoing monitoring or post‑retirement obligations.

AIRC is used to perform and document governance reviews associated with offboarding, while AICT can be used to manage technical life-cycle workflows for AI assets based on governance outcomes. Offboarding is initiated when an AI asset owner \[sn\_ai\_asset\_mgmt.ai\_asset\_owner\] or steward \[sn\_ai\_governance\_ai\_steward\] submits an offboarding request in AICT, which then drives governance review activities in AIRC. For more information, see [Create offboarding requests for AI assets](https://www.servicenow.com/docs/access?context=create-ai-asset-offboarding-request&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)

When an AI model or dataset is used by one or more governed AI systems, offboarding review may include evaluating downstream dependencies to help ensure that impacted systems are updated, remediated, or retired as needed before the asset is fully offboarded.

Governance activities associated with offboarding focus on evaluating business, legal, ethical, and safety impacts, while technical life-cycle actions focus on disabling access, removing operational dependencies, and updating AI inventory records based on completed governance outcomes.

Governance activities may also include evaluating whether legal, ethical, safety, or compliance risks remain after retirement and documenting how those residual risks are mitigated, accepted, or formally closed.

## What is completed in AI Risk and Compliance during offboarding

AIRC supports the governance portion of AI asset offboarding. Through AIRC, organizations review and document risk, impact, and compliance considerations related to retiring AI models and datasets. When AI models or datasets are associated with a governed AI system, offboarding activities may be reviewed and tracked at the AI system level to help ensure complete governance coverage.

You can view AI assets and their governance status on the Operations tab in the AI Risk and Compliance Workspace. For more information, see [Operations tab](operations-tab.md).

![The list page showing AI assets in an offboarding-related state in the AI Risk and Compliance workspace.](../image/offboard-list.png "Operations tab")

For more information about the AI governance life cycle and how offboarding fits into the broader AI asset life cycle, see [AI governance life cycle](ai-gov-lifecycle.md) and [AI asset lifecycle](https://www.servicenow.com/docs/access?context=ai-asset-lifecycle&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

In AIRC, practitioners can perform activities such as reviewing regulatory risk classifications, completing or updating impact assessments, and conducting conformity or policy-alignment reviews as part of the AI life cycle.

For more information, see [Perform impact assessment on an AI use case](../task/perform-impact-assessment-of-ai-use-case.md) and [Initiate risk assessment on AI asset](../task/initiate-risk-assessment-on-ai-systems.md).

AIRC maintains governance records related to AI assets, including assessments, controls, issues, and attestations. These records remain available after an AI asset is retired, supporting audit readiness and historical traceability.

Risks and issues identified during offboarding review can be tracked and formally closed in AIRC, helping ensure that governance concerns are addressed before an AI asset is retired.

Offboarding is considered complete when required governance reviews are finished, related issues are resolved or formally accepted, and the AI asset life-cycle status is updated to retired.

For more information about resolving governance issues before asset retirement, see [Remediate an issue in AI Risk and Compliance](../task/remediate-an-issue-in-airc.md).

## Assessment behavior during offboarding

During offboarding, governance activities in AI Risk and Compliance are driven by risk classification, assessment status, and life-cycle state. AI system or model categories selected during intake \(for example, Agentic or Generative\) are captured as descriptive metadata only and don’t change assessment creation, scoring, or life-cycle behavior.

Impact or risk assessments may be created during offboarding when governance review determines that additional evaluation is required based on the asset’s risk classification and existing assessment coverage. If an active assessment of the same type already exists, a duplicate assessment isn’t created.

When offboarding is completed and the AI asset life-cycle state is updated to retired, any remaining open governance assessments associated with the asset are closed or cancelled according to configured governance rules. Historical records remain available for audit and traceability.

Offboarding review may also confirm that documentation, assessment results, and data‑handling decisions required for regulatory, audit, or investigative purposes are preserved before the AI asset is retired.

## Assessment guidance during AI asset offboarding

During offboarding, organizations may use different types of assessments in AI Risk and Compliance to support governance decisions related to retiring AI systems, models, or datasets. The specific assessments considered depend on the asset’s risk classification, usage context, and existing governance coverage.

Impact assessments are commonly used when offboarding decisions require evaluating how retiring an AI asset affects users, business processes, downstream systems, or decision‑making workflows. These assessments help determine whether retirement introduces operational, ethical, or safety impacts that must be addressed before the asset is retired.

Risk assessments may be used during offboarding to evaluate residual risks associated with an AI asset, including legal, ethical, or compliance risks that may persist after operational use ends. Risk assessments can also be used to confirm that previously identified risks are adequately mitigated, accepted, or formally closed prior to retirement.

Conformity or policy‑alignment reviews may be performed for AI assets subject to regulatory or internal governance requirements to confirm that applicable obligations have been satisfied before offboarding is finalized.

The creation and sequencing of offboarding‑related assessment tasks are managed through AI Control Tower, while AI Risk and Compliance provides the governance context, assessment records, and audit traceability needed to support offboarding decisions.

For more information about performing specific assessment types, see [Perform impact assessment on an AI use case](../task/perform-impact-assessment-of-ai-use-case.md), [Perform risk assessments on AI systems](../task/perform-risk-assessments-on-ai-systems.md), [Initiate risk assessment on AI asset](../task/initiate-risk-assessment-on-ai-systems.md), and [Initiate risk assessment on AI asset's risks](../task/request-risk-assessments-for-ai-systems.md).

