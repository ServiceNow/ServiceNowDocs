---
title: Reviewing regulatory classification and compliance status
description: Review regulatory risk classification and compliance posture to understand how AI assets align with configured governance expectations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/gov-airc-regulatory-status.html
release: zurich
topic_type: concept
last_updated: "2026-05-13"
reading_time_minutes: 4
keywords: [use]
breadcrumb: [Governance posture and compliance, Managing risk and compliance, Govern AI assets, AI Control Tower, Enable AI experiences]
---

# Reviewing regulatory classification and compliance status

Review regulatory risk classification and compliance posture to understand how AI assets align with configured governance expectations.

## Overview of regulatory classification and compliance status

Regulatory risk classification and compliance score views help you understand how AI assets are categorized and how their control posture aligns with configured frameworks.

AI assets refer to the various components and resources that are essential for the development, deployment, and operation of artificial intelligence systems. These assets can include:

1.  AI systems: The complete software or hardware infrastructure that runs AI algorithms and processes. This can include machine learning platforms, natural language processing systems, and other AI-driven applications.
2.  AI models: The mathematical and computational models that are trained on data to perform specific tasks. These models can range from simple linear regression models to complex deep learning neural networks.
3.  AI datasets: The collections of data used to train, validate, and test AI models.

For more information, see [AI systems](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/ai-system-airc.md), [AI models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/ai-model-airc.md), and [Datasets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/dataset-airc.md).

At the portfolio level, you can get a snapshot view of the regulatory risk classification for your AI portfolio. This classification groups AI assets into categories such as unacceptable, high, medium, and low. Compliance views show an overall compliance score and framework-related posture for authority documents or policies.

## Regulatory risk classification

Regulatory risk classification widget presents a donut chart which organizes AI assets into risk levels based on their regulatory risk assessment results. This section displays the risk classifications of AI systems, AI models, and Datasets using donut charts. The risks are qualitatively classified as **Low**, **Medium**, **High**, **Unacceptable**, **Critical**, and **To be determined**. The risk level displayed for each asset is the regulatory risk classification assigned when the asset's regulatory risk classification assessment completes. This dashboard widget enables your governance teams, compliance officers, and AI administrators to quickly assess risk exposure and identify assets requiring intervention.

**Note:**

-   All AI assets marked as managed are evaluated
-   Only assets with a completed regulatory risk classification assessment are categorized into a risk level
-   Assets labeled as "To be determined" are excluded from risk classification charts and reports until an assessment is completed

How this is calculated: The risk level shown for an asset comes from the `risk_score` field on the asset's governance details record. This field is populated when the asset's regulatory risk classification assessment completes, and the widget reflects that value in real time on every page load. Assets without a completed assessment display as **To be determined** and are excluded from the risk classification counts until an assessment finishes.

\[Omitted image "image.aict-govern-regulatory-risk-classification"\] Alt text:

## Compliance score

Framework-specific compliance posture and issue indicators help you understand whether governance coverage is available for the selected frameworks and which areas may require additional attention.

Compliance scores measure how well AI systems conform to applicable regulations, policies, and controls. The section shows compliance based on controls implemented. By default, compliance scores are displayed for the priority frameworks configured in your environment. Each framework's citations, and any child citations, are mapped to control objectives, and each citation's compliance score is calculated based on its control attestations.

You can choose to view compliance data by selecting one of two options: **Authority Documents** or **Policies**. Additionally, you can view the overall compliance score percentage, along with the number of compliant and non-compliant authority documents and policies, by using the drop-down filter to select specific authority documents or policies. You can also see all the issues that require immediate attention and AI cases related to each authority document or policy.

Compliance score calculation:

1.  Each AI system is linked to one or more entities or profiles through the entity map record \(sn\_grc\_ai\_gov\_ai\_system\_entity\_map\)
2.  Each entity has its own compliance score calculated by the Policy &amp; Compliance engine. The score is based on the state of its controls \(whether controls pass or fail compliance tests and attestations\)
3.  The AI system's compliance score is calculated as the average of all active entities' compliance scores, rounded to a whole number

**Note:**

-   Compliance scores depend on linked entities; ensure all relevant entities are properly mapped to AI systems for accurate scoring
-   **Retired** and **Canceled** AI systems are excluded from compliance score calculations to maintain focus on active systems
-   Compliance scores are averaged across all active linked entities; individual entity scores may vary

The authority documents are provided solely for informational and guidance purposes to assist with the initial setup of AI Risk and Compliance frameworks. It doesn't constitute legal advice or assurance of regulatory compliance. You're solely responsible for ensuring that all use of the content complies with applicable laws, regulations, directives, and industry standards in their jurisdictions.

\[Omitted image "image.aict-govern-compliance-score"\] Alt text:

## How data is determined

Regulatory status data is updated through scheduled and on-demand processes that evaluate your AI assets and calculate their risk and compliance metrics.

Regulatory risk classification data:

-   The `risk_score` field on the governance details record is populated when the asset's regulatory risk classification assessment completes
-   Status charts and reports are generated in real time based on live values; no scheduled refresh is required
-   Widgets and visualizations reflect current data on every page load

Compliance score data:

-   Individual AI system compliance scores are calculated by scheduled and on-demand jobs
-   System scores are based on the compliance scores of linked entities, which are maintained by the Policy &amp; Compliance engine

## Scheduled and on-demand jobs

Regulatory status data is kept current through the following automated processes:

For regulatory risk classification:

-   No scheduled or on-demand jobs directly update risk classifications
-   The `risk_score` field is populated when a regulatory risk classification assessment completes

For compliance scores:

-   **AI system Compliance score calculation**: Calculates individual AI system compliance scores based on linked entity scores
-   **AIRC daily compliance score scheduled job**: Refreshes compliance score data for the home page compliance score widget on a daily schedule

