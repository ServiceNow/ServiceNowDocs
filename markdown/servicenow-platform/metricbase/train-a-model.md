---
title: Create and train a predictive model
description: Use statistical models to determine significant anomalies in real-time using MetricBase triggers. You will need to train a model using representative data that has already been stored in MetricBase.
locale: en-US
release: xanadu
product: MetricBase
classification: metricbase
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Detecting anomalies in MetricBase data using predictive models, Defining and collecting MetricBase data, MetricBase, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Create and train a predictive model

Use statistical models to determine significant anomalies in real-time using MetricBase triggers. You will need to train a model using representative data that has already been stored in MetricBase.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **MetricBase** &gt; **MetricBase Models**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_u35_xsq_23b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Model name

</td><td>

Name of the model. The name can be any combination of alphanumeric characters. This model name is not the same as the model class. In general, the name relates to the value in **Group by**.

</td></tr><tr><td>

Table name

</td><td>

Name of the table that contains the training data.

</td></tr><tr><td>

Metric

</td><td>

Name of the metric that you use to train the model. The metric must belong to the table.

</td></tr><tr><td>

Created

</td><td>

Date that you trained the model.

</td></tr><tr><td>

Filter

</td><td>

Filters that you use to exclude some of the data in the dataset.**Note:** When choosing data to train your model, try to select data that demonstrates an expected behavior to reduce anomalies in the training set.

</td></tr><tr><td>

Group by

</td><td>

You can use **Group by** as a discriminator field for your model data. For example, if you want to create a data model over a group of production servers whose performance differs by role \(such as database or application server roles\) then you would choose role as the **Group by** field. The training process creates one model per role in the group of records selected by the filter. You do not have to manually create a model for each role.

</td></tr><tr><td>

Model Class

</td><td>

The algorithm to use when training data. Select a moving average algorithm \(PEWMA, ARIMA\), a seasonal algorithm \(STL, HW\), or choose **Find Best Fit Model**. The default is **Find Best Fit Model**, which tries each algorithm and selects the one which appears to have the best fit over the training set.

</td></tr><tr><td>

Training Dataset Start Date

</td><td>

MetricBase time series data for the metric starting with this date.

</td></tr><tr><td>

Training Dataset End Date

</td><td>

MetricBase time series data for the metric ending with this date.

</td></tr><tr><td>

Valid until

</td><td>

Date that serves as a reminder to consider retraining the model. If the model is performing well, there's no need to retrain it. The model can continue working past this date.

</td></tr><tr><td>

Active

</td><td>

Option to use the trained model. Once the model is active it becomes available for use as a Workflow Studio trigger.

</td></tr></tbody>
</table>4.  Click **Submit and Train**.

    MetricBase trains the model. When complete, the model appears on the **MetricBase Model Instances** tab.

5.  Click the model name.

    The modeling data appears as does the model string with the parameters optimized by the training.

    ![Trained model data](../image/trained-model-results.png)

6.  Click the model name and then click **Set Model** to change the model parameters.

    You can edit the model parameters when you want to override the settings for training your model. The graph does not update, you are saving the revised model string.


## What to do next

You can create a Workflow Studio trigger for this model. For more information, see [Create a model trigger](create-metricbase-model-trigger.md).

