---
title: Minimum records needed for label to include it
description: Set a threshold for the minimum number of records a label must have in your dataset to be included in model training.
locale: en-US
release: zurich
product: Predictive Intelligence
classification: predictive-intelligence
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuring advanced settings for your ML solutions, Configure Predictive Intelligence, Predictive Intelligence, Enable AI experiences]
---

# Minimum records needed for label to include it

Set a threshold for the minimum number of records a label must have in your dataset to be included in model training.

## Before you begin

Verify that your dataset includes label values suitable for classification.

Role required: ml\_admin or admin

## About this task

This advanced option helps to eliminate labels that occur infrequently. Setting this minimum threshold can reduce overfitting and unreliable predictions.

To configure, you provide a number for a minimum count of records. Any class value with fewer records than the minimum is dropped from the training set. Class values that are dropped before training can't appear in predictions.

To add this option using a script:

```
config.setMinLabelCount(50);
```

In JSON format:

```
{
    "min_label_count": 50
    }
```

## Procedure

1.  To add this option in the solution definition form, navigate to **All** &gt; **Predictive Intelligence** &gt; **Classification** &gt; **Solution Definitions**.

2.  Open an existing classification solution or create a new one.

3.  Select the **Advanced Solution Settings** tab in the **Related Links** section of the form.

4.  Select **New** to open the **Advanced Solution Setting** \(ml\_advanced\_solution\_settings\) form.

5.  In the **Solution Parameters** field, search for `minimum records needed for label to include it`.

6.  In the **User Inputs** field, enter the number of records you want as the minimum, then select **Submit**.

    ![On the Advanced Solution Setting form, the Solution Parameters field and the User Inputs field are highlighted. The User Inputs field has an example value of 30.](../images/predictive-intel-minimum-records-needed-labelZ1.png)


## Result

The setting appears as a row on the **Advanced Solution Setting** tab on your solution's form.

## What to do next

Retrain your solution.

**Related topics**  


[Using Machine Learning APIs](../concept/using-ml-apis.md#)

[Create and train a classification solution](create-solution-definition.md)

