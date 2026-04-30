---
title: Use LightGBM algo for classification model training
description: Enable the LightGBM \(Light Gradient-Boosting Machine\) algorithm as an advanced option for training classification models.
locale: en-US
release: zurich
product: Predictive Intelligence
classification: predictive-intelligence
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuring advanced settings for your ML solutions, Configure Predictive Intelligence, Predictive Intelligence, Enable AI experiences]
---

# Use LightGBM algo for classification model training

Enable the LightGBM \(Light Gradient-Boosting Machine\) algorithm as an advanced option for training classification models.

## Before you begin

Role required: ml\_admin or admin

## About this task

The LightGBM algorithm offers performance and efficiency for large datasets. For detailed information about this algorithm see [https://lightgbm.readthedocs.io](https://lightgbm.readthedocs.io).

Use the following procedure to add this option in the solution definition form. Alternatively, you can use a script to add this algorithm.

To add this option using a script:

```
var config = new MLPredictorConfig('ml_solution_ID');
                    config.useLightGBM();
                    config.updateConfig();
```

In JSON format:

```
{
    "use_lightgbm": true
    }
```

## Procedure

1.  Navigate to **All** &gt; **Predictive Intelligence** &gt; **Classification** &gt; **Solution Definitions**.

2.  Open an existing classification solution or create a new one.

3.  Select the **Advanced Solution Settings** tab in the **Related Links** section of the form.

4.  Select **New** to open the **Advanced Solution Setting** \(ml\_advanced\_solution\_settings\) form.

5.  In the **Solution Parameters** field, search for `Use LightGBM algo for classification model training`.

6.  Leave the **User Inputs** field blank, and select **Submit**.

    ![In the Advanced Solution Setting new record, in the Solution Parameters field, the option Use LightGBM algo for classification model training is highlighted.](../images/predictive-intel-lightgbm-algoZ1.png)


## Result

The setting appears as a row on the **Advanced Solution Setting** tab on your solution's form.

## What to do next

Retrain your solution.

**Related topics**  


[Using Machine Learning APIs](../concept/using-ml-apis.md#)

[Create and train a classification solution](create-solution-definition.md)

