---
title: Edit a model
description: Edit the case models that have already been trained and deployed. Change the model configurations, view the updated training results, and redeploy the model.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Task Intelligence for Customer Service, Machine learning solutions, Implement Intelligence, Configure, Customer Service Management]
---

# Edit a model

Edit the case models that have already been trained and deployed. Change the model configurations, view the updated training results, and redeploy the model.

## Before you begin

Role required: ti\_admin

A prediction model must already be created, trained, and deployed.

## About this task

You have two options for editing your model: view the current training results or retrain the model. The first time you edit a model, a pop-up appears to ask you which option you would like to take. Resetting your prediction preferences enables you to change how visible the predictions are for agents. Retraining your model enables you to select new data for training, which changes the prediction capabilities of the model. While you can retest your prediction model, it doesn’t change the prediction skills.

## Procedure

1.  Navigate to **All** &gt; **Task Intelligence for Customer Service** &gt; **Setup**.

2.  From the **Models** list, select the menu icon of the model you want to edit, and then select **Edit Model**.

3.  Modify the fields to get the required predictions.

4.  Select **Launch training**.

    A warning message appears asking if you want to update and train the model.

5.  Select **Retrain**.

    The new training results page loads.

6.  Select the **Compare models results** button to show both the previous results and the new results.

7.  Select **Save &amp; continue**.

8.  Set your preferences for displaying the predictions or running them in the background.

9.  Select **Save &amp; continue**.

    The **Deploy your model** screen loads and shows the changes that you made indicated in yellow. If you don't want to deploy the changes, select **Discard changes**.

10. Review the model and select **Redeploy**.

    Your updated model is deployed.


## What to do next

See how to [Export a model](export-a-task-intelligence-model.md)

