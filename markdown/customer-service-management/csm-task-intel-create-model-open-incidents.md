---
title: Create a model to predict similar open incidents
description: Use the Task Intelligence for CSM to create and train a machine learning model that identifies similar open incidents. The model analyzes similar open incidents data to suggest relevant incident records when working on a current open incident, helping agents resolve issues faster. The plugin includes a ready-to-train model for predicting similar cases and also lets you create custom models tailored to your specific use cases.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Task Intelligence for Customer Service, Machine learning solutions, Implement Intelligence, Configure, Customer Service Management]
---

# Create a model to predict similar open incidents

Use the Task Intelligence for CSM to create and train a machine learning model that identifies similar open incidents. The model analyzes similar open incidents data to suggest relevant incident records when working on a current open incident, helping agents resolve issues faster. The plugin includes a ready-to-train model for predicting similar cases and also lets you create custom models tailored to your specific use cases.

## Before you begin

-   Ensure that the Task Intelligence for Customer Service plugin is installed.
-   Ensure that your instance contains sufficient open incident records \(minimum 10,000 recommended\) for meaningful training.
-   Role required: ml\_admin, ti\_admin

## Set up the prediction model

## Procedure

1.  Navigate to **All** &gt; **Task Intelligence for Customer Service** &gt; **Setup**.

    The Task Intelligence Admin Console displays.

2.  On the Similar Open Incidents card, select **Ready to train**.

    The model opens in a guided setup flow. The Define the purpose screen appears.

3.  **Define the purpose:**

    1.  Review the pre-filled Model name.

    2.  The Prediction table and Training table are pre-selected as **Cases** and **Incidents**, respectively.

        These values are fixed and cannot be edited.

    3.  Select **Save &amp; Continue**.

        The Train your model screen appears.

4.  **Train your model:**

    1.  The **Model name** and **Prediction table** fields are pre-filled and cannot be edited.

    2.  Apply **Conditions** to filter the training data.

    3.  In the **Prediction table** field, select fields such as Description and Short description that the model should use to identify similarities.

    4.  In the **Training table** section, select matching or relevant fields that help the model compare open incidents.

    5.  Choose the **language** for training.

    6.  Set the **Update frequency**.

    7.  Review the **Number of records**.

        If needed, select the **Load records** icon to reload.

    8.  Enable **Auto-retrain** to allow retraining the model on a set schedule.

    9.  Select **Launch training**.

    10. Once training starts, select **View current results** to preview sample outputs.

        The Assess and define screen appears.

5.  **Assess and define**:

    1.  Review the **Estimated number of records** used for training.

    2.  In **Prediction preference**, select one of the following options:

        -   Recommendations – Recommends similar open incidents \(selected by default\).
        -   Monitor only – Runs the model in the background without displaying recommendations. You can analyze the logged data before enabling recommendations.
        -   Turn off predictions – Disables all predictions for this model.
    3.  Select **Save &amp; Continue**.

        The Deploy your model screen appears.

6.  **Deploy your model**:

    1.  Review your setup and training summary and then select **Deploy** to activate the model.

        A confirmation message appears when deployment is complete.

    **Result**

    Once deployed, similar open incidents are displayed in the Recommended Actions section under the Suggested Actions tab when an agent opens a case that helps them resolve cases faster using related issues and prior solutions.


