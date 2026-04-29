---
title: Explore Predictive Intelligence
description: ServiceNow Predictive Intelligence is a platform function that provides a layer of artificial intelligence that empowers features and capabilities across ServiceNow applications to provide better work experiences.
locale: en-US
release: australia
product: Predictive Intelligence
classification: predictive-intelligence
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Predictive Intelligence, Enable AI experiences]
---

# Explore Predictive Intelligence

ServiceNow® Predictive Intelligence is a platform function that provides a layer of artificial intelligence that empowers features and capabilities across ServiceNow® applications to provide better work experiences.

## Overview of Predictive Intelligence

Predictive Intelligence is a powerful set of tools applying artificial intelligence and machine learning to make predictions. You can create and train models in three different frameworks: classification, clustering, and similarity. A trained solution can be invoked by any ServiceNow application through an API.![The benefits of using Predictive Intelligence.](../images/predictive-intelligence-resolves-faster.png)

To learn more about ways to use existing models, see [Using Predictive Intelligence](using-predictive-intelligence.md).

## Predictive Intelligence for on-premise customers

Predictive Intelligence is also available for on-premise customers. If you're interested in deploying this product on-premise, contact your account manager. For on-premise installation and configuration instructions, see the complete instructions for [Machine Learning Engine installation and configuration for self-hosted customers \[KB0782052\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0782052) in the Now Support Self-Hosted Knowledge Base.

**Note:** Only on-premise accounts can access the Now Support Self-Hosted Knowledge Base.

## Terminology

-   **Artificial intelligence**

    Systems designed to do work that needs a level of human intelligence to accomplish.

-   **Machine learning**

    Ability for models to improve over time with more experience.

-   **Models**

    Collections of algorithms, math, and statistics that make predictions and decisions based on input-output data.

-   **Training**

    Adding or changing data that the model is based on to affect future predictions.

-   **Supervised Training**

    Providing input-out pairs so that the model can generate rules that connect the two.

-   **Unsupervised Training**

    Providing raw data so that the model can identify structures in the data set.

-   **Training frequency**

    How often models are retrained to incorporate new data into an existing model.

-   **Word corpus**

    Vocabulary that a model can use to look for textual similarity.


## Predictive model components

A predictive model includes these components, some of which you must provide.

-   **Solution definition**

    A data record you create and configure that specifies these values for training a predictive model.

    -   The records used to train the model. For example, only train on incidents that are resolved or closed within the last six months.
    -   The input fields that the model uses to make predictions. For example, use the incident short description to make a prediction.
    -   The output field whose value the model predicts. For example, set the incident category based on the short description.
    -   The frequency to retrain the model. For example, retrain the model every 30 days.
-   **Solution**

    The solution is the result of a solution definition that you've trained in a ServiceNow datacenter. Predictive Intelligence uses the solution to predict a target field value given one or more input field values. All solutions specify these values.

    -   The solution precision is the aggregate percentage of correct predictions. For example, a precision of 50 means that out of 100 predictions, half of them should have the correct value.
    -   The solution coverage is the aggregate percentage of records that receive a prediction. For example, a coverage of 50 means half of all eligible records actually receive a prediction.
    -   The solution classes are the output field values for which the model can make predictions. Each class is an output field value with a list of possible precision, coverage, and distribution metrics to choose from. For example, the Incident Categorization solution has a class for each category such as software, inquiry, and database.
    -   The class distribution is the percentage of records from the entire table that have this particular output field value. For example, a distribution of 50 for the inquiry class means that half of incidents have the inquiry category.

-   **[Predictive Intelligence frameworks](predictive-intelligence-frameworks.md)**  
Predictive Intelligence provides three different model frameworks in the Australia release: classification, similarity, and clustering. Each framework specializes in different types of predictions.
-   **[ServiceNow apps and features that use Predictive Intelligence](servicenow-apps-features-use-predictive-intelligence.md)**  
Learn about ServiceNow applications and features that leverage Predictive Intelligence. Solutions that you can adapt are available for various business units and industries.

**Parent Topic:**[Predictive Intelligence](predictive-intelligence-landing.md)

