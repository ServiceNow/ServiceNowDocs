---
title: Predictive Intelligence release notes
description: The ServiceNow Predictive Intelligence application enables you to create and train machine learning models to improve performance, efficiency, and flexibility to your systems. Predictive Intelligence was enhanced and updated in the Xanadu release.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2025-07-29"
reading_time_minutes: 2
---

# Predictive Intelligence release notes

The ServiceNow® Predictive Intelligence application enables you to create and train machine learning models to improve performance, efficiency, and flexibility to your systems. Predictive Intelligence was enhanced and updated in the Xanadu release.

## Predictive Intelligence highlights for the Xanadu release

-   The dashboard for Prediction Results has been migrated to the Next Experience UI. Upgrading customers with existing Prediction Results dashboards can use either the Next Experience UI version or access the Core UI version from within the new dashboard.
-   The dashboard for Solution Statistics has been deprecated. Upgrading customers can continue to use their existing Solutions Statistics dashboards from the application menu.
-   New advanced options for classification solutions are available from Xanadu Patch 9.

See [Predictive Intelligence](https://www.servicenow.com/docs/access?context=predictive-intelligence-landing&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US) for more information.

## UI changes

-   **[Prediction Results dashboard](https://www.servicenow.com/docs/access?context=review-prediction-results&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

    The dashboard for Prediction Results has been migrated to the Next Experience UI. For new customers onboarding with the Xanadu release, the Prediction Results dashboard is available only in the Next Experience UI. For upgrading customers, the Core UI dashboard is also accessible from within the new dashboard. For more information, see [Track classification prediction results over time](https://www.servicenow.com/docs/access?context=review-prediction-results&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).


## Changed in this release

-   **[Leverage new advanced options for classification solutions](https://www.servicenow.com/docs/access?context=configuring-advanced-settings-ml-solutions&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US), from Xanadu Patch 9.**

    Five new advanced options are available for classification solutions, including new parameters and a new algorithm.

    -   [Configure include only top N labels](https://www.servicenow.com/docs/access?context=predictive-intel-only-top-n-labels&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US). Limit the classification model to use only the top most frequent labels. You can choose a number as the limit.
    -   [Minimum records needed for label to include it](https://www.servicenow.com/docs/access?context=predictive-intel-minimum-records-needed-label&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US). Set a threshold for the minimum number of records a label must have in your dataset to be included in model training.
    -   [Remove others label](https://www.servicenow.com/docs/access?context=predictive-intel-remove-others-label&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US). Reduce noise in the model and enhance predictive accuracy by removing records with the label "others" from training data.
    -   [Use LightGBM algo for classification model training](https://www.servicenow.com/docs/access?context=predictive-intel-lightgbm-algo&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US). Enable the LightGBM \(Light Gradient-Boosting Machine\) algorithm for training classification models.
    -   [Config parameters for model config in classification](https://www.servicenow.com/docs/access?context=predictive-intel-config-parameters-classification&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US). Customize training behavior by including a dictionary of parameters in the JSON format.

## Deprecations

The dashboard for Solution Statistics has been deprecated. Upgrading customers can continue to use their existing Solutions Statistics dashboards from the application menu. For new customers onboarding with the Xanadu release, the Solutions Statistics dashboard is not available. For more information, see [Review classification solution statistics](https://www.servicenow.com/docs/access?context=review-solution-statistics&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).

## Activation information

Predictive Intelligence is a ServiceNow AI Platform feature that is available with activation of the Predictive Intelligence Reports \(com.glide.platform\_ml\_pa\) plugin and its dependent Predictive Intelligence \(com.glide.platform\_ml\) plugin. For details, see [Install Predictive Intelligence](https://www.servicenow.com/docs/access?context=install-predictive-intelligence&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).

## Related ServiceNow applications and features

-   **[Document Intelligence](https://www.servicenow.com/docs/access?context=document-intelligence-landing&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

    Use Document Intelligence to extract and categorize key information from documents using artificial intelligence \(AI\).

-   **[Task Intelligence](https://www.servicenow.com/docs/access?context=task-intelligence&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

    Create and train machine learning models to automate task creation, triage, and investigation.


**Parent Topic:**[Intelligent Experiences release notes](intelligent-experiences-rn-landing.md)

