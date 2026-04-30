---
title: Predictive Intelligence release notes
description: The ServiceNow Predictive Intelligence application enables you to create and train machine learning models to help improve performance, efficiency, and flexibility to your systems. Predictive Intelligence was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-07-29"
reading_time_minutes: 2
---

# Predictive Intelligence release notes

The ServiceNow® Predictive Intelligence application enables you to create and train machine learning models to help improve performance, efficiency, and flexibility to your systems. Predictive Intelligence was enhanced and updated in the Yokohama release.

## Predictive Intelligence highlights for the Yokohama release

-   Learn which classes contribute the most to your model's predictions by adding Model Explainability to Workflow Classification solutions.
-   ITSM Predictive Intelligence Workbench is deprecated in the Yokohama release.
-   New advanced options for classification solutions are available from Yokohama Patch 4.

See [Predictive Intelligence](https://www.servicenow.com/docs/access?context=predictive-intelligence-landing&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) for more information.

## New in the Yokohama release

-   **[Model Explainability](https://www.servicenow.com/docs/access?context=predictive-intel-explainability&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Learn which classes contribute most to your model's predictions by optionally adding Model Explainability to Workflow Classification solutions. Model Explainability provides a new tab labeled **Feature Importance** where you can run an analysis of each class's contribution to the overall prediction.

-   **[Leverage new advanced options for classification solutions](https://www.servicenow.com/docs/access?context=configuring-advanced-settings-ml-solutions&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US), from Yokohama Patch 4.**
    -   [Configure include only top N labels](https://www.servicenow.com/docs/access?context=predictive-intel-only-top-n-labels&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US). Limit the classification model to use only the top most frequent labels. You can choose a number as the limit.
    -   [Minimum records needed for label to include it](https://www.servicenow.com/docs/access?context=predictive-intel-minimum-records-needed-label&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US). Set a threshold for the minimum number of records a label must have in your dataset to be included in model training.
    -   [Remove others label](https://www.servicenow.com/docs/access?context=predictive-intel-remove-others-label&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US). Reduce noise in the model and enhance predictive accuracy by removing records with the label "others" from training data.
    -   [Use LightGBM algo for classification model training](https://www.servicenow.com/docs/access?context=predictive-intel-lightgbm-algo&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US). Enable the LightGBM \(Light Gradient-Boosting Machine\) algorithm for training classification models.
    -   [Config parameters for model config in classification](https://www.servicenow.com/docs/access?context=predictive-intel-config-parameters-classification&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US). Customize training behavior by including a dictionary of parameters in the JSON format.

## Deprecations

With the Yokohama release, ITSM Predictive Intelligence Workbench is deprecated and no longer supported. To obtain the latest experience for this functionality, install the Task Intelligence for ITSM application \(com.snc.itsm\_ml\_task\). For more information, see [ITSM Predictive Intelligence Workbench release notes](../it-service-management/itsm-predictive-intelligence-workbench-rn.md).

## Activation information

Predictive Intelligence is a ServiceNow AI Platform feature that is available with activation of the Predictive Intelligence plugin \(com.glide.platform\_ml\). For details, see [Install Predictive Intelligence](https://www.servicenow.com/docs/access?context=install-predictive-intelligence&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

## Related ServiceNow applications and features

-   **[Document Intelligence](https://www.servicenow.com/docs/access?context=document-intelligence-landing&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Document Intelligence is an artificial intelligence solution that enables any organization to automate and accelerate the process of extracting data from documents.

-   **[Task Intelligence](https://www.servicenow.com/docs/access?context=task-intelligence&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Task Intelligence uses machine learning to train solutions with your data and achieve important outcomes.


**Parent Topic:**[AI Experiences release notes](intelligent-experiences-rn-landing.md)

