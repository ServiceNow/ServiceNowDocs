---
title: Exploring Task Intelligence for ITSM
description: With Task Intelligence for ITSM, you can set up and deploy machine learning models to predict field-level recommendations and identify similar records for incidents, which will appear as actionable recommendations in the side panel.
locale: en-US
release: zurich
product: Task Intelligence for ITSM
classification: task-intelligence-for-itsm
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Task Intelligence for ITSM, IT Service Management]
---

# Exploring Task Intelligence for ITSM

With Task Intelligence for ITSM, you can set up and deploy machine learning models to predict field-level recommendations and identify similar records for incidents, which will appear as actionable recommendations in the side panel.

## Task Intelligence for ITSM overview

Task Intelligence for ITSM enables you to create, configure, and deploy solution models to predict incident fields information and similar records for incidents.

Task Intelligence for ITSM provides the following types of prediction models:

-   Incident Categorization model - Predicts incident field information to categorize incidents and applications such as Service Operations Workspace. For more information, see [Create an incident prediction model in Task Intelligence for ITSM](create-incident-prediction-model.md).
-   Similar Incidents model: Predicts similar incidents by recognizing similarities between two types of tables by comparing their fields.
-   Similar open Change Requests for Incidents model: Predicts change requests by recognizing the similarities between the incident table and change request table, by comparing their fields.
-   Similar open Problems for Incidents model: Predicts problems by recognizing the similarities between the incident table and problem table, by comparing their fields.

    **Note:** To know more about similarity based models, see [Create a similar records prediction model in Task Intelligence for ITSM](create-a-similar-records-model-in-task-intelligence-for-itsm.md)


The prediction models enable the agents to focus more on incident resolution reducing the time spent filling in field information or searching for similar records. These models can help lower the meantime to resolve \(MTTR\) of tasks. You can also track and monitor how the solution models are performing and modify the parameters of the model accordingly.

Task Intelligence for ITSM enables the agents to do the following:

-   Solve issues faster for better service and experiences
-   Focus  on  meaningful, high-value work
-   Reduce  error  rates  and  drive down costs
-   Improve time to value with intuitive experiences

The Admin Console for Task Intelligence for ITSM provides the admin a no-code experience for deploying Task Intelligence solution models. Using machine-learning models, the application enables you to automate and optimize incident prediction and incident categorizations. The models use statistics to predict future data by training with your past data.

Task Intelligence for ITSM supports Utah patch 5 and later releases.

## Task Intelligence for ITSM workflow

The workflow for Task Intelligence for ITSM includes the following:

1.  Task Intelligence for ITSM: Use this application to set up and configure an incident prediction model to predict and recommend incident fields on the incident form. To configure and use a model, you must do the following:
    1.  Set up an incident prediction model: Set up a model using the default template available with the base system.
    2.  Train your model: Train the model with your data.
    3.  Set your preferences: Set the prediction preferences and behavior for the model.
    4.  Deploy the model: Deploy the model to predict incident field information.
    5.  Monitor and analysis: Monitor how the model is performing and analyze the performance result data.
    6.  Edit your model: Based on the analysis of the performance results, edit your model and deploy it again.
2.  Go to the Advanced Recommended actions for ITSM application configuration to configure where, how, and when the model must be implemented in the Service Operations Workspace application. For more information, see [Recommended Actions for ITSM in Service Operations Workspace](../../service-operations-workspace/concept/recommended-actions-for-itsm-in-service-operations-workspace.md).
3.  Get incident predictions and recommendations in the incident form of Service Operations Workspace.

## Task Intelligence for ITSM benefits

Task Intelligence for ITSM provides the following benefits:

|Benefit|Feature|User|
|-------|-------|----|
|Create and deploy solution-based incident prediction models to predict incidents fields for new IT service incidents. This helps in incident categorization|[Create an incident prediction model in Task Intelligence for ITSM](create-incident-prediction-model.md)|Administrator|
|Create and deploy similarity-based model to predict similar records for IT service incidents which appear as actionable recommendations.|[Create a similar records prediction model in Task Intelligence for ITSM](create-a-similar-records-model-in-task-intelligence-for-itsm.md)|Administrator|
|Export an incident prediction model in Task Intelligence for ITSM to another instance so you can use the model in the other instance without recreating the model from scratch.|[Export an incident prediction model](../task/export-your-model.md)|Administrator|
|Monitor the performance results of the model.|[Monitoring and Analytics for Task Intelligence for ITSM](task-intel-monitor-analystics.md)|Analyst|
|Edit the incident prediction model based on the performance results and deploy again.|[Edit an incident prediction model in Task Intelligence for ITSM](../task/edit-your-model.md)|Administrator|

