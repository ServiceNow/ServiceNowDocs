---
title: Set up similar records prediction model
description: Use Task Intelligence for ITSM to set up similar records prediction model, define the purpose of the model, and train it with your data to make predictions. Access your model's performance results, set the prediction preferences and behavior, and deploy your model. 
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/task-intelligence-for-itsm/set-up-similar-records-prediction-model.html
release: australia
product: Task Intelligence for ITSM
classification: task-intelligence-for-itsm
topic_type: task
last_updated: "2026-08-19"
reading_time_minutes: 2
keywords: [similar records prediction model, Task Intelligence for ITSM, similar incidents, similar change requests, similar problems, major incident recommendation, machine learning model, prediction model setup, model training, model deployment, Service Operations Workspace, recommended actions, similarity-based models]
audience: administrator
breadcrumb: [Create a similar records prediction model, Manage, Task Intelligence for ITSM, IT Service Management]
---

# Set up similar records prediction model

Use Task Intelligence for ITSM to set up similar records prediction model, define the purpose of the model, and train it with your data to make predictions. Access your model's performance results, set the prediction preferences and behavior, and deploy your model. 

## Before you begin

Role required: sn\_ti\_admin.tia\_admin or sn\_itsm\_ml\_task.ti\_admin

## About this task

You can configure any of the following similarity-based models:

-   Similar Incidents: For predicting the similar incidents for incidents table.
-   Similar open Change Requests for Incident: For predicting the similar change requests for incident table.
-   Similar open Problems for Incident: For predicting the similar problems for incident table.
-   Major Incident Recommendation: For recommending similar active major incidents which the current incident can be linked to, and for recommending that you propose similar incidents as a major incident.

## Procedure

1.  Navigate to **All** &gt; **Task Intelligence for ITSM** &gt; **Setup** to access the Task Intelligence Admin Console.

2.  On the **Surface similar records to reduce resolution time** card, select **Set up model**.

    \[Omitted image "TI\_Similarity\_model\_template.png"\] Alt text: Similarity\_model\_Template

    This action opens the model and displays the introductory pages. Each page in the model asks you questions and helps you select the information needed to build an effective model.


## What to do next

After you open the model, complete the wizard to define the purpose, train, assess, and deploy the model. For more information, see [Define the purpose](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/task-intelligence-for-itsm/define-the-purpose.md).

To make the model's predictions appear to agents in Service Operations Workspace:

1.  Set a recommended action for the context \(for example, Incident\) and map the model into the Resource generator's **Model** field.
2.  Confirm that the rule for the recommendation is active in the Recommended Actions for ITSM configuration.

To test the model before agents rely on it, view sample results during the assess step or set the prediction behavior to **Monitor only** to run predictions in the background. For more information, see [Assess the similarity model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/task-intelligence-for-itsm/assess-the-similarity-model.md).

-   **[Define the purpose](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/task-intelligence-for-itsm/define-the-purpose.md)**  
Specify the purpose of the similar records model. You can select the prediction table for which predictions will be generated. Then, select the training table \(Incidents, Problems, or Change Requests\) which will appear as predictions based on similarities between their selected fields.
-   **[Train the similarity model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/task-intelligence-for-itsm/train-the-similarity-model.md)**  
Train your similar record models with training data to predict the similar records by recognizing similarities between fields of Incident table and training tables.
-   **[Assess the similarity model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/task-intelligence-for-itsm/assess-the-similarity-model.md)**  
Assess the results from the model training and view sample results to see the similar records predicted for incidents. Reviewing the results gives you a preview of how your model will perform after being deployed. Based on the sample results, select the prediction preference.
-   **[Deploy the similarity model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/task-intelligence-for-itsm/deploy-the-similarity-model.md)**  
Deploy the Similar incidents model to predict the similar records for the incidents. 

**Parent Topic:**[Create a similar records prediction model in Task Intelligence for ITSM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/task-intelligence-for-itsm/create-a-similar-records-model-in-task-intelligence-for-itsm.md)

