---
title: Risk scoring
description: Calculate a risk score for an enterprise model record based on two vectors: likelihood and impact.
locale: en-US
release: xanadu
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Exploring Enterprise Asset Management, Enterprise Asset Management, IT Asset Management]
---

# Risk scoring

Calculate a risk score for an enterprise model record based on two vectors: likelihood and impact.

Assets associated to a model inherit the risk score values of the model. However, you can override the model risk scores by defining risk scores for the assets that are different from the risk score values specified on the model.

Access the Risk modules for the Enterprise Asset Management application by navigating to **Asset** &gt; **Enterprise Risk Configuration**. Use the following modules to enter configuration values for likelihood, impact, and score.

-   **Risk Likelihood**
-   **Risk Impact**
-   **Risk Score**

**Note:** For details on configuring values for likelihood, impact, and score, see [Create configuration values for risk likelihood](../task/risk-likelihood-config.md), [Create configuration values for risk impact](../task/risk-impact-config.md), or [Create configuration values for risk scores](../task/risk-score-config.md).

After you’ve configured the values in the Risk modules and frozen them, the heat maps are rendered on the following views on the Enterprise Asset Workspace:

-   Enterprise asset estate view: heat map for asset scores
-   Enterprise model management view: heat map for model risk scores.

If a model is no longer in the **Build** stage and you update the Model's risk scores, you can propagate the updated values to the associated assets using the **Update risk** button on the model form. On clicking this button, the **EAM - Update model risk values to asset** scheduled job runs and updates the risk values for all the assets associated with this model.

**Note:** If the model is in the **Build** stage, the **Update risk** button doesn't appear.

