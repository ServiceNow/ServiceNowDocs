---
title: Managing risks scores in Enterprise Asset Management
description: Manage risk scores in the Enterprise Asset Management application by creating configuration values for risk likelihood, risk impact, and risk scores.
locale: en-US
release: australia
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Managing enterprise models and assets, Enterprise Asset Management, IT Asset Management]
---

# Managing risks scores in Enterprise Asset Management

Manage risk scores in the Enterprise Asset Management application by creating configuration values for risk likelihood, risk impact, and risk scores.

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

-   **[Create configuration values for risk likelihood](../task/risk-likelihood-config.md)**  
Use the Risk Likelihood module to create configuration values for the likelihood vector.
-   **[Create configuration values for risk impact](../task/risk-impact-config.md)**  
Use the Risk Impact module to create configuration values for the impact vector.
-   **[Create configuration values for risk scores](../task/risk-score-config.md)**  
Use the Risk Score module to create configuration values for risk score bands.

**Parent Topic:**[IT Asset Management](../../software-asset-management2/concept/it-asset-management.md)

