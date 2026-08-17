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

See  for more information.

## New in the Yokohama release

-   ****

    Learn which classes contribute most to your model's predictions by optionally adding Model Explainability to Workflow Classification solutions. Model Explainability provides a new tab labeled **Feature Importance** where you can run an analysis of each class's contribution to the overall prediction.

-   **Leverage new advanced options for classification solutions, from Yokohama Patch 4.**
    -   . Limit the classification model to use only the top most frequent labels. You can choose a number as the limit.
    -   . Set a threshold for the minimum number of records a label must have in your dataset to be included in model training.
    -   . Reduce noise in the model and enhance predictive accuracy by removing records with the label "others" from training data.
    -   . Enable the LightGBM \(Light Gradient-Boosting Machine\) algorithm for training classification models.
    -   . Customize training behavior by including a dictionary of parameters in the JSON format.

## Deprecations

With the Yokohama release, ITSM Predictive Intelligence Workbench is deprecated and no longer supported. To obtain the latest experience for this functionality, install the Task Intelligence for ITSM application \(com.snc.itsm\_ml\_task\). For more information, see [ITSM Predictive Intelligence Workbench release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/itsm-predictive-intelligence-workbench-rn.md).

## Activation information

Predictive Intelligence is a ServiceNow AI Platform feature that is available with activation of the Predictive Intelligence plugin \(com.glide.platform\_ml\). For details, see .

## Related ServiceNow applications and features

-   ****

    Document Intelligence is an artificial intelligence solution that enables any organization to automate and accelerate the process of extracting data from documents.

-   ****

    Task Intelligence uses machine learning to train solutions with your data and achieve important outcomes.


**Parent Topic:**[AI Experiences release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/intelligent-experiences-rn-landing.md)

