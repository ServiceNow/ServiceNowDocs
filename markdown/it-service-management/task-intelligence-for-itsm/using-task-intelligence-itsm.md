---
title: Managing Task Intelligence for ITSM models
description: Use the machine learning capabilities of Task Intelligence for ITSM to predict field level recommendations and similar records on the incidents which appear as actionable recommendations in the side panel.
locale: en-US
release: xanadu
product: Task Intelligence for ITSM
classification: task-intelligence-for-itsm
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Task Intelligence for ITSM, IT Service Management]
---

# Managing Task Intelligence for ITSM models

Use the machine learning capabilities of Task Intelligence for ITSM to predict field level recommendations and similar records on the incidents which appear as actionable recommendations in the side panel.

Managing Task Intelligence for ITSM involves the following tasks.

## Creating a prediction model

You can create and deploy solution-based prediction models to predict incidents fields and actionable real-time recommendations based on the similarities between two types of tables by comparing their fields for IT service incidents.

Task Intelligence for ITSM provides the following types of prediction models:

-   **Incident Categorization model**: This model predicts incidents fields for new IT service incidents.
-   **Similar Incidents model**: The model looks at the prediction fields of a prediction table and the training fields of a training table. It uses the similarities in these fields to predict similar records for incidents.
-   **Similar open Change Requests for Incidents**: The model looks at the incident fields of an incident table and the change request fields of a change request table. It uses the similarities in these fields to predict similar change requests for incidents.
-   **Similar open Problems for Incidents**: The model looks at the incident fields of an incident table and the problem fields of a problem table. It uses the similarities in these fields to predict similar problems for incidents.

Creating a model involves the following steps:

-   Set up a model: Set up a prediction model using a template available in the base system.
-   Define a model: Specify the purpose of the model by selecting the training table and prediction table which will be used for training the model further.
-   Train a model: Train a model to make predictions using your data.
-   Assess your model: Assess the results from the model training, view sample results for the predictions, and select the prediction preferences and behavior for your model.
-   Deploy your model: Deploy your model to predict incident fields on incident forms.

## Editing a prediction model

Edit a prediction model that has already been trained and deployed. Change the model configurations, view the updated training results, and redeploy the model.

## Exporting a prediction model

Export a prediction model in Task Intelligence for ITSM to another instance so you can use the model in the other instance without recreating the model from scratch.

-   **[Create an incident prediction model in Task Intelligence for ITSM](create-incident-prediction-model.md)**  
Create and deploy solution-based incident categorization prediction models to predict incidents fields for new IT service incidents.
-   **[Create a similar records prediction model in Task Intelligence for ITSM](create-a-similar-records-prediction-model-in-task-intelligence-for-itsm.md)**  
Set up a training model to help it recognize similarities between two types of tables by comparing their fields.
-   **[Edit an incident prediction model in Task Intelligence for ITSM](../task/edit-your-model.md)**  
Edit either the Similar Incidents or Incident Categorization model that has already been trained and deployed. Change the model configurations, view the updated training results, and redeploy the model.
-   **[Export an incident prediction model](../task/export-your-model.md)**  
Export either the Similar Incidents or Incident Categorization model model in Task Intelligence for ITSM to another instance so you can use the model in the other instance without recreating the model from scratch.

**Parent Topic:**[Task Intelligence for ITSM](c-itsm-task-intelligence.md)

