---
title: Get familiar with MetricBase APIs
description: Experiment with MetricBase APIs using Data Explorer that is part of the MetricBase Demo application. Data Explorer uses the data installed with the MetricBase Demo application.
locale: en-US
release: australia
product: MetricBase
classification: metricbase
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Working with demo data, Configure, MetricBase, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Get familiar with MetricBase APIs

Experiment with MetricBase APIs using Data Explorer that is part of the MetricBase Demo application. Data Explorer uses the data installed with the MetricBase Demo application.

## Before you begin

Role required: clotho\_admin

## About this task

Data Explorer is a playground where you can see and edit example scripts that visualize data included with the MetricBase Demo application. The example scripts use the MetricBase JavaScript APIs. For information on the MetricBase JavaScript APIs, see [Client](https://www.servicenow.com/docs/access?context=ClientScopedAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US), [Data](https://www.servicenow.com/docs/access?context=DataScopedAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US), [DataBuilder](https://www.servicenow.com/docs/access?context=DataBuilderScopedAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US), [Transformer](https://www.servicenow.com/docs/access?context=TransformerScopedAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US), [TransformPart](https://www.servicenow.com/docs/access?context=TransformPartScopedAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US), [TransformResult](https://www.servicenow.com/docs/access?context=TransformResultScopedAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US).

Note that the now/v1/clotho/transform/topic API endpoint is reserved for internal use only.

Example scripts use either:

-   Transforms, which use the [Transformer](https://www.servicenow.com/docs/access?context=TransformerScopedAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US) method.
-   Machine Language, trained models that predict expected behavior. All the scripts without "Transform" in their title use Machine Language.

## Procedure

1.  Navigate to **All** &gt; **MetricBase Demo** &gt; **Data Explorer**.

    The **Data Explorer** displays.

    ![Data Explorer UI](../image/data-explorer.png)

    When you run a script, the data visualization appears under **Data Explorer Script Result Display**.

2.  Select one of the sample scripts to run in the **Example Script** menu.

    ![Steps to run a script](../image/data-explorer-buttons.png)

3.  Click **Load Example**.

4.  Click **Run**.

    The script displays the data visualization under **Data Explorer Script Result Display**.

5.  Change the values or statements in the script or write an entirely new script and click **Run**.

    **Note:** If you want to save the changes you made in the script, click **Save**.

6.  Under **Server Output**, look at the server's response that might include error information.


## Example

<table id="table_v2g_vkq_23b"><thead><tr><th>

Example script

</th><th>

Definition and visualization

</th></tr></thead><tbody><tr><td>

Simple Transform

</td><td>

Uses the transformer API to display a single time-series metric, the average speed of the drones: `transformer.metric('mb_demo_mt_speed').avg`\(\). ![Simple transform using average](../image/data-explorer-average-speed.png)

</td></tr><tr><td>

Simple Transform with Grouping

</td><td>

Uses the transformer API to display a group of time-series metrics, the average altitude of the fleet of the drones: ```
transformer.groupBy("fleet").metric("mb_demo_mt_altitude").
      avg().label('avg - %g:fleet:')
```

 ![Grouping transform](../image/data-explorer-simple-xform-grouping.png)

</td></tr><tr><td>

Normal Model

</td><td>

Models normal data, which approximates a bell-shaped or Gaussian curve for distributed values.

</td></tr><tr><td>

Linear Model

</td><td>

Creates a line to summarize the current data and predict future values. This example, about the remaining charge in drone batteries, graphs both the trained model values and the average of the values.```
var builder = new sn_clotho.Transformer(drones);
var fit = builder.metric("mb_demo_nt_rem_battery").resample(100).
          fit({model:"linear"}).label("Fitted");
builder.metric("nb_demp_mt_rem_battery").avg().label("Original")
```

 ![Linear model](../image/data-explorer-linear-model.png)

</td></tr><tr><td>

Seasonal Trend Decomposition Model

</td><td>

Uses a seasonal trend model so that data can be subtracted to reveal non-seasonal trends. This model is similar in purpose to the Holt Winters model but arrives at the result using different algorithms.```
var builder = new sn_clotho.Transformer(drones);
var metric = "nb_demo_mt_rem_battery";
var fit = builder.metric(metric).fit({model:"STL",periodicity:"PT2H", 
          innerCycles:1, outerCycles:10})
```

 ![Seasonal correction to trend](../image/data-explor-seasonal-trend-decomp.png)

</td></tr><tr><td>

Holt Winters Model

</td><td>

Uses the Holt Winters, seasonal trend model so that data can be subtracted to reveal non-seasonal trends. This model is similar in purpose to the Seasonal Trend Decomposition model but arrives at the result using different algorithms.

</td></tr><tr><td>

ARIMA Model

</td><td>

The most general class of models for predicting time-series data that has no trend, meaning all the data has the same value or the values fluctuate sinusoidally around the mean.

</td></tr><tr><td>

Deviation Model

</td><td>

Uses chisquare model to show the differences between the real data and the model's prediction. ```
var metric = "nb_demo_mt_rem_battery";
builder.metric(metric).deviation(model, "chiSquare");
```

 ![Deviation model](../image/data-explor-chisquare-deviation.png)

</td></tr></tbody>
</table>**Parent Topic:**[Working with MetricBase demo data](../concept/working-with-metricbase-demo-data.md)

