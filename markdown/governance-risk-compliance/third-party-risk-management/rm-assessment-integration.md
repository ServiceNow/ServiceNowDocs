---
title: Integrating Third-party Risk Management with Risk Management
description: Integrating Risk Management with Third-party Risk Management lets you model enterprise risks and use third‑party assessments to dynamically update risk posture and scores for third parties and engagements. Optional TPRM rules can trigger assessments or remediation work when risks change.
locale: en-US
release: yokohama
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Integrate, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Integrating Third-party Risk Management with Risk Management

Integrating Risk Management with Third-party Risk Management lets you model enterprise risks and use third‑party assessments to dynamically update risk posture and scores for third parties and engagements. Optional TPRM rules can trigger assessments or remediation work when risks change.

If you have the Risk Management and Third-party Risk Management applications installed:

Third parties and engagements can be represented as entities in Risk Management \(for example, using an entity type such as Vendors\), enabling consistent association of risk statements and scoring.

In Third-party Risk Management, when a questionnaire is sent to a third party or an engagement and they respond, assessment ratings are calculated and then rolled up to the associated third party and engagement, updating their risk posture and scores.

Responses dynamically update risk posture and scoring at the assessment level, and scores aggregate to the third party and engagement according to the configured rollup method \(MIN, MAX, or AVG\). Both Risk Management users and third‑party risk assessors can monitor risk status.

Optionally, TPRM rules \(such as provider‑based submission rules\) can trigger assessments or create issues/tasks and send notifications when external risk‑intelligence ratings change.

For more information on implementing Risk Management, see [Risk Management implementation](../../grc-risk/concept/risk-impl-overview.md).

-   **[Manually add a risk to a third party or engagement](../task/tprm-add-risks-tp.md)**  
If you’re using both Risk Management and Third-party Risk Management, you can associate risks and risk statements with third parties and engagements. These associations influence risk posture and scoring.

**Parent Topic:**[Integrating TPRM with other applications](../../grc-vendor-risk/concept/integrating-with-tprm.md)

**Related topics**  


[Define the risk appetite for a risk](../../grc-workspace-risk/task/define-risk-appetite-on-risk.md)

[Create a risk statement](../../grc-risk/task/t_CreateRiskState.md)

[Define the risk appetite for a risk statement](../../grc-workspace-risk/task/define-risk-appetite-on-risk-statement.md)

