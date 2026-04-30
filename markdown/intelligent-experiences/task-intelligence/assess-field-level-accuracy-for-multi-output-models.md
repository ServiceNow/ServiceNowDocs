---
title: Assess field-level accuracy for multi-output models
description: Evaluate the performance of your model by field.
locale: en-US
release: xanadu
product: Task Intelligence
classification: task-intelligence
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Assess a Task Intelligence model, Manage machine learning models with Task Intelligence, Task Intelligence, Enable AI experiences]
---

# Assess field-level accuracy for multi-output models

Evaluate the performance of your model by field.

## Before you begin

Role required: admin

## About this task

After you have created and tested your model, assess its performance to evaluate how well it's predicting what you want it to predict. For multi-output models that predict multiple fields, you may want to assess the performance of each field individually.

If you have not already created a model, see either [Create a model to predict record fields](https://www.servicenow.com/docs/access?context=csm-task-intel-create-cat-solution&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US) or [Create a model to predict incident fields](https://www.servicenow.com/docs/access?context=create-incident-prediction-model&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US) to make one.

Your model must be in Monitoring mode. You can set Monitoring mode on the Assess Your Model screen. For more details, see the Set your preferences step in [Create a case field prediction model](https://www.servicenow.com/docs/access?context=csm-task-intel-create-cat-solution&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US) or [Create a model to predict incident fields](https://www.servicenow.com/docs/access?context=create-incident-prediction-model&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US) model.

## Procedure

1.  Navigate to the **Predictor Results** \(ml\_predictor\_results\_task\) by entering `ml_predictor_results_task.list` in the Application navigator.

2.  Filter the **Predicted Output Value Name** for the name of the field you want to assess, such as "product" or "category."

3.  Group the list by **Predicted Correctly** by selecting the list controls icon in the top left corner of the screen.

    ![List control open to group by Predicted Correctly](../images/predictor-results-list.png)

4.  Divide the number of records where **Predicted Correctly** is **true** by the total number of records.

    This represents your accuracy for the specific field.

5.  Follow steps 2-4 for each field in which you would like to calculate the accuracy.

6.  View the performance of your model on the Monitoring screen.

    1.  Navigate to **Task Intelligence for Customer Service** &gt; **Monitoring** in the Application navigator.

        The Monitoring screen allows you to select the model, field, and date range to display in the charts. Accuracy is measured based on whether the top autofilled value or the top 3 recommendations are correct.

        ![Monitoring screen showing options to view model performance charts at the field level.](../images/task-intel-analytics.png)

    2.  Select a model.

    3.  Select an output column for the field.

    4.  Select a date range.


## What to do next

If the accuracy of each field is acceptable, transition your model from monitoring mode to real-time predictions and deploy. If the accuracy of a specific field is not acceptable, you can remove that output field from your model, retrain, and deploy. See [Edit a Task Intelligence model](../concept/edit-a-task-intelligence-model.md) for more information on editing your model.

