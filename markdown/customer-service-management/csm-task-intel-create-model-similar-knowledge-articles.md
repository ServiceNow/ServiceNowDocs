---
title: Create a model to predict similar knowledge articles
description: Use the Task Intelligence for CSM to create and train a machine learning model that recommends relevant knowledge articles based on the context of open incidents. The model analyzes existing data to display relevant articles when working on a current case, helping agents find useful information faster. The plugin includes a ready-to-train model for predicting similar articles and also enables you to create custom models tailored to your data.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-10-28"
reading_time_minutes: 2
breadcrumb: [Configure, Task Intelligence for Customer Service, Machine learning solutions, Implement Intelligence, Configure, Customer Service Management]
---

# Create a model to predict similar knowledge articles

Use the Task Intelligence for CSM to create and train a machine learning model that recommends relevant knowledge articles based on the context of open incidents. The model analyzes existing data to display relevant articles when working on a current case, helping agents find useful information faster. The plugin includes a ready-to-train model for predicting similar articles and also enables you to create custom models tailored to your data.

## Before you begin

-   Ensure that the Task Intelligence for Customer Service plugin is installed.
-   Ensure that your instance contains sufficient case and knowledge data \(minimum 10,000 recommended\) for meaningful training.
-   Role required: ml\_admin, ti\_admin

## Set up the prediction model

## Procedure

1.  Navigate to **All** &gt; **Task Intelligence for Customer Service** &gt; **Setup**.

    The Task Intelligence Admin Console displays.

2.  On the Similar Knowledge Articles card, select **Ready to train**.

    The model opens in a guided setup flow. The Define the purpose screen appears.

3.  **Define the purpose:**

    1.  The Prediction table and Training table are pre-selected as **Cases** and **Knowledge**, respectively.

        These values are fixed and can’t be edited.

    2.  Select **Save &amp; Continue**.

        The Train your model screen appears.

4.  **Train your model:**

    1.  The **Model name** and **Prediction table** fields are pre-filled and can’t be edited.

    2.  Apply **Conditions** to filter the training data.

    3.  In the **Prediction fields** field, select Short description that the model uses to identify similarities.

    4.  **Note:** The options selected here are defaults. You can modify the options in the **Prediction fields** and **Training fields** based on your requirements.

        In the **Training fields** field, select Article body and Short description of the Knowledge training table.

    5.  Choose the **language** for training.

    6.  Set the **Update frequency**.

    7.  Review the **Number of records**.

        If needed, select the **Load records** icon to reload.

    8.  Enable **Auto-retrain** to enable retraining the model on a set schedule.

    9.  Select **Launch training**.

    10. Once training starts, select **View current results** to preview sample outputs.

        The Assess and define screen appears.

5.  **Assess and define**:

    1.  Review the **Estimated number of records** used for training.

    2.  In **Similar Knowledge preference**, select one of the following options:

        -   Recommendations – Recommends similar records based on training and prediction fields \(selected by default\).
        -   Monitor only – Runs the model in the background without displaying recommendations. You can analyze the logged data before enabling recommendations.
        -   Turn off predictions – Disables all predictions for this model.
    3.  Select **Save &amp; Continue**.

        The Deploy your model screen appears.

6.  **Deploy your model**:

    1.  Review your setup and training summary and then select **Deploy** to activate the model.

        A confirmation message appears when deployment is complete.

    **Result**

    Once deployed, similar knowledge articles appear in the Recommended Actions section under the Suggested Actions tab when an agent opens a case, helping them resolve cases faster.


