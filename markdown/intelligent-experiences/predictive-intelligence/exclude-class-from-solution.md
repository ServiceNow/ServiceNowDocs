---
title: Exclude a class from solution training
description: Exclude a class from solution training to prevent the model from ever making predictions for a particular output field class. For example, you can exclude a particular incident category from training if you plan to retire or change the category.
locale: en-US
release: xanadu
product: Predictive Intelligence
classification: predictive-intelligence
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Create and train a classification solution, Creating and training solutions, Predictive Intelligence, Enable AI experiences]
---

# Exclude a class from solution training

Exclude a class from solution training to prevent the model from ever making predictions for a particular output field class. For example, you can exclude a particular incident category from training if you plan to retire or change the category.

## Before you begin

Role required: admin or ml\_admin

## About this task

Excluding a class from training doesn't prevent the solution from making predictions for records that use the excluded class. Solution training still uses the input and output field values as data and attempts to match input field values to a new output field class. This attempt may cause undesirable prediction results unless you have another suitable class to replace the excluded class value.

Typically, you only exclude a class from training if you change the list of valid output field values. For example, if you replaced one incident category with another incident category, you may exclude the old category from training so that the solution only uses the new category for predictions.

**Note:** If you specify a target recall for a class, don't exclude the class from training even if the number of records are less than 30 for that class.

## Procedure

1.  Navigate to **All** &gt; **Predictive Intelligence** &gt; **Classification** &gt; **Solution Definitions**.

    The system shows the current list of solution definitions.

2.  Select the solution definition you want to edit.

    For example, select **Incident Categorization** to exclude an incident category from training.

3.  Edit the filter to exclude the class.

    You can use the **\[is one of\]** or **\[is not one of\]** operators to exclude a particular class.

    For example, if you want to exclude the Hardware class, add this condition: **\[Category\] \[is not one of\] \[Hardware\]**.

4.  Click **Update &amp; Train**.

    The system schedules the solution for training with the nearest training service. When training is complete, the system uploads the solution as an Attachment record.


## Result

The solution excludes the class from all predictions.

## What to do next

Review the trained solution precision and coverage statistics.

