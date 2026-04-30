---
title: Exclude a class from prediction
description: Exclude a class from prediction if its precision or coverage aren't satisfactory. Excluding a class prevents the classification model from predicting a particular output field value.
locale: en-US
release: zurich
product: Predictive Intelligence
classification: predictive-intelligence
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Create and train a classification solution, Creating and training solutions, Predictive Intelligence, Enable AI experiences]
---

# Exclude a class from prediction

Exclude a class from prediction if its precision or coverage aren't satisfactory. Excluding a class prevents the classification model from predicting a particular output field value.

## Before you begin

-   Train the solution definition whose output field values you want to exclude.
-   Role required: admin or ml\_admin

## About this task

As part of the testing and refinement of your classification solution, you can try excluding an output class to check the effect on the model's results.

Excluding a class from prediction is temporary. The class is restored the next time you train your solution, as long as the solution definition remains the same. If your precision or coverage targets are still not met, consider deactivating the solution or changing the solution definition.

Typically, you exclude a class from prediction if you want a person to manually set the excluded class value. For example, exclude a particular incident category when the solution doesn't offer sufficient precision or coverage, or because the class triggers other business logic that requires review or approval.

## Procedure

1.  Navigate to **All** &gt; **Predictive Intelligence** &gt; **Classification** &gt; **Solutions**.

2.  In the ML Solutions list, select the solution whose classes you want to exclude.

    This solution must have a **State** of **Solution Complete**.

3.  In the **Class Confidence** related list, select the class you want to exclude.

4.  In the Class Confidence record, review the precision and coverage combinations available from the **Precision Coverage Lookups** embedded list.

5.  Select the check box for the 100 precision and 0 coverage combination.

    You can select only one check box.

6.  From the Actions on selected rows control, select **Apply Values**.

    The system shows a **Precision / Coverage Setting** confirmation window.

7.  Click **OK** to confirm the change or **Cancel** to discard it.


## Result

The solution excludes the class from all predictions until the next training cycle.

## What to do next

If you conclude that this class does not contribute to meaningful predictions, consider deactivating the solution or changing the solution definition.

