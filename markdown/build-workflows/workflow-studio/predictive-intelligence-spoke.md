---
title: Machine Learning solutions for Flow Designer
description: With Predictive Intelligence for Flow Designer \(com.snc.ml\_flowdesigner\), you can deploy machine learning solutions in your instance. This spoke provides actions to incorporate Predictive Intelligence model predictions into flows.
locale: en-US
release: yokohama
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2026-01-20"
reading_time_minutes: 2
breadcrumb: [Spokes, Workflow Studio flow integrations, Flows, subflows, and actions reference, Workflow Studio reference, Workflow Studio, Build workflows]
---

# Machine Learning solutions for Flow Designer

With Predictive Intelligence for Flow Designer \(com.snc.ml\_flowdesigner\), you can deploy machine learning solutions in your instance. This spoke provides actions to incorporate Predictive Intelligence model predictions into flows.

## Predictive Intelligence activation

This spoke requires Predictive Intelligence \(com.glide.platform\_ml\). For more information, see [Install Predictive Intelligence](https://www.servicenow.com/docs/access?context=install-predictive-intelligence&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

## Key features

Predictive Intelligence for Flow Designer provides three frameworks that you can use to create machine-learning solutions in your instance. Each framework delivers a different solution type for training the system to predict, recommend, and organize data outcomes.

-   Classification framework
-   Similarity framework
-   Clustering framework

## Spoke requirements

-   A sharedservice.worker user to train solutions.
-   A pre-trained Predictive Intelligence solution.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   Predictive Intelligence \(com.glide.platform\_ml\) plugin
-   Predictive Intelligence Reporting \(com.glide.platform\_ml\_pa\) plugin

**Note:** Some plugins may be licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke actions

Predictive Intelligence for Flow Designer \(com.snc.ml\_flowdesigner\) provides actions to make predictions using existing models without having to write or maintain script. Available actions include:

<table id="table_gdw_w1v_r4b"><thead><tr><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Classification Batch Prediction

</td><td>

Obtain a predicted value from an active classification solution definition using multiple input records.

</td></tr><tr><td>

Classification Prediction

</td><td>

Obtain a predicted value from an active classification solution definition using a single input record.

</td></tr><tr><td>

PI Confidence Check

</td><td>

Compare an output value \(number\) from Predictive intelligence with a number specified by the user. For example: Compare the confidence value of a prediction with a specified value.

</td></tr><tr><td>

Regression Batch Prediction

</td><td>

Obtain a predicted value from an active regression solution definition using multiple input records.**Note:** The regression framework is deprecated in the Yokohama release. You can continue to use existing regression solutions but you can't create new ones.

</td></tr><tr><td>

Regression Prediction

</td><td>

Obtain a predicted value from an active regression solution definition using a single input record.**Note:** The regression framework is deprecated in the Yokohama release. You can continue to use existing regression solutions but you can't create new ones.

</td></tr><tr><td>

Similarity Prediction

</td><td>

Obtain similar records that exist in the table specified by the user in their similarity solution definition.

</td></tr></tbody>
</table>## Spoke user roles

Predictive Intelligence for Flow Designer provides these user roles to control access to data:

|User role|Description|
|---------|-----------|
|ml\_admin|Grants access to all Predictive Intelligence features|

**Parent Topic:**[Spokes](../concept/spokes.md)

**Related topics**  


[Use Predictive Intelligence in Flow Designer with ML actions](https://www.servicenow.com/docs/access?context=use-predictive-intelligence-flow-designer-ml-actions&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)

