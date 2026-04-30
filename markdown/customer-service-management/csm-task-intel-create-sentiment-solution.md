---
title: Create a model to predict case sentiment
description: Edit and test the pre-trained sentiment model to predict sentiment for customer service cases.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configure Task Intelligence for Customer Service, Task Intelligence for Customer Service, Machine learning solutions for Customer Service Management, Implement Intelligence, Configuring Customer Service Management, Customer Service Management]
---

# Create a model to predict case sentiment

Edit and test the pre-trained sentiment model to predict sentiment for customer service cases.

-   **Before you begin**

    Role required: ml\_admin, admin

-   **About this task**

    The case sentiment model is pre-trained with a large data set to learn communication patterns. You select a set of records to test the model and then view the results before deploying.


## Set up your model

1.  Navigate to **All** &gt; **Task Intelligence for Customer Service** &gt; **Setup** to access the Task Intelligence Admin Console.
2.  Select **Edit model** on this model: **Predict case sentiment to improve CSAT**.

    This opens the model and displays the first of five pages. Each page in the model asks you questions and helps you select the information you need to build an effective model.


## Define the purpose

Tell the model when you want it to make predictions.

![Case sentiment model screen with options to select the case type for sentiment prediction.](../image/task-intel-sentiment-model-pg1.png)

The sentiment model is pre-trained with a large data set to understand communication patterns. This data comes from customer emails and from case descriptions and comments.

1.  Select the table that contains the records to be tested.

    Select **All cases** to test records in the Case table or select a case type table.

2.  Select **Save &amp; continue**.

## Test your model

Choose the cases to use to test the model.

![Case sentiment model with multiple condition fields that filter past cases for sentiment prediction.](../image/task-intel-sentiment-model-pg2.png)

Selecting this information tells the model what type of records to use for testing. When the model is deployed, it predicts sentiment on all records in the table that match the selected conditions.

1.  Use conditions to choose a set of records for testing.
2.  Select **Launch testing**.

## Assess your model

Assess the results from the testing and view sample results for past cases.

![Case sentiment model providing a sample selection of test results with sentiment predictions based on past hundred cases.](../image/task-intel-sentiment-model-pg3.png)

Reviewing the results gives you a preview of how your model will perform after being deployed.

1.  Select **View all test results** to see a list of results.
2.  Select **Save &amp; continue**.

## Set your preferences

Tell the model how you want to use the sentiment predictions.

![Options to show predictions for new cases or to monitor predictions running in the background.](../image/task-intel-sentiment-model-pg4.png)

1.  Display predictions in the **Current sentiment** and **Sentiment over time** fields.
2.  If desired, you can run the model in the background only.

    With this option, the system makes the predictions and stores the information in the Predictions History but does not add any information to the case records.

3.  Select **Save &amp; continue**.

## Deploy your model

Review your choices from the previous pages. Then you can select **Deploy** to deploy the model.

![Information about the model testing and cases that the model will work on before deploying the case sentiment model.](../image/task-intel-sentiment-model-pg5.png)

