---
title: Edit an incident prediction model in Task Intelligence for ITSM
description: Edit either the Similar Incidents or Incident Categorization model that has already been trained and deployed. Change the model configurations, view the updated training results, and redeploy the model.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/task-intelligence-for-itsm/edit-your-model.html
release: australia
product: Task Intelligence for ITSM
classification: task-intelligence-for-itsm
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Manage, Task Intelligence for ITSM, IT Service Management]
---

# Edit an incident prediction model in Task Intelligence for ITSM

Edit either the Similar Incidents or Incident Categorization model that has already been trained and deployed. Change the model configurations, view the updated training results, and redeploy the model.

## Before you begin

A prediction model must already be created, trained, and deployed. For more information on how to create a model, see [Managing Task Intelligence for ITSM models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/task-intelligence-for-itsm/using-task-intelligence-itsm.md).

Role required: sn\_ti\_admin.tia\_admin or sn\_itsm\_ml\_task.ti\_admin

## About this task

You have two options for editing your model: view the current training results or retrain the model. The first time you edit a model, a pop-up appears to ask you which option you would like to take.

\[Omitted image "ti-edit-model.png"\] Alt text: UI of the popup options to edit your model.

Resetting your prediction preferences enables you to change how visible the predictions are for agents. Retraining your model enables you to select new data for training, which changes the prediction capabilities of the model.

While you can retest your prediction model, it doesn’t change the prediction skills. Edit your prediction model to reset your prediction preferences. Edit your prediction models to retrain the models with new data, predict different fields, or change the prediction preferences.

Changes aren’t saved until you redeploy the model. The updated model replaces the previous model.

## Procedure

1.  Navigate to **All** &gt; **Task Intelligence for ITSM** &gt; **Setup**.

2.  From the **Models** list, select the menu \(\[Omitted image "menu-icon.png"\] Alt text: Menu icon\) icon of the model you want to edit, and then select **Edit Model**.

3.  Modify the fields to get the required predictions.

4.  Select **Launch training**.

    A warning message appears.

    \[Omitted image "ti-edit-model-retrain.png"\] Alt text: Warning message.

5.  Select **Retrain**.

    The new training results page loads.

6.  Select the **Compare models results** button to show both the previous results and the new results.

7.  Select **Save &amp; continue**.

8.  Set your preferences for displaying the predictions or running them in the background.

9.  Select **Save &amp; continue**.

    The **Deploy your model** screen loads and shows the changes that you made indicated in yellow. If you don't want to deploy the changes, select **Discard changes**.

    \[Omitted image "ti-edit-retrain-review.png"\] Alt text: UI of the page to review the model changes.

10. Review the model and select **Redeploy**.


## Result

Your updated model is deployed.

**Parent Topic:**[Managing Task Intelligence for ITSM models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/task-intelligence-for-itsm/using-task-intelligence-itsm.md)

