---
title: Configure include only top N labels
description: Limit your classification model to use only the most common classes when training. You can specify the number of classes to use.
locale: en-US
release: australia
product: Predictive Intelligence
classification: predictive-intelligence
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring advanced settings for your ML solutions, Configure Predictive Intelligence, Predictive Intelligence, Enable AI experiences]
---

# Configure include only top N labels

Limit your classification model to use only the most common classes when training. You can specify the number of classes to use.

## Before you begin

Role required: ml\_admin or admin

## About this task

Restricting the model to a fixed number of the most frequent labels improves focus and performance, especially with large datasets.

You can add this option in the solution definition form by using the following procedure. Alternatively, you can use a script to add this option.

To add this option using a script:

```
config.setTopNLabels(100);
```

In JSON format:

```
{
    "include_top_n_labels": 100
    }
```

## Procedure

1.  To add this option in the solution definition form, navigate to **All** &gt; **Predictive Intelligence** &gt; **Classification** &gt; **Solution Definitions**.

2.  Open an existing classification solution or create a new one.

3.  Select the **Advanced Solution Settings** tab in the **Related Links** section of the form.

4.  Select **New** to open the **Advanced Solution Setting** \(ml\_advanced\_solution\_settings\) form.

5.  In the **Solution Parameters** field, search for `include only top n labels`.

6.  In the **User Inputs** field, enter the number of classes you want as the limit, then select **Submit**.

    ![On the Advanced Solution Setting form, the Solution Parameters field and the User Inputs field are highlighted. The User Inputs field displays an example value of 100.](../images/predictive-intel-only-top-n-labelsZ1.png)


## Result

The setting appears as a row on the **Advanced Solution Setting** tab on your solution's form.

## What to do next

Retrain your solution.

**Parent Topic:**[Configuring advanced settings for your ML solutions](../concept/configuring-advanced-settings-ml-solutions.md)

**Related topics**  


[Using Machine Learning APIs](../concept/using-ml-apis.md#)

[Create and train a classification solution](create-solution-definition.md)

