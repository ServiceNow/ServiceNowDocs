---
title: Predictive Intelligence release notes
description: The ServiceNow Predictive Intelligence application enables you to create and train machine learning models to help improve performance, efficiency, and flexibility to your systems. Predictive Intelligence was enhanced and updated in the Yokohama release.The ServiceNow Predictive Intelligence application enables you to create and train machine learning models to help improve performance, efficiency, and flexibility to your systems. Predictive Intelligence was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: topic
last_updated: "2025-07-29"
reading_time_minutes: 2
---

# Predictive Intelligence release notes

The ServiceNow® Predictive Intelligence application enables you to create and train machine learning models to help improve performance, efficiency, and flexibility to your systems. Predictive Intelligence was enhanced and updated in the Yokohama release.

## About Predictive Intelligence

-   Learn which classes contribute the most to your model's predictions by adding Model Explainability to Workflow Classification solutions.
-   ITSM Predictive Intelligence Workbench is deprecated in the Yokohama release.
-   New advanced options for classification solutions are available from Yokohama Patch 4.

See [Predictive Intelligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/predictive-intelligence-landing.md) for more information.

## Activation and other requirements

-   **Activation information**

    Predictive Intelligence is a ServiceNow AI Platform feature that is available with activation of the Predictive Intelligence plugin \(com.glide.platform\_ml\). For details, see [Install Predictive Intelligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/install-predictive-intelligence.md).


**Parent Topic:**[AI Experiences release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/intelligent-experiences-rn-landing.md)

## Yokohama

The ServiceNow® Predictive Intelligence application enables you to create and train machine learning models to help improve performance, efficiency, and flexibility to your systems. Predictive Intelligence was enhanced and updated in the Yokohama release.

### What's new

-   **[Model Explainability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/predictive-intel-explainability.md)**

    Learn which classes contribute most to your model's predictions by optionally adding Model Explainability to Workflow Classification solutions. Model Explainability provides a new tab labeled **Feature Importance** where you can run an analysis of each class's contribution to the overall prediction.

-   **[Leverage new advanced options for classification solutions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/configuring-advanced-settings-ml-solutions.md), from Yokohama Patch 4.**
    -   [Configure include only top N labels](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/predictive-intel-only-top-n-labels.md). Limit the classification model to use only the top most frequent labels. You can choose a number as the limit.
    -   [Minimum records needed for label to include it](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/predictive-intel-minimum-records-needed-label.md). Set a threshold for the minimum number of records a label must have in your dataset to be included in model training.
    -   [Remove others label](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/predictive-intel-remove-others-label.md). Reduce noise in the model and enhance predictive accuracy by removing records with the label "others" from training data.
    -   [Use LightGBM algo for classification model training](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/predictive-intel-lightgbm-algo.md). Enable the LightGBM \(Light Gradient-Boosting Machine\) algorithm for training classification models.
    -   [Config parameters for model config in classification](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/predictive-intel-config-parameters-classification.md). Customize training behavior by including a dictionary of parameters in the JSON format.

### What's deprecated or removed

With the Yokohama release, ITSM Predictive Intelligence Workbench is deprecated and no longer supported. To obtain the latest experience for this functionality, install the Task Intelligence for ITSM application \(com.snc.itsm\_ml\_task\). For more information, see [ITSM Predictive Intelligence Workbench release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/itsm-predictive-intelligence-workbench-rn.md).

