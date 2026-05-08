---
title: Set up your incident prediction model
description: Use Task Intelligence for ITSM to set up your incident prediction model and train it with your data to make predictions. Access your model's performance results, set the prediction preferences and behavior, and deploy your model.Train your incident prediction model with data to predict the incident fields.Assess the results from the model training and view sample results for the predicted fields. Reviewing the results gives you a preview of how your model will perform after being deployed. Based on the sample results, select the prediction preference and behavior for each field.Deploy the incident prediction model to predict the incident field information.
locale: en-US
release: australia
product: Task Intelligence for ITSM
classification: task-intelligence-for-itsm
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Create an incident prediction model, Manage, Task Intelligence for ITSM, IT Service Management]
---

# Set up your incident prediction model

Use Task Intelligence for ITSM to set up your incident prediction model and train it with your data to make predictions. Access your model's performance results, set the prediction preferences and behavior, and deploy your model.

## Before you begin

Role required: sn\_ti\_admin.tia\_admin or sn\_itsm\_ml\_task.ti\_admin

## Procedure

1.  Navigate to **All** &gt; **Task Intelligence for ITSM** &gt; **Setup** to access the Task Intelligence Admin Console.

2.  On the **Predict incident field choices to reduce handle time** card, select **Set up model**.

    ![Categorization_template](../image/ti_Categorization_model_template.png)

    This action opens the model and displays the introductory pages. Each page in the model asks you questions and helps you select the information needed to build an effective model.


**Parent Topic:**[Create an incident prediction model in Task Intelligence for ITSM](../concept/create-incident-prediction-model.md)

## Train your model

Train your incident prediction model with data to predict the incident fields.

### Before you begin

You can set up a task intelligence model or use the base system template that is shipped with Task Intelligence for ITSM. For more information on setting up a new model, see [Set up your incident prediction model](set-up-model.md#).

Role required: sn\_ti\_admin.tia\_admin or admin

### About this task

When you train a machine learning model, the model learns patterns from past data to make predictions about new data. Models are trained using large amounts of data so that they can learn patterns. A large data set makes the learned patterns statistically significant. As you answer questions about your information systems, business process, and service operations, the system actively learns from your responses.

You can select the table and fields that you want to predict, such as the Output table and Output fields. Also, you can select the tables and fields that you want the model to use to predict the incident information, such as the Input table and Input fields.

Select this information to tell the model what to look for during training.

**Note:** You can either use the recommended settings or customize the settings to fit your needs.

### Procedure

1.  Enter a name for the model.

2.  Select the **Output table** you want the model to predict.

3.  Select **Conditions** to choose a set of records to use for training.

    The selected conditions determine how the model is trained. These conditions provide the requirements that a record must meet to make the predictions.

4.  Select the **Output fields** you want the model to predict.

    ![UI of the output table with its conditions and the output fields.](../image/ti-train-output-fields.png)

5.  Select the **Input table** in the training data that you want the model to use to make predictions.

6.  Select the **Input fields** that you want the model to use to make predictions.

    ![UI of the input table and input fields section.](../image/ti-train-input-fields.png)

7.  Review the resulting **Number of records** in the training data based on the selected conditions.

    The records that are counted include the number of fields, parameters, and data that the model uses to train. Based on the provided information and the set conditions, the number or records gets updated automatically. The model needs a minimum of 10,000 records for effective training. If this minimum number hasn't been reached, try selecting different conditions. You can also click the refresh icon \(![get latest matrix refresh](../../service-operations-workspace/image/get-latest-matrix.png)\) to refresh the number.

    ![UI of the "Review the resulting number of records" section.](../image/ti_train_review_resulting_records.png)

8.  Select **Launch training**.


### Result

If you’re training the model on a large amount of data, training can take some time. You can request that the system sends you an email when the training is done.

## Assess your model

Assess the results from the model training and view sample results for the predicted fields. Reviewing the results gives you a preview of how your model will perform after being deployed. Based on the sample results, select the prediction preference and behavior for each field.

### Before you begin

You must train your model with various data. For more information on how to train your model, see [Train your model](set-up-model.md#).

Role required: sn\_ti\_admin.tia\_admin or admin

### About this task

The model has flexible options. Based on the sensitivity and requirements of each incident field on the Incident form, you can do the following actions:

-   Auto-fill the predicted value in the incident field.
-   Recommend the predicted value in the incident field.
-   Monitor and run the prediction model for the incident field in the background only.
-   Turn off the predictions for the incident field.

### Procedure

1.  View the number value in the **Estimated number of autofilled fields** section.

    The number helps you predict how your model performs when deployed.

2.  Select **View sample results** to see the sample results for each predicted field.

3.  Select the **Comparison** button to see the details for a selected result.

4.  Choose one of the following options from the **Prediction preference** drop-down list for each field.

<table id="choicetable_lzr_gyr_zyb"><thead><tr><th align="left" id="d286683e417">

Options

</th><th align="left" id="d286683e420">

Description

</th></tr></thead><tbody><tr><td id="d286683e426">

**Autofill**

</td><td>

Adds the best predicted value to the field on the Incident form.

</td></tr><tr><td id="d286683e435">

**Recommendations**

</td><td>

Shows the top recommended values for a field. Agents can choose to accept or reject the recommendation. You can configure the number of recommended values using Advanced Recommended actions for ITSM. For more information, see [Recommended Actions for ITSM in Service Operations Workspace](../../service-operations-workspace/concept/recommended-actions-for-itsm-in-service-operations-workspace.md).

</td></tr><tr><td id="d286683e460">

**Turn off predictions**

</td><td>

Stops the model from performing any predictions.

</td></tr><tr><td id="d286683e469">

**Monitor only**

</td><td>

Monitors and runs the model in the background only without making any predictions on the incident form.

</td></tr></tbody>
</table>    ![Access the model page](../image/ti_access_set_preferences_page.png)

5.  Select **Save &amp; continue**.


## Deploy your model

Deploy the incident prediction model to predict the incident field information.

### Before you begin

You must access the model and set the preferences for your model. For more information on setting model preferences, see [Assess your model](set-up-model.md#).

Role required: sn\_ti\_admin.tia\_admin or admin

### Procedure

1.  Review your choices from the previous pages and information about how the model was trained.

    ![UI of the page to review the model's information. It shows "How this model was trained" and "What your model will do."](../image/ti-deploy-review-model.png)

2.  Select **Deploy** to deploy the model.


### Result

A pop-up appears confirming that your model was deployed.

![Model deployed confirmation pop-up.](../image/ti-ra-popup.png)

### What to do next

Select **Configure Recommended Actions** to configure the implementation of the incident prediction model in the incident fields. For more information, see [Recommended Actions for ITSM in Service Operations Workspace](../../service-operations-workspace/concept/recommended-actions-for-itsm-in-service-operations-workspace.md).

