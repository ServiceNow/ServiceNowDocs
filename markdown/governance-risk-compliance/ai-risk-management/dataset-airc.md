---
title: Datasets
description: Datasets in AI Risk and Compliance capture and govern the data used by AI models, enabling organizations to evaluate risk, ensure compliance, and maintain transparency across the AI asset life cycle.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/ai-risk-management/dataset-airc.html
release: brazil
product: AI Risk Management
classification: ai-risk-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [dataset, AI governance, aggregated risk score, AI Risk and Compliance, data lineage]
breadcrumb: [AI assets, Explore, AI Risk and Compliance, Governance, Risk, and Compliance]
---

# Datasets

Datasets in AI Risk and Compliance capture and govern the data used by AI models, enabling organizations to evaluate risk, ensure compliance, and maintain transparency across the AI asset life cycle.

The AI dataset supports governance objectives by capturing key information about AI models, including risk assessments, compliance status, ownership, audit trails, and performance metrics. It also enables effective oversight, accountability, and decision-making within the organization. The quality and composition of a dataset directly impact the performance, fairness, and accuracy of the AI model. Well-curated datasets help verify that models learn meaningful patterns and generate reliable outputs in real-world scenarios.

Each dataset should be evaluated for completeness, accuracy, and relevance to the intended use case. Bias in datasets can lead to unfair or inaccurate model predictions and should be identified and mitigated. Tracking data lineage helps verify traceability, transparency, and accountability in how datasets are used and maintained.

Manage datasets according to applicable data protection regulations, privacy laws, and organizational data handling policies. Regular reviews and updates help maintain dataset quality and reflect evolving data standards or business needs.

The following image shows the overview page of datasets.

\[Omitted image "datasets-overview-page.png"\] Alt text: Overview page listing AI datasets with columns for name, status, risk score, and owner

Individual risk scores for entities that use Risk assessment for AI inventory as the Risk Assessment Methodology \(RAM\) roll up to form the aggregated risk score. An AI dataset record provides an aggregated risk score. You can see the aggregated risk score under the Details tab of the AI system record in the **Aggregated risk score** section. For more information about how risk score is rolled up, see [Risk score rollup in Advanced Risk Assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/grc-risk-management-workspace/risk-rollup-ara-concept.md).

**Note:**

To see the aggregated risk score, you must enable the Migrate to Advanced Risk Assessments **\(sn\_risk\_advanced.migrate\_to\_advanced\_risk\)** under **All** &gt; **Advanced Risk** &gt; **Properties**.

**Note:** This section appears only if the Advanced Risk application is installed.

The aggregated risk score consolidates individual risks such as bias, drift, and security, to inform departmental or enterprise-level AI risk profiles, enabling higher-level visibility and oversight. For example, several customer-facing AI models exhibiting signs of bias can lead to organizational risks. Aggregated risk score enables the AI Risk and Compliance team to obtain a consolidated view of AI risks across multiple models, teams, and business units, rather than relying on fragmented risk assessments.

## Related AI assets

The Related AI assets section lists the following for an AI dataset:

-   AI systems: The AI systems that use this AI dataset.
-   AI models: The AI models that use this AI dataset.

