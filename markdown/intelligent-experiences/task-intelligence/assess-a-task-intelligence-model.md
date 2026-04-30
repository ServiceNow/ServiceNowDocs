---
title: Assess a Task Intelligence model
description: Assessing a machine learning model's performance helps determine how to use and train the model to achieve your desired outcomes.
locale: en-US
release: xanadu
product: Task Intelligence
classification: task-intelligence
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Manage machine learning models with Task Intelligence, Task Intelligence, Enable AI experiences]
---

# Assess a Task Intelligence model

Assessing a machine learning model's performance helps determine how to use and train the model to achieve your desired outcomes.

## Overview of assessing a Task Intelligence model

The Assess Your Model screen allows you to evaluate the model’s performance. After training or retraining your model, the Assess Your Model screen will show an estimate of the model’s average performance against your most recent data.

**Note:** It is normal to see some variability in model performance from day to day. Performance tends to average out to the estimated performance over time.

![Assess your model screen showing estimated number of autofilled field values, last training date, and sample test results](../images/assess-your-model-screen.png)

The Assess Your Model screen also allows you to view example predictions on a sample of records. These examples demonstrate the predictions but do not necessarily reflect the quality or average performance of the model. The estimates provided on the Assess Your Model screen as well as the reports on the **Monitoring** page are calculated from a much larger number of cases.

You can also use the Assess Your Model screen to choose one of the following preferences for each field:

-   **Autofill** the predicted value in the field.
-   **Recommendations** are provided for the predicted value in the field.
-   **Monitor only** and run the prediction model for the field only in the background.
-   **Turn off predictions** for the field.

## Monitoring mode

Monitoring mode allows you to monitor the performance of a model at the field level without the predictions being applied to records. The model runs in the background only and can be trained and retrained until you are satisfied with its performance. You can set the model fields to Monitoring mode from the Assess Your Model screen when [editing your model](edit-a-task-intelligence-model.md).

You can view and track model performance with the Task Intelligence Admin Console. See [Task Intelligence Analytics and Monitoring](task-intelligence-analytics-and-monitoring.md).

