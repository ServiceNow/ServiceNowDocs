---
title: AI models
description: An AI model goes through design, deployment, and monitoring in accordance with structured governance frameworks that support ethical use, regulatory compliance, and risk mitigation throughout its life cycle.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/ai-risk-management/ai-model-airc.html
release: australia
product: AI Risk Management
classification: ai-risk-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [AI model, AI governance, model life cycle, aggregated risk score, AI Risk and Compliance]
breadcrumb: [AI assets, Explore, AI Risk and Compliance, Governance, Risk, and Compliance]
---

# AI models

An AI model goes through design, deployment, and monitoring in accordance with structured governance frameworks that support ethical use, regulatory compliance, and risk mitigation throughout its life cycle.

An AI model is developed by training on large datasets using machine learning or other AI techniques. The model learns data relationships to generalize outcomes for new, unseen inputs. AI models are used in applications such as language processing, image recognition, and recommendation systems.

Each model performs a defined task like classification, regression, or content generation. Models must be evaluated for accuracy, reliability, and robustness in real-world scenarios. Models are also assessed for risks such as bias, opacity, and unintended behavior.

Regular validation and performance monitoring support ongoing model effectiveness and stability. Clear documentation helps maintain transparency and supports informed decision-making. Adhering to ethical guidelines and legal standards is critical throughout the model life cycle.

The following image shows the overview page of an AI model.

\[Omitted image "ai-model-overview-page.png"\] Alt text: Overview page of an AI model showing risk score, details, and related assets

An AI model record provides an aggregated risk score. The individual risk scores for entities that have Risk assessment for AI inventory as the Risk Assessment Methodology \(RAM\) roll up to form an aggregated risk score. You can see the aggregated risk score under the Details tab of the AI system record in the **Aggregated risk score** section. For more information about how risk score is rolled up, see [Risk score rollup in Advanced Risk Assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-risk-management-workspace/risk-rollup-ara-concept.md).

**Important:** To see the aggregated risk score, you must enable the **Migrate to Advanced Risk Assessments** \(`sn_risk_advanced.migrate_to_advanced_risk`\) under **All** &gt; **Advanced Risk** &gt; **Properties**.

**Note:** You can see this section only if the Advanced Risk application is installed.

Aggregated risk score consolidates individual risks such as bias, drift, and security, to inform departmental or enterprise-level AI risk profiles, enabling higher-level visibility and oversight. For example, several customer-facing AI models exhibiting signs of bias can lead to organizational risks. Aggregated risk score enables the AI Risk and Compliance team to obtain a consolidated view of AI risks across multiple models, teams, and business units, moving beyond fragmented risk assessments.

## Related AI assets

The Related AI assets section includes the following assets for an AI model:

-   AI systems that use this AI model
-   Training datasets used within this AI model
-   Evaluation datasets used within this AI model

