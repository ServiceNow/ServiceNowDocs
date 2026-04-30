---
title: Track classification prediction results over time
description: Use the Prediction Results dashboard to determine if classification solution predictions are improving over time. Identify solutions that need refining or retraining.
locale: en-US
release: yokohama
product: Predictive Intelligence
classification: predictive-intelligence
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Testing and monitoring predictions, Predictive Intelligence, Enable AI experiences]
---

# Track classification prediction results over time

Use the Prediction Results dashboard to determine if classification solution predictions are improving over time. Identify solutions that need refining or retraining.

## Before you begin

-   Role required: admin, ml\_admin, or ml\_report\_user

## About this task

The Prediction Results dashboard reports on coverage, precision, and recall over time for classification solutions.

With the Xanadu release, this dashboard has been migrated to the Next Experience UI. Customers upgrading from previous releases can access the Core UI version from the current dashboard. ![The Prediction Results dashboard for classification solutions, displayed in the Next Experience UI.](../images/review-prediction-results_X1.png)

On the Prediction Results dashboard, statistics are provided in two timeframes: the average for the past 30 days, and daily. The indicators coverage, precision, and recall are defined as follows.

|Report type|Definition|
|-----------|----------|
|Coverage|The percentage of predictions that yielded an outcome out of the total number of predictions that were attempted.|
|Precision|The percentage of predictions where the predicted value was the same as the final value of the field when the report closed.|
|Recall|The percentage of correct predictions that yielded an outcome out of the total number of predictions that were attempted.|

## Procedure

1.  Navigate to **All** &gt; **Predictive Intelligence** &gt; **Classification** &gt; **Prediction Results Report**.

2.  In the Prediction Results dashboard **Filter by solution** prompt, select the solution statistics you want to review.

    The system updates the dashboard based on the solution you selected.

3.  Identify classes with anomalous coverage, precision, or recall values.

    For example, identify solutions where coverage, precision, or recall is declining over time.


## What to do next

Refine the solution definition filter by including or excluding classes as needed. After updating, retrain the solution.

