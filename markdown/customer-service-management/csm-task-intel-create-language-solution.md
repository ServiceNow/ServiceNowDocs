---
title: Create a model to detect case language
description: Edit and test the pre-trained model to detect the language used to create customer service cases.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure, Task Intelligence for Customer Service, Machine learning solutions, Implement Intelligence, Configure, Customer Service Management]
---

# Create a model to detect case language

Edit and test the pre-trained model to detect the language used to create customer service cases.

-   **Before you begin**

    Role required: ti\_admin

-   **About this task**

    The language detection model is a pre-trained model. You select a set of records to test the model and then view the results before deploying.

    Using the language detection model automatically enables the Task Intelligence Case Language Detection flow and the **sn\_csm\_ml\_task.case.language.mlpredictor.enabled** property.

-   **Prerequisite**

    -   Activate the I18N: Internationalization plugin
    -   Enable the ServiceNow translator.
    For more information, see [Configure language detection](case-language-detection-configure.md).


## Set up your model

1.  Navigate to **All** &gt; **Task Intelligence for Customer Service** &gt; **Setup** to access the Task Intelligence Admin Console.
2.  Select **Edit model** on this model: **Predict case language to improve assignments**.

    This opens the model and displays the first of four pages. Each page in the model asks you questions and helps you select the information you need to build an effective model.


## Test your model

Choose the cases to use to test the model.

![Language detection model for filtering past cases for language prediction with multiple conditions fields.](../image/task-intel-language-detection-pg1.png)

Selecting this information tells the model which records to use for testing. When the model is deployed, it predicts the language on all records in the table that match the selected conditions.

1.  Use conditions to choose a set of records for testing.
2.  Select **Launch testing**.

## Assess your model

Assess the results from the testing and view sample results for past cases.

![Language detection model providing a sample selection of test results with language predictions based on the past hundred cases.](../image/task-intel-language-detection-pg2.png)

Reviewing the results gives you a preview of how your model will perform after being deployed.

1.  Select **View all test results** to see a list of results.
2.  Select **Save &amp; continue**.

## Set your preferences

Tell the model how you want to use the language predictions.

![Options menu enabling the user to use language predictions for new cases or monitor predictions running in the background.](../image/task-intel-language-detection-pg3.png)

1.  Use predictions in new cases.
    1.  Add the predicted language in the **Language** field in cases.
    2.  Use the language prediction as a skill to assist with case routing \(add the language skill to the Task Skills table for the case record\).
2.  If desired, you can run the model in the background only.

    With this option, the system makes the language predictions and stores the information in the Predictions History but does not add any information to the case records.

3.  Select **Save &amp; continue**.

## Deploy your model

Review your selections from the previous pages. Then you can select **Deploy** to deploy the model.

![Details menu with information about model testing, functions, and predictions.](../image/task-intel-language-detection-pg4.png)

