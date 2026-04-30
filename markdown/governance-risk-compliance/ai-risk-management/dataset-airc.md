---
title: Datasets
description: A dataset is a curated collection of structured data used to develop, deploy, and monitor AI systems in line with organizational policies, regulations, and ethical standards.
locale: en-US
release: yokohama
product: AI Risk Management
classification: ai-risk-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [AI assets, Explore, AI Risk and Compliance, Governance, Risk, and Compliance]
---

# Datasets

A dataset is a curated collection of structured data used to develop, deploy, and monitor AI systems in line with organizational policies, regulations, and ethical standards.

The AI dataset supports governance objectives by capturing key information about AI models, including risk assessments, compliance status, ownership, audit trails, and performance metrics. It also enables effective oversight, accountability, and decision-making within the organization. The quality and composition of a dataset directly impact the performance, fairness, and accuracy of the AI model. Well-curated datasets help verify models learn meaningful patterns and generate reliable outputs in real-world scenarios.

Each dataset should be evaluated for completeness, accuracy, and relevance to the intended use case. Bias in datasets can lead to unfair or inaccurate model predictions and should be identified and mitigated. Tracking data lineage helps verify traceability, transparency, and accountability in how datasets are used and maintained.

Datasets must comply with data protection regulations, including privacy laws and organizational data handling policies. Regular reviews and updates help maintain dataset quality and reflect evolving data standards or business needs.

The following image shows the overview page of datasets.

![Datasets overview page](../image/datasets-overview-page.png "Datasets overview page")

An AI dataset record provides an aggregated risk score. The individual risk scores for entities, that have Risk assessment for AI inventory as the Risk Assessment Methodology \(RAM\) roll-up and form an aggregated risk score. You can see the aggregated risk score under the Details tab of the AI system record in the **Aggregated risk score** section. For more information about how risk score is rolled up, see [Risk score rollup in Advanced Risk Assessment](../../grc-risk/concept/risk-rollup-ara-concept.md).

**Important:** To see the aggregated risk score, you must enable the **Migrate to Advanced Risk Assessments** \(`sn_risk_advanced.migrate_to_advanced_risk`\) under **All** &gt; **Advanced Risk** &gt; **Properties**.

**Note:** You can see this section only if the Advanced Risk application is installed.

Aggregated risk score consolidates individual risks such as bias, drift, and security, to inform departmental or enterprise-level AI risk profiles, enabling higher-level visibility and oversight. For example, several customer-facing AI models exhibiting signs of bias can lead to organizational risks. Aggregated risk score enables the AI Risk and Compliance team to obtain a consolidated view of AI risks across multiple models, teams, and business units, moving beyond fragmented risk assessments.

## Related AI assets

The Related AI assets section lists the following for an AI dataset:

-   AI systems: The AI systems that use this AI dataset.
-   AI models: The AI models that use this AI dataset.

