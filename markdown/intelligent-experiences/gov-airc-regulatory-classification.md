---
title: Classifying AI assets by regulatory risk
description: Regulatory risk classification places an AI asset in a risk rating, such as Low or High, based on the score from a risk assessment.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/gov-airc-regulatory-classification.html
release: australia
topic_type: concept
last_updated: "2026-10-05"
reading_time_minutes: 4
keywords: [regulatory risk classification, automated risk classification, Use and purpose, AI Risk and Compliance]
breadcrumb: [Reviewing regulatory classification and compliance status, Reviewing AI governance posture and compliance status, Managing risk and compliance, Govern AI assets, AI Control Tower, Enable AI experiences]
---

# Classifying AI assets by regulatory risk

Regulatory risk classification places an AI asset in a risk rating, such as Low or High, based on the score from a risk assessment.

A regulatory risk classification is the inherent rating that a risk assessment produces for an AI asset. The AI Risk and Compliance application uses the classification to group AI assets, such as AI systems, AI models, and datasets, into rating bands on the Regulatory risk classification donut chart. For more information about how to read the chart, see [Reviewing regulatory classification and compliance status](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/gov-airc-regulatory-status.md).

For the risk assessment methodologies \(RAMs\), formulas, risk ratings, and factors, see [Regulatory risk classification reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/gov-airc-ref-regulatory-classification.md).

## How automated classification works

The Automated risk classification for AI system RAM produces the classification without an assessor. For the classification that an assessor produces, see [Risk rating calculation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/gov-airc-risk-score-calculation.md).

The automated classification scores six factors from the Use and purpose responses. Each response option carries a point value, and each factor adds up the points of the fields that it uses. The inherent score is the highest of the six factor scores. The system converts the score to a rating.

A factor whose points total is 9000 or more scores 10. That score places the asset in the top rating band, Unacceptable.

If an asset has no Use and purpose record, every factor scores 0 and the classification is To be determined.

**Warning:**

The system generates the automated classification without an assessor. The classification can be inaccurate or incomplete, for example, when the Use and purpose responses are out of date. Review the classification and the responses that produced it before you rely on it.

## Example: Customer service chatbot

A support team registers a customer service chatbot as an AI system. The chatbot drafts replies to customer emails, and it uses past support tickets that contain customer names and account details. In the Use and purpose section, the team answers the questions about the chatbot:

-   For **Type of output produced**, they select **Generated Content**, which carries 50 points.
-   For **Data used by the system**, they select **Profile or Account Data**, which carries 9000 points.

The Data &amp; Model Risks factor adds these points: `50 + 9000 = 9050`. Because the total is 9000 or more, the factor score is 10, regardless of the other five factors. The highest factor score becomes the inherent score, so the chatbot's inherent score is 10 and its classification is Unacceptable.

## When and how the classification is applied

The system calculates the classification when the asset is created. After the asset moves to the Managed state, the system revises the classification when the Use and purpose fields or the regulatory risk classification are updated.

Automated classification runs only when all of the following are true:

-   The **sn\_grc\_ai\_gov.ai\_system\_automated\_risk\_classification\_asmt\_ram** property specifies a RAM.
-   The specified RAM is published.
-   The Use and purpose record is linked to the governance details record of an AI asset.

If a condition isn't met, the system doesn't create a classification assessment and the classification remains To be determined.

When the conditions are met, the system completes these actions:

1.  Runs the automated risk assessment subflow in the background.
2.  Stores the resulting inherent rating on the governance details record of the asset.
3.  Copies the inherent rating to the **Risk Classification** field of the related entity of the AI system. The system updates the related entity only when the rating changes.

For unmanaged AI assets, the classification is based on the Use and purpose data on the governance details record of the asset.

The system can cancel a classification assessment that is still open for the related entities of an AI asset. An assessment is open when its status isn't Completed, Archived, or Cancelled. A canceled assessment doesn't produce a classification. The system doesn't change assessments that are completed, archived, or canceled. The system cancels open classification assessments when the AI asset's **Active** field changes to false, such as when you retire or cancel the asset.

## Classification and aggregated inherent risk

The regulatory risk classification of an AI asset is separate from the aggregated inherent risk rating that the risk rollup calculates for an AI system. The classification comes from the classification RAM. The aggregated inherent rating comes from the risk assessments of the risks that belong to the AI system. For the aggregated rating, see Risk rating calculation.

