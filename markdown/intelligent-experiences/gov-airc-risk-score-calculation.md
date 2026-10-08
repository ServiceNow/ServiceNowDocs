---
title: Risk rating calculation
description: The inherent, control effectiveness, and residual ratings of an AI system come from risk assessment scores that a risk rollup aggregates.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/gov-airc-risk-score-calculation.html
release: brazil
topic_type: concept
last_updated: "2026-10-05"
reading_time_minutes: 5
keywords: [inherent risk, control effectiveness, residual risk, risk aggregation, primary RAM, AI Risk and Compliance]
breadcrumb: [Reviewing AI risk posture, Reviewing AI governance posture and compliance status, Managing risk and compliance, Govern AI assets, AI Control Tower, Establishing AI governance, Enable AI Experiences]
---

# Risk rating calculation

The inherent, control effectiveness, and residual ratings of an AI system come from risk assessment scores that a risk rollup aggregates.

## How the system calculates risk scores

AI Risk and Compliance calculates the risk scores of an AI system in two stages. First, a risk assessment scores each risk that belongs to the related entities of the AI system. Second, the Advanced Risk rollup engine aggregates the scores of those risks into one inherent rating, one control effectiveness rating for the AI system. For how the rollup works in general, see [Risk score rollup in Advanced Risk Assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/risk-rollup-ara-concept.md).

For the formulas, rating bands, and rollup settings, see [AI risk score calculation reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/gov-airc-ref-risk-score-calculation.md).

**Important:**

The rollup requires the Advanced Risk application. Install it and set the **Migrate to Advanced Risk Assessments** property to **Yes** before the inherent, control effectiveness ratings become available. This is a one-way configuration change.

The predefined risk assessment methodology \(RAM\) named Risk assessment for AI inventory defines the scoring logic. It's a risk-based RAM with inherent, control assessments, and it applies to AI systems, AI models, and datasets alike: every AI digital asset is represented by the same underlying AI system entity map record regardless of its asset type, so the same rollup and primary RAM apply no matter which asset type you're viewing. It ships in the Draft state, so publish it or a custom RAM before you use it.

**Note:**

The aggregated inherent rating of an AI system is separate from its regulatory risk classification. The aggregated rating comes from the risk rollup. The classification comes from the classification RAM. For the classification, see [Classifying AI assets by regulatory risk](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/gov-airc-regulatory-classification.md).

## Score types

Each risk is scored before the rollup.

-   **Inherent risk**

    Risk level before controls are considered, based on the inherent assessments of the contributing risks. For each risk, an assessor answers two choice factors, Impact and Likelihood. The score of each factor is the value of the option that the assessor selects, and the inherent score is the average of the two factor scores.

-   **Control effectiveness**

    Measure of how well the controls address the risks, based on the control assessments of the contributing risks. For each risk, the system calculates the score from the status and weight of its controls. No assessor input is needed.


## Example: Fraud detection model

A fraud detection model has three active controls. The access control review is compliant and carries the most weight, 100, because restricting who can modify the model is the most important safeguard. The data retention policy and the bias testing control are both non-compliant, each weighted at 10. The control effectiveness is `(100 ÷ 120) × 100 = 83`, close to a perfect score, but because two controls are still non-compliant, it lands in the Needs improvement band \(level 1\) rather than Effective.

## Primary RAM

The rollup runs against one RAM for each AI system, called the primary RAM. A RAM can be the primary RAM only when it is published, assesses risks, and belongs to the AI risk and compliance domain. Each AI system stores its own primary RAM. If you remove the primary RAM from an AI system, the AI system no longer shows rollup scores.

When you don't set a primary RAM, the system selects a default. You can set the default in the **sn\_grc\_ai\_gov.aisystem\_primary\_ram** property.

## Aggregation to the AI system

The rollup includes the active related entities of the AI system that use the same primary RAM, the risks of those entities, and their assessments in the Monitor state. The rollup excludes third-line audit entries, and it skips AI systems in the Retired or Canceled state.

The rollup averages the scores of the contributing risks and converts the average to a rating band. The rollup takes the maximum of the annual loss expectancy values.

## Example: Loan approval assistant

A loan approval assistant has three contributing risks: unauthorized access to applicant data \(inherent rating High, 7\), model drift from outdated training data \(inherent rating Medium, 4\), and dependency on a single data vendor \(inherent rating Low, 1\). The average is `(7 + 4 + 1) ÷ 3 = 4`, so the inherent rating of the AI system is Medium. The control effectiveness ratings of the AI system are aggregated the same way from the values of the same risks.

## When scores are recalculated

Each AI system has one risk rollup result. The system flags the result for recalculation after the primary RAM of the AI system is set or changed, or after a score-affecting change on a related entity that uses the primary RAM. A scheduled job then recalculates the scores. Scores on the AI system don't change at the moment that an assessment changes. They update after the next scheduled recalculation.

## Where the scores appear

The ratings appear on the AI system record and in the Risk posture charts and risk heat map. The Risk posture page shows the All assets by aggregated risk score chart and the Risk heat map, and you can switch the charts between inherent and residual risk. For how to read them, see [Reviewing AI risk posture](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/gov-airc-risk-posture.md). To see which assessments contributed to the score of an AI system, use the contributing assessments of the risk rollup result.

## Review of calculated ratings

The system calculates the control effectiveness, and aggregated ratings automatically, without an assessor. The ratings can be inaccurate or incomplete, for example, when controls or assessments are out of date. Review the ratings and the assessments that produced them before you rely on them.

## Assessed classification

An assessed classification is the inherent rating that an assessor produces for an AI asset. The assessor answers Impact and Likelihood questions, and the classification is the average of the two scores. The assessed classification is separate from the automated classification, which the system calculates from the Use and purpose responses.

The system applies one of two RAMs, depending on the type of AI asset. Risk classification for AI system applies to AI systems. Risk classification for AI Model or Dataset applies to AI models and datasets. You select the RAM when the assessment starts. For the formulas, subfactor weights, and rating bands, see AI risk score calculation reference.

## Things to note for addressing errors

If the Risk and Compliance dashboards on the AI asset record page or the landing page show a `No data found` error for the risk score, see [Risk score and compliance score dashboard errors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/gov-airc-ref-troubleshooting.md).

