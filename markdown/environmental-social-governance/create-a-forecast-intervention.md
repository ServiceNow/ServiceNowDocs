---
title: Adjust parameters
description: Adjust parameters to model different outcomes based on specific interventions or changes. When you update these parameters it enables your organization to explore the potential impacts of different decisions, providing a clear comparison of outcomes.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Set up analysis contexts and analyses, Use, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Adjust parameters

Adjust parameters to model different outcomes based on specific interventions or changes. When you update these parameters it enables your organization to explore the potential impacts of different decisions, providing a clear comparison of outcomes.

## Before you begin

Role required: sn\_esg.program\_manager

## Procedure

1.  Navigate to **All** &gt; **Operational Sustainability Management** &gt; **Operational Sustainability Workspace** &gt; **Lists** &gt; **Analysis contexts**.

2.  Select the Analysis context record that you want and navigate to the **Analysis** tab.

3.  Select the Analysis record that you want and then navigate to the **Forecast** tab.

4.  Select the information icon ![Information icon.](../../../reuse/icons/product-icons/circle-info-outline-24.svg) to open the forecast sidebar and fill in the parameter fields.

<table id="table_zqs_sgr_fgc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Period

</td><td>

The timeframe used for simulating the adjusted forecast information.

</td></tr><tr><td>

Calculated metric definition \(CMD\) formula operands

</td><td>

The parameters that were used in the formula.Original values used for the forecast are displayed for each of the parameter fields. You can adjust each parameter to model different interventions and their outcomes.

For example, if your formula is as follows:

```
(Total electricity consumption - Solar panel contribution) * Emission factor
```

, the following parameter fields would be available to adjust: Total electricity consumption, Solar panel contribution, Emission factor. By modifying these parameters, you can simulate various analyses to assess the impact of different sustainability interventions on emissions.

**Note:**

-   The fields displayed vary based on the operands chosen in the CMD formula and differ according to the specific CMD.
-   These fields appear when creating an analysis context with a metric definition selected in the **Type** field and a calculated metric definition selected in the **Metric definition** field. For more information, refer to [Create an analysis context](create-an-analysis-context.md).


</td></tr><tr><td>

Adjustment

</td><td>

Choose an adjustment type absolute \(123\) or percentage \(%\) and enter the corresponding adjustment value.**Note:**

-   This fields appear when while creating a analysis context, the metric definition is selected in **Type** field, a manual or automated metric definition is selected in **Metric definition** field.
-   This fields appears when creating a analysis context, a metric is selected in **Type** field and a metric is selected in the **Metric** field. For more information, refer to [Create an analysis context](create-an-analysis-context.md).


</td></tr></tbody>
</table>5.  Select **Save**.

    The updated parameters are used to simulate the calculation based upon the updated values that were entered. The forecast graph shows the original standard forecast and the new adjusted forecast and the formula parameters for each are shown in the Formula parameters section.

6.  Repeat the above until the new adjusted forecast and formula parameters meet your requirements.

7.  Select **Publish**.

    After publishing, you will not be able to make any changes to the parameters.


## What to do next

After creating and publishing multiple analyses and forecasts, you can compare the analyses and view a graph that captures the data for each analysis you select. For more information on viewing a Comparison graph see, [Create a forecast comparison graph](create-forecast-comparison.md). For more information on creating analyses, see [Create an analysis](create-a-scenario-analysis.md).

**Parent Topic:**[Set up analysis contexts and analyses](../concept/set-up-scenarios.md)

