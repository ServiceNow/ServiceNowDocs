---
title: Create a model to predict record fields
description: Create and train a model to predict fields for case and interaction records.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Configure Task Intelligence for Customer Service, Task Intelligence for Customer Service, Machine learning solutions for Customer Service Management, Implement Intelligence, Configuring Customer Service Management, Customer Service Management]
---

# Create a model to predict record fields

Create and train a model to predict fields for case and interaction records.

-   **Before you begin**

    Role required: ml\_admin, admin

-   **About this task**

    The field prediction model is a guide that includes some recommended settings. You can use these settings, such as the recommended input fields, or add your own preferences.

    You can create and train multiple field prediction models for cases, case types, and interactions.


## Set up your model

1.  Navigate to **All** &gt; **Task Intelligence for Customer Service** &gt; **Setup** to access the Task Intelligence Admin Console.
2.  Select **Set up model** on this model: **Predict field choices to reduce handle time**.

    This opens the model and displays the first of five pages. Each page in the model asks you questions and helps you select the information you need to build an effective model.


## Define the purpose

Select the table and the trigger for the model's predictions.

![Model page displaying options for selection like case or interaction data to predict fields as well as the prediction trigger.](../image/tiac-categorization-model-pg1.png)

You can have the model predict case or interaction fields when a new customer email arrives or when an interaction is created. Base your decision on the data that your model should use to make the predictions.

<table id="table_tkc_2yb_d5b"><tbody><tr><td>

Choose the type of table that has the fields you want to predict

</td><td>

Select the table type:-   Cases
-   Interactions

The model uses data from the selected table to make predictions.

</td></tr><tr><td>

Choose the source of data for a prediction

</td><td>

Select the source for the prediction:-   Cases
-   Emails
-   Interactions

</td></tr><tr><td>

Choose the condition that needs to be met

</td><td>

Select the condition for the prediction:-   After create: A prediction is triggered after a case is created.
-   On change: A prediction is triggered when a field is modified.

</td></tr><tr><td>

Choose to include optional training inputs

</td><td>

Enable the check box to include attachments when training the model.Email and record attachments can have information that is useful for routing records correctly.

</td></tr></tbody>
</table>1.  Choose a table type for the model.
2.  Choose the source of data for prediction.
3.  Choose the condition.
4.  If desired, enable the check box to include attachment data.

    Include text from email or record attachments if this information is useful for making predictions. The model can evaluate attachment data, along with email or record text, to make predictions.

5.  Select **Save &amp; continue**.

## Train your model

Select the input fields and output fields so your model can learn patterns. Output fields are the fields that you want the model to predict. Input fields are the fields that the model uses to make predictions.

Selecting this information tells the model what to look for during training.

**Note:** You can use the recommended settings or select different ones.

![Model page used to choose fields and conditions for your model to make predictions.](../image/task-intel-admin-console-pg-2.png)

1.  Provide a name for the model.
2.  Choose the output table and the output fields for the model to predict.
3.  Select conditions to choose a set of records for training.

    The selected conditions determine both how the model is trained and act as a filter for the conditions that a record has to meet in order for predictions to be made.

4.  Select the fields in the training data that the model should use to make the predictions \(input fields\).

    ![Model page displaying different input fields in the training data to make predictions.](../image/task-intel-admin-console-pg-2a.png)

5.  Choose the input fields.
6.  Review the resulting number of cases in the training data based on the selected conditions.

    The model needs a minimum of 500 records for effective training. If this minimum number isn't available, try selecting different conditions.

7.  Select **Launch training**.

    Training can take some time, particularly if you are training the model on a large amount of data. You can request that the system send you an email when the training is done.


## Assess your model

Assess the results from the training and view sample results for the predicted fields. Reviewing the results gives you a preview of how your model will perform after being deployed.

Select the prediction preference for each field. The model provides flexible options to autofill field values, provide recommendations for field values, monitor only, or turn off predictions depending on the sensitivity of those fields.

![Model page displaying the estimated number of predicted field values and a sample selection of the test results.](../image/task-intel-admin-console-pg3-new.png)

1.  Select a **Prediction preference** for each enabled field.

<table id="table_arg_4fd_d5b"><tbody><tr><td>

Autofill

</td><td>

Adds the best predicted value to the field on the record.

</td></tr><tr><td>

Recommendations

</td><td>

Shows the recommended value in a message below the field.

</td></tr><tr><td>

Monitor only

</td><td>

The system makes the field predictions and stores the information in the Predictions History but does not add any information to the case records.

</td></tr><tr><td>

Turn off predictions

</td><td>

Turns off predictions for the field.

</td></tr></tbody>
</table>2.  Select **View sample results** to see sample results for each predicted field.
3.  Select **Save &amp; continue**.

## Deploy your model

Review your choices from the previous pages and information about how the model was trained. Then you can select **Deploy** to deploy the model.

![Model page displaying choices and inputs for review before deploying the model.](../image/task-intel-admin-console-pg5.png)

