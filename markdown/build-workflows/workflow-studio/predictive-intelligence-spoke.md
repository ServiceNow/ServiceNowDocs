---
title: Machine Learning solutions for Flow Designer
description: Provides actions to make predictions from trained Predictive Intelligence solutions. Also reuse this short description in the release notes.
locale: en-US
release: xanadu
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Spokes, Workflow Studio flow integrations, Flows, subflows, and actions reference, Workflow Studio reference, Workflow Studio, Build workflows]
---

# Machine Learning solutions for Flow Designer

Provides actions to make predictions from trained Predictive Intelligence solutions.

## Predictive Intelligence subscription

This spoke requires a subscription to Predictive Intelligence. For more information, see [Install Predictive Intelligence](https://www.servicenow.com/docs/access?context=install-predictive-intelligence&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).

## Key features

Predictive Intelligence for Flow Designer provides four frameworks that you can use to create machine-learning solutions in your instance. Each framework delivers a different solution type for training the system to predict, recommend, and organize data outcomes.

-   Classification framework
-   Similarity framework
-   Clustering framework
-   Regression framework

## Spoke requirements

-   A sharedservice.worker user to train solutions
-   A pre-trained solution for your Predictive Intelligence framework

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   Predictive Intelligence \(com.glide.platform\_ml\) plugin
-   Predictive Intelligence Reporting \(com.glide.platform\_ml\_pa\) plugin

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke actions

Predictive Intelligence for Flow Designer provides actions to make predictions using existing models without having to write or maintain script. Available actions include:

|Action|Description|
|------|-----------|
|Classification Batch Prediction|Obtain a predicted value from an active classification solution definition using multiple input records.|
|Classification Prediction|Obtain a predicted value from an active classification solution definition using a single input record.|
|PI Confidence Check|Compare an output value \(number\) from Predictive intelligence with a number specified by the user. For example: Compare the confidence value of a prediction with a specified value.|
|Regression Batch Prediction|Obtain a predicted value from an active regression solution definition using multiple input records.|
|Regression Prediction|Obtain a predicted value from an active regression solution definition using a single input record.|
|Similarity Prediction|Obtain similar records that exist in the table specified by the user in their similarity solution definition.|

## Spoke user roles

Predictive Intelligence for Flow Designer provides these user roles to control access to data:

|User role|Description|
|---------|-----------|
|ml\_admin|Grants access to all Predictive Intelligence features|

**Parent Topic:**[Spokes](../concept/spokes.md)

**Related topics**  


[Use Predictive Intelligence in Flow Designer with ML actions](https://www.servicenow.com/docs/access?context=use-predictive-intelligence-flow-designer-ml-actions&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)

