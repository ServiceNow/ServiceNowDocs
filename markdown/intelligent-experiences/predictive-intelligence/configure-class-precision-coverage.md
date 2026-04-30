---
title: Tune a trained classification solution
description: Tune the performance of a trained classification solution by configuring class level precision and coverage values.
locale: en-US
release: zurich
product: Predictive Intelligence
classification: predictive-intelligence
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Create and train a classification solution, Creating and training solutions, Predictive Intelligence, Enable AI experiences]
---

# Tune a trained classification solution

Tune the performance of a trained classification solution by configuring class level precision and coverage values.

## Before you begin

-   Train the solution definition whose output field values you want to configure.
-   Role required: admin or ml\_admin

## About this task

The system creates a class record for each output field value that it can predict. Each class record includes a list of possible precision and coverage combinations to choose from. By default, solutions use the highest combination of precision and coverage available. You can select another combination to refine predictions based on acceptable precision and coverage values.

## Procedure

1.  Navigate to **All** &gt; **Predictive Intelligence** &gt; **Classification** &gt; **Solutions**.

    The system shows the list of available solutions.

2.  Select the solution whose classes you want to configure.

    This solution must have a **State** of **Solution Complete**.

    The system shows the Solution record.

3.  From the **Class Confidence** related list, select the class you want to configure.

    The solution only lists output field values for which it can make predictions. If the output field value is missing from this list, update the solution definition filter to provide more data for this output field value, and retrain the solution.

    The system shows the Class Confidence record.

4.  Review the precision and coverage combinations available from the **Precision Coverage Lookups** embedded list.

5.  Select the check box for the precision and coverage combination you want to use to make predictions for this class.

    You can only select one check box. Some combinations produce special prediction results.

    |Prediction result|Precision|Coverage|
    |-----------------|---------|--------|
    |Never include class in predictions|100|0|
    |Always include class in predictions|0|100|

6.  From the Actions on selected rows control, select **Apply Values**.

    The system shows a **Precision / Coverage Setting** confirmation window.

7.  Click **OK** to confirm the change or **Cancel** to discard it.


## What to do next

Test predictions for this class to verify that the system produces acceptable results.

