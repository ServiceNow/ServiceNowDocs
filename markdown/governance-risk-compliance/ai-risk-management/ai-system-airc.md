---
title: AI systems
description: An AI system is an AI-powered solution that is developed, deployed, and managed under a formal governance framework. This framework ensures that the system operates in a responsible, compliant, and risk-aware manner throughout its life cycle.
locale: en-US
release: zurich
product: AI Risk Management
classification: ai-risk-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [AI assets, Explore, AI Risk and Compliance, Governance, Risk, and Compliance]
---

# AI systems

An AI system is an AI-powered solution that is developed, deployed, and managed under a formal governance framework. This framework ensures that the system operates in a responsible, compliant, and risk-aware manner throughout its life cycle.

An AI system functions within an organization’s digital or operational environment to support business activities. It enables automation, enhances data-driven decision-making, and improves overall process efficiency. The system includes components such as machine learning models, natural language processing engines, or computer vision tools.

These components are often supported by datasets, algorithms, and computing infrastructure. Together, they enable the system to analyze data, recognize patterns, and generate outcomes with minimal human intervention. Each AI system is subject to a structured evaluation process. This process assesses potential risks related to functionality, security, and societal impact. It also verifies compliance with applicable regulations, industry standards, and internal governance policies.

Governance frameworks are applied to manage the AI system throughout its life cycle. They ensure that the system operates securely and delivers predictable, explainable, and trustworthy results. Ethical principles such as fairness, accountability, and transparency are enforced through defined controls and oversight mechanisms. Regular monitoring supports responsible AI use and reduces the risk of unintended consequences.

The following image shows the overview page of an AI system.

![AI system overview page](../image/ai-system-overview-page.png "AI system overview page")

An AI system record provides an aggregated risk score. The individual risk scores for entities that have Risk assessment for AI inventory as the Risk Assessment Methodology \(RAM\) roll-up and form an aggregated risk score. You can see the aggregated risk score under the Details tab of the AI system record in the **Aggregated risk score** section. For more information about how risk score is rolled up, see [Risk score rollup in Advanced Risk Assessment](../../grc-risk/concept/risk-rollup-ara-concept.md).

**Important:** To see the aggregated risk score, you must enable the **Migrate to Advanced Risk Assessments** \(`sn_risk_advanced.migrate_to_advanced_risk`\) under **All** &gt; **Advanced Risk** &gt; **Properties**.

**Note:** You can see this section only if the Advanced Risk application is installed.

Aggregated risk score consolidates individual risks such as bias, drift, and security, to inform departmental or enterprise-level AI risk profiles, enabling higher-level visibility and oversight. For example, several customer-facing AI models exhibiting signs of bias can lead to organizational risks. Aggregated risk score enables the AI Risk and Compliance team to obtain a consolidated view of AI risks across multiple models, teams, and business units, moving beyond fragmented risk assessments.

The following image shows the aggregated risk score section:

![Details page of an AI system showing the aggregated risk score](../image/aggregated-risk-score-details-tab-ai-system.png "Aggregated risk score")

## Related AI assets

The Related AI assets section lists the following for an AI system:

-   AI models: The AI models within this AI system.
-   Datasets: The datasets used within this AI system.

**Related topics**  


[Request an AI use case](../task/request-ai-system.md)

[Request an AI model](../task/request-ai-model.md)

[Request a dataset](../task/request-dataset.md)

