---
title: Predictive Intelligence release notes
description: The ServiceNow Predictive Intelligence application enables you to create and train machine learning models to help improve the performance, efficiency, and flexibility of your systems. Predictive Intelligence was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
---

# Predictive Intelligence release notes

The ServiceNow® Predictive Intelligence application enables you to create and train machine learning models to help improve the performance, efficiency, and flexibility of your systems. Predictive Intelligence was enhanced and updated in the Zurich release.

## Predictive Intelligence highlights for the Zurich release

-   Predictive Intelligence errors are logged in a new, dedicated table. The PI - Observability Dashboard leverages this table to provide analytics on prediction errors.
-   New advanced options for Classification models are available, including new parameters and a new algorithm.
-   Validation logic ensures that Predictive Intelligence models have ACLs to access data tables.

See [Predictive Intelligence](https://www.servicenow.com/docs/access?context=predictive-intelligence-landing&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) for more information.

## New in the Zurich release

-   **[Review any errors in predictions using the Observability Dashboard](https://www.servicenow.com/docs/access?context=prediction-errors-observability-dashboard&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Monitor errors using the Observability Dashboard which provides analytics derived from a new table. This table is dedicated to logging any errors that may occur during Predictive Intelligence predictions.

-   **[Leverage new advanced options for classification solutions](https://www.servicenow.com/docs/access?context=configuring-advanced-settings-ml-solutions&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Customize your classification models in Predictive Intelligence with the following advanced options.

    -   [Configure include only top N labels](https://www.servicenow.com/docs/access?context=predictive-intel-only-top-n-labels&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US): Limit the classification model to use only the top most frequent labels. You can choose a number as the limit.
    -   [Minimum records needed for label to include it](https://www.servicenow.com/docs/access?context=predictive-intel-minimum-records-needed-label&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US): Set a threshold for the minimum number of records a label must have in your dataset to be included in model training.
    -   [Remove others label](https://www.servicenow.com/docs/access?context=predictive-intel-remove-others-label&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US): Reduce noise in the model and enhance predictive accuracy by removing records with the label "others" from training data.
    -   [Use LightGBM algo for classification model training](https://www.servicenow.com/docs/access?context=predictive-intel-lightgbm-algo&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US): Enable the LightGBM \(Light Gradient-Boosting Machine\) algorithm for training classification models.
    -   [Config parameters for model config in classification](https://www.servicenow.com/docs/access?context=predictive-intel-config-parameters-classification&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US): Customize training behavior by including a dictionary of parameters in the JSON format.

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

-   **[Document Intelligence](https://www.servicenow.com/docs/access?context=document-intelligence-landing&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Document Intelligence is an artificial intelligence solution that enables any organization to automate and accelerate the process of extracting data from documents.

-   **[Task Intelligence](https://www.servicenow.com/docs/access?context=task-intelligence&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Task Intelligence uses machine learning to train solutions with your data and achieve important outcomes.

-   **[ServiceNow® apps and features that use Predictive Intelligence](https://www.servicenow.com/docs/access?context=servicenow-apps-features-use-predictive-intelligence&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Prebuilt Predictive Intelligence solutions tailored to specific BUs are available in apps across the ServiceNow AI Platform.


**Parent Topic:**[AI Experiences release notes](intelligent-experiences-rn-landing.md)

