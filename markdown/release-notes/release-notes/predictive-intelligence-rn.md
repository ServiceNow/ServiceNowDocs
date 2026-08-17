---
title: Predictive Intelligence release notes
description: The ServiceNow Predictive Intelligence application enables you to create and train machine learning models to help improve the performance, efficiency, and flexibility of your systems. Predictive Intelligence was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2026-07-23"
reading_time_minutes: 2
---

# Predictive Intelligence release notes

The ServiceNow® Predictive Intelligence application enables you to create and train machine learning models to help improve the performance, efficiency, and flexibility of your systems. Predictive Intelligence was enhanced and updated in the Zurich release.

## Predictive Intelligence highlights for the Zurich release

-   Predictive Intelligence errors are logged in a new, dedicated table. The PI - Observability Dashboard leverages this table to provide analytics on prediction errors.
-   New advanced options for Classification models are available, including new parameters and a new algorithm.
-   Validation logic ensures that Predictive Intelligence models have ACLs to access data tables.

See [Predictive Intelligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/predictive-intelligence-landing.md) for more information.

## New in the Zurich release

-   **[Review any errors in predictions using the Observability Dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/prediction-errors-observability-dashboard.md)**

    Monitor errors using the Observability Dashboard which provides analytics derived from a new table. This table is dedicated to logging any errors that may occur during Predictive Intelligence predictions.

-   **[Leverage new advanced options for classification solutions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/configuring-advanced-settings-ml-solutions.md)**

    Customize your classification models in Predictive Intelligence with the following advanced options.

    -   [Configure include only top N labels](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/predictive-intel-only-top-n-labels.md): Limit the classification model to use only the top most frequent labels. You can choose a number as the limit.
    -   [Minimum records needed for label to include it](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/predictive-intel-minimum-records-needed-label.md): Set a threshold for the minimum number of records a label must have in your dataset to be included in model training.
    -   [Remove others label](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/predictive-intel-remove-others-label.md): Reduce noise in the model and enhance predictive accuracy by removing records with the label "others" from training data.
    -   [Use LightGBM algo for classification model training](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/predictive-intel-lightgbm-algo.md): Enable the LightGBM \(Light Gradient-Boosting Machine\) algorithm for training classification models.
    -   [Config parameters for model config in classification](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/predictive-intel-config-parameters-classification.md): Customize training behavior by including a dictionary of parameters in the JSON format.

## UI changes

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


## Changed in this release

-   **Validation logic ensures that Predictive Intelligence can access data tables**

    Reduce errors while training Predictive Intelligence models with the help of new validation logic. This validation checks whether your data tables have ACLs \(Access Control Lists\) granting access to Predictive Intelligence.


## Activation information

Predictive Intelligence is a ServiceNow AI Platform feature that is active by default.

## Accessibility information

-   **Dark theme**

    The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


## Related ServiceNow applications and features

-   **[Now Assist in Document Intelligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/docintel-nowassist-landing.md)**

    With Now Assist in Document Intelligence you can use generative AI to get key information from digital documents into your automation workflows.

-   **[Task Intelligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/task-intelligence.md)**

    Task Intelligence uses machine learning to train solutions with your data and achieve important outcomes.

-   **[ServiceNow® apps and features that use Predictive Intelligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/servicenow-apps-features-use-predictive-intelligence.md)**

    Prebuilt Predictive Intelligence solutions tailored to specific BUs are available in apps across the ServiceNow AI Platform.


**Parent Topic:**[AI Experiences release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/intelligent-experiences-rn-landing.md)

