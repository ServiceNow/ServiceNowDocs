---
title: Create a custom similar case model
description: Set up a training model to help it recognize similarities between two types of tables by comparing their fields.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Configure, Task Intelligence for Customer Service, Machine learning solutions, Implement Intelligence, Configure, Customer Service Management]
---

# Create a custom similar case model

Set up a training model to help it recognize similarities between two types of tables by comparing their fields.

The model looks at the prediction fields of a prediction table and the training fields of a training table. It uses the similarities in these fields to predict similar records.

-   **Before you begin**

    Role required: ml\_admin, ti\_admin

-   **About this task**

    The case similarity model is pre-trained with a large data set to learn communication patterns. You select a set of records to test the model and then view the results before deploying.


## Set up similar cases prediction model

Use Task Intelligence for CSM to set up similar case prediction model and train it with your data to make predictions. Access your model's performance results, set the prediction preferences and behavior, and deploy your model.

1.  Navigate to **All** &gt; **Task Intelligence for Customer Service** &gt; **Setup** to access the Task Intelligence Admin Console.
2.  On the **Suggest similar case to reduce resolution time** card, select **Set up model**.

This action opens the model and displays the introductory pages. Each page in the model asks you questions and helps you select the information needed to build an effective model.

## Train the similarity model

Train your similar case model with training data to predict the similar records by recognizing similarities between fields of Case table and training tables. When you train a machine learning model, the model looks at the prediction fields of a prediction table and the training fields of a training table. It uses the similarities in these fields to predict similar records.

You can select the table and fields that you want to predict, such as the Prediction table and Predictions fields. Also, you can select the tables and fields that you want the model to use to predict the similar records, such as the Training table and Training fields. Select this information to tell the model what to look for during training.

**Note:** You can either use the recommended settings or customize the settings to fit your needs.

1.  Enter a name for the model.
2.  Select the **Prediction table** you want the model to predict.
3.  Select **Conditions** to choose a set of records to use for training.

    **Note:** These conditions provide the requirements that a record must meet to make the predictions. However, this functionality is currently not supported.

4.  Select the **Prediction fields** which will be used to predict similar records.
5.  Select the **Training table** in the training data that you want the model to use to make predictions.
6.  Select **Conditions** to choose a set of records to use for training.
7.  Select the **Training fields** that you want the model to use to make predictions.
8.  Select the **Language** in which training takes place.
9.  Select the **Update Frequency** to decide how frequently the training should occur.
10. Review the resulting **Number of records** in the training data based on the selected conditions.

    The records that are counted include the number of fields, parameters, and data that the model uses to train. Based on the provided information and the set conditions, the number or records gets updated automatically. The model needs a minimum of 10,000 records for effective training. If this minimum number hasn't been reached, try selecting different conditions. You can also click the refresh icon to refresh the number.

11. Select to retain a model manually or set it to auto retrain.
12. Select **Launch training**.

## Assess the similarity model

Assess the results from the model training and view sample results to see the similar records predicted for cases. Reviewing the results gives you a preview of how your model will perform after being deployed. Based on the sample results, select the prediction preference. The model has flexible options. Based on the sensitivity and requirements of each case record, you can do the following actions:

-   Recommend similar records for the cases.
-   Monitor and run the prediction model for the cases in the background only. Admin can track the predictions made by model by going to **All** &gt; **Task Intelligence for Customer Service** &gt; **History**.
-   Turn off the predictions for the cases.

Steps in Assess the similarity model:

1.  View the number value in the **Estimated number of records used for training** section.
2.  Select **View sample results** to see the similar records predicted for each case.
3.  Choose one of the following options from the **Prediction preference** drop-down list for each field.

    |Options|Description|
    |-------|-----------|
    |Recommendations|Shows the top recommendations based on the similarity patterns. Agents can choose to accept or reject the recommendation. You can configure the number of recommended values using Advanced Recommended actions for CSM. For more information, see [Configuring the Recommended Actions application](configure-recommended-actions.md).|
    |Turn off predictions|Stops the model from performing any predictions.|
    |Monitor only|Monitors and runs the model in the background only without making any predictions on the case form.|

4.  Select **Save &amp; continue**.

## Deploy the similarity model

Deploy the Similar cases model to predict the similar records for the cases.

1.  Review your choices from the previous pages and information about how the model was trained.
2.  Select **Deploy** to deploy the model.

A pop-up appears confirming that your model was deployed.

