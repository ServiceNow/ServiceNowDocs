---
title: AI models
description: An AI model is designed, deployed, and monitored in accordance with structured governance frameworks. These frameworks ensure the AI model’s ethical use, regulatory compliance, and risk mitigation throughout its lifecycle.
locale: en-US
release: yokohama
product: AI Risk Management
classification: ai-risk-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [AI assets, Explore, AI Risk and Compliance, Governance, Risk, and Compliance]
---

# AI models

An AI model is designed, deployed, and monitored in accordance with structured governance frameworks. These frameworks ensure the AI model’s ethical use, regulatory compliance, and risk mitigation throughout its lifecycle.

An AI model is developed by training on large datasets using machine learning or other AI techniques. The model learns data relationships to generalize outcomes for new, unseen inputs. AI models are used in applications such as language processing, image recognition, and recommendation systems.

Each model performs a defined task like classification, regression, or content generation. They must be evaluated for accuracy, reliability, and robustness in real-world scenarios. Models are also assessed for risks such as bias, opacity, and unintended behavior.

Regular validation and performance monitoring ensure ongoing model effectiveness and stability. Clear documentation helps maintain transparency and supports informed decision-making. Compliance with ethical guidelines and legal standards is critical throughout the model’s life-cycle.

The following image shows the overview page of an AI model.

![AI model overview page](../image/ai-model-overview-page.png "AI model overview page")

An AI model record provides an aggregated risk score. The individual risk scores for entities, that have Risk assessment for AI inventory as the Risk Assessment Methodology \(RAM\) roll-up and form an aggregated risk score. You can see the aggregated risk score under the Details tab of the AI system record in the **Aggregated risk score** section. For more information about how risk score is rolled up, see [Risk score rollup in Advanced Risk Assessment](../../grc-risk/concept/risk-rollup-ara-concept.md).

**Important:** To see the aggregated risk score, you must enable the **Migrate to Advanced Risk Assessments** \(`sn_risk_advanced.migrate_to_advanced_risk`\) under **All** &gt; **Advanced Risk** &gt; **Properties**.

**Note:** You can see this section only if the Advanced Risk application is installed.

Aggregated risk score consolidates individual risks such as bias, drift, and security, to inform departmental or enterprise-level AI risk profiles, enabling higher-level visibility and oversight. For example, several customer-facing AI models exhibiting signs of bias can lead to organizational risks. Aggregated risk score enables the AI Risk and Compliance team to obtain a consolidated view of AI risks across multiple models, teams, and business units, moving beyond fragmented risk assessments.

## Related AI assets

The Related AI assets section lists the following for an AI model:

-   AI systems: The AI systems that use this AI model.
-   Training datasets: The training datasets used within this AI model.
-   Evaluation datasets: The evaluation datasets used within this AI model.

