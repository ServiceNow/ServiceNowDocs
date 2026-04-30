---
title: Create an incident prediction model in Task Intelligence for ITSM
description: Create and deploy solution-based incident categorization prediction models to predict incidents fields for new IT service incidents.
locale: en-US
release: zurich
product: Task Intelligence for ITSM
classification: task-intelligence-for-itsm
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Manage, Task Intelligence for ITSM, IT Service Management]
---

# Create an incident prediction model in Task Intelligence for ITSM

Create and deploy solution-based incident categorization prediction models to predict incidents fields for new IT service incidents.

With an incident field prediction model, you can choose what the model uses to predict information. If you're an admin, you can decide when you want it to make predictions, what you want it to predict, and what data to use for those predictions. You can select the following information:

-   Output fields: The fields that the model predicts
-   Input fields: The fields used to predict the output fields
-   Conditions that choose the set of records to train the model
-   The prediction behavior: auto-fill, recommend, or Monitor only \(run in the background\) or turn off predictions.

After customizing your model, you can view the test results and deploy the model.

The model uses previous case records to train. You can see how the model would have predicted fields for past cases, providing you with an estimate of how the model performs when deployed.

## Base system model

Task Intelligence for ITSM comes with a base system which has following models based on similarity:

-   Similar Incidents: For predicting the similar incidents for incidents table.
-   Similar open Change Requests for Incident: For predicting the similar change requests for incident table.
-   Similar open Problems for Incident: For predicting the similar problems for incident table.
-   Major Incident Recommendation: For recommending similar active major incidents which the current incident can be linked to, and for recommending that you propose similar incidents as a major incident.

When you install the Task Intelligence for ITSM plugin in your production instance, the model is installed and is trained on your data automatically. This model is auto-deployed. The model starts predicting data in the background and doesn’t impact the Incident form.

The prediction data is then stored in the prediction tables. You can navigate to **All** &gt; **Task Intelligence for ITSM** &gt; **Monitoring** to view the performance results of this model. Based on these results, you can edit the model to show the predictions in Service Operations Workspace. You can configure the model to use the predictions to either auto-fill or give recommendations for the output fields on an incident form.

To edit and redeploy the base system model, you can navigate to the Setup page. From the model list, select the required similarity model and edit the model. For more information on how to edit the model, see [Edit an incident prediction model in Task Intelligence for ITSM](../task/edit-your-model.md).

This model is linked with a base system rule in the Recommended Actions for ITSM configuration. An admin isn't required to go to the Recommended Actions for ITSM application to configure any rules for this model.

To set up a new model using a template, see [Set up your incident prediction model](../task/set-up-model.md#).

-   **[Set up your incident prediction model](../task/set-up-model.md#)**  
Use Task Intelligence for ITSM to set up your incident prediction model and train it with your data to make predictions. Access your model's performance results, set the prediction preferences and behavior, and deploy your model.

**Parent Topic:**[Managing Task Intelligence for ITSM models](using-task-intelligence-itsm.md)

