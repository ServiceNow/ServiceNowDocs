---
title: Create a similar records prediction model in Task Intelligence for ITSM
description: Set up a training model to help it recognize similarities between two types of tables by comparing their fields.
locale: en-US
release: yokohama
product: Task Intelligence for ITSM
classification: task-intelligence-for-itsm
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Managing Task Intelligence for ITSM models, Task Intelligence for ITSM, IT Service Management]
---

# Create a similar records prediction model in Task Intelligence for ITSM

Set up a training model to help it recognize similarities between two types of tables by comparing their fields.

The model looks at the prediction fields of a prediction table and the training fields of a training table. It uses the similarities in these fields to predict similar records.

For example, the prediction fields might be the short description and description of an incident record, while the training fields could be the short description and title of a knowledge base \(KB\) article. The model compares these fields to find KB articles that are similar to the current incident. This makes it easier for agents to find relevant information and resolve incidents quickly.

If you're an admin, you can decide when you want it to make predictions, what you want it to predict, and what data to use for those predictions.

You can select the following information: 

-   Prediction fields that are used to predict similar records for the model.
-   Training fields that have the similarities to the prediction fields.
-   Conditions used to choose the set of records to train the model.
-   The prediction behavior: **Recommendation**, **Monitor only** \(run in the background\)  or **turn off predictions**.

After customizing your model, you can view the test results and deploy the model.

The model uses previous case records to train. You can see how the model would have predicted similar records for past cases, providing you with an estimate of how the model performs when deployed.

## Base system model 

Task Intelligence for ITSM comes with a base system which has following models based on similarity:

-   Similar Incidents: For predicting the similar incidents for incidents table.
-   Similar open Change Requests for Incident: For predicting the similar change requests for incident table.
-   Similar open Problems for Incident: For predicting the similar problems for incident table.
-   Major Incident Recommendation: For recommending similar active major incidents which the current incident can be linked to, and for recommending that you propose similar incidents as a major incident.

When you install the Task Intelligence for ITSM plugin in your production instance, the model is installed and is trained on your data automatically. This model is auto-deployed. The model starts predicting data in the background and doesn’t impact the Incident form. 

**Note:** As an admin user, you should receive an email within four weeks with a link to your analytics dashboard.

The prediction data is then stored in the prediction tables. You can navigate to **All** &gt; **Task Intelligence for ITSM** &gt; **Monitoring** to view the performance results of this model. Based on these results, you can edit the model to show the predictions in Service Operations Workspace.

To edit and redeploy the base system model, you can navigate to the Setup page. From the model list, select the required similarity model\(For example, Similar Incidents\) and edit the model. For more information on how to edit the model, see [Edit an incident prediction model in Task Intelligence for ITSM](../task/edit-your-model.md).

This model is linked with a base system rule in the Recommended Actions for ITSM configuration. An admin isn't required to go to the Recommended Actions for ITSM application to configure any rules for this model.

To set up a new model using a template, see [Set up similar records prediction model](set-up-similar-records-prediction-model.md).

-   **[Set up similar records prediction model](set-up-similar-records-prediction-model.md)**  
Use Task Intelligence for ITSM to set up similar records prediction model, define the purpose of the model, and train it with your data to make predictions. Access your model's performance results, set the prediction preferences and behavior, and deploy your model. 

**Parent Topic:**[Managing Task Intelligence for ITSM models](using-task-intelligence-itsm.md)

