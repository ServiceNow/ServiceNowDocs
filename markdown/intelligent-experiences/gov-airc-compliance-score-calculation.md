---
title: Compliance score calculation
description: The compliance score of an AI system measures how well its controls are met, based on the scores of its active related entities.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/gov-airc-compliance-score-calculation.html
release: brazil
topic_type: concept
last_updated: "2026-10-05"
reading_time_minutes: 3
keywords: [compliance score, AI system compliance, entity compliance score, AI Risk and Compliance]
breadcrumb: [Reviewing regulatory classification and compliance status, Reviewing AI governance posture and compliance status, Managing risk and compliance, Govern AI assets, AI Control Tower, Establishing AI governance, Enable AI Experiences]
---

# Compliance score calculation

The compliance score of an AI system measures how well its controls are met, based on the scores of its active related entities.

## How the score is calculated

AI Risk and Compliance doesn't score an AI system directly. It averages the compliance scores of the entities that are linked to the AI system. For the formula, calculation rules, scheduled jobs, and properties, see [AI system compliance score calculation reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/gov-airc-ref-compliance-score.md).

An AI system links to one or more entities in the AI system entity map. The system averages the compliance scores of the active linked entities and stores the result as the compliance score of the AI system. The system skips AI systems in the Retired or Canceled state and excludes entities that belong to third-line audit entries.

**Note:**

Map every relevant entity to the AI system. An entity that isn't mapped doesn't affect the score, so a missing entity can make the score look better or worse than the real compliance posture.

## Example: Hiring assistant AI system

A hiring assistant AI system is linked to three active entities in its governance plan: Data privacy compliance \(80\), Model bias testing \(60\), and Vendor risk assessment \(70\). The compliance score of the AI system is `(80 + 60 + 70) ÷ 3 = 70`. After an AI steward also links a fourth entity, Incident response readiness, with a compliance score of 50, the score becomes `(80 + 60 + 70 + 50) ÷ 4 = 65` - mapping an additional entity can lower the overall score if that entity needs attention.

## Where the entity scores come from

The Policy and Compliance engine calculates the compliance score of each entity, based on the state of its controls, such as whether the controls pass compliance tests and attestations. Depending on configuration, this calculation can also take the scores of related entities into account. For the formula, calculation rules, and configuration options, see [Compliance score calculation of an entity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/compliance-score-calculation-pc-ws.md).

The compliance score of an AI system changes when the score of any contributing entity changes.

An individual entity's compliance score is color-coded consistently with other Policy and Compliance records: green for 80-100, yellow for 50-79, and red for 0-49.

## How and when scores are processed

The system queues an AI system for recalculation when its compliance score record is inserted. A scheduled process then completes these actions:

1.  Picks up queued records that are in the Inserted or Error state and marks them as processing.
2.  Calculates the average of the compliance scores of the related entities for each queued AI system.
3.  Stores the new score on the AI system.
4.  Removes the processed records from the queue.

If the calculation fails for an AI system, the system logs an error, but the queued record is still removed in the same run. The AI system isn't automatically retried unless a new compliance score record is queued for it again.

## Scores by authority document or policy

A compliance score relates to an authority document through the citation that the authority document is associated with. The citation is also linked to the applicable control. Based on these relationships, the system calculates the compliance score for the corresponding authority document.

The Compliance score card shows the score as a percentage on a gauge. The card also shows compliance posture for the priority frameworks, with separate tabs for authority documents and policies. Those posture scores come from the compliance of citations and their controls, and they are separate from the compliance score of the AI system. For how citation scores are calculated, see [Compliance score calculation for a citation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/compliance-score-calculation-for-a-citation.md). For how to read the compliance views, see [Reviewing regulatory classification and compliance status](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/gov-airc-regulatory-status.md).

## Review of calculated scores

The system calculates the compliance score automatically, without an assessor. The score can be inaccurate or incomplete, for example, when entities or controls are missing or out of date. Review the score and the entity scores that produced it before you rely on it.

## Things to note for addressing errors

If the Risk and Compliance dashboards on the AI asset record page or the landing page show a `No data found` error for the compliance score, see [Risk score and compliance score dashboard errors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/gov-airc-ref-troubleshooting.md).

