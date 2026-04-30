---
title: Exclude a class from prediction
description: Exclude a class from prediction if its precision or coverage statistics don't meet your threshold of usefulness. For example, exclude it if you don't want the model to predict a particular output field value.
locale: en-US
release: xanadu
product: Predictive Intelligence
classification: predictive-intelligence
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Create and train a classification solution, Creating and training solutions, Predictive Intelligence, Enable AI experiences]
---

# Exclude a class from prediction

Exclude a class from prediction if its precision or coverage statistics don't meet your threshold of usefulness. For example, exclude it if you don't want the model to predict a particular output field value.

## Before you begin

-   Train the solution definition whose output field values you want to exclude.
-   Role required: admin or ml\_admin

## About this task

If your classification solution doesn't provide sufficient precision or coverage, you can exclude a particular incident category from prediction.

Excluding a class from prediction only lasts until the next time you train your solution. If a class still doesn't provide sufficient precision or coverage values, you may want to consider deactivating the solution until it provides better results.

Typically, you exclude a class from prediction if you only want a person to manually set the excluded class value. For example, exclude the class if the solution doesn't offer sufficient precision or coverage, or because the class triggers other business logic that requires review or approval.

## Procedure

1.  Navigate to **All** &gt; **Predictive Intelligence** &gt; **Classification** &gt; **Solutions**.

2.  In the ML Solutions list, select the solution whose classes you want to exclude.

    This solution must have a **State** of **Solution Complete**.

3.  In the **Class Confidence** related list, select the class you want to exclude.

4.  In the Class Confidence record, review the precision and coverage combinations available from the **Precision Coverage Lookups** embedded list.

5.  Select the check box for the 100 precision and 0 coverage combination.

    You can only select one check box.

6.  From the Actions on selected rows control, select **Apply Values**.

    The system shows a **Precision / Coverage Setting** confirmation window.

7.  Click **OK** to confirm the change or **Cancel** to discard it.


## Result

The solution excludes the class from all predictions until the next training cycle.

## What to do next

If you conclude this class will never produce meaningful predictions, consider deactivating the solution or changing the solution definition.

