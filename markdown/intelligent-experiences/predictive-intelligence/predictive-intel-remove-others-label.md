---
title: Remove others label
description: Reduce noise in your classification model and enhance predictive accuracy by removing records with the label "others" from training data. These are records with a distribution frequency of under one percent.
locale: en-US
release: yokohama
product: Predictive Intelligence
classification: predictive-intelligence
topic_type: task
last_updated: "2025-07-15"
reading_time_minutes: 1
breadcrumb: [Configuring advanced settings for your ML solutions, Configure Predictive Intelligence, Predictive Intelligence, Enable AI experiences]
---

# Remove others label

Reduce noise in your classification model and enhance predictive accuracy by removing records with the label "others" from training data. These are records with a distribution frequency of under one percent.

## Before you begin

Role required: ml\_admin or admin

## About this task

When this option is set to true, records under 1% of total data distribution are excluded from training. These records are labeled "others" in the interface. The 1% threshold can't be modified.

You can add this option in the solution definition form by using the following procedure. Alternatively, you can use a script to add this option.

To add this option using a script:

```
config.removeOthersLabel(true);
```

In JSON format:

```
{
    "remove_others_label": true
    }
```

## Procedure

1.  To add this option in the solution definition form, navigate to **All** &gt; **Predictive Intelligence** &gt; **Classification** &gt; **Solution Definitions**.

2.  Open an existing classification solution or create a new one.

3.  Select the **Advanced Solution Settings** tab in the **Related Links** section of the form.

4.  Select **New** to open the **Advanced Solution Setting** \(ml\_advanced\_solution\_settings\) form.

5.  In the **Solution Parameters** field, search for `Remove others label`, then select **Submit** to save your update.

    ![On the Advanced Solution Setting form, in the Solution Parameters field, Remove others label is selected.](../images/predictive-intel-remove-others-labelZ1.png)


## Result

The setting appears as a row on the **Advanced Solution Setting** tab on your solution's form.

## What to do next

Retrain your solution.

**Related topics**  


[Using Machine Learning APIs](../concept/using-ml-apis.md#)

[Create and train a classification solution](create-solution-definition.md)

