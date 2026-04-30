---
title: Adjust parameters
description: Adjust parameters to model different outcomes based on specific interventions or changes. When you update these parameters it enables your organization to explore the potential impacts of different decisions, providing a clear comparison of outcomes.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2025-01-13"
reading_time_minutes: 2
breadcrumb: [Set up analysis contexts and analyses, Using ESG Management, Environmental, Social, and Governance Management]
---

# Adjust parameters

Adjust parameters to model different outcomes based on specific interventions or changes. When you update these parameters it enables your organization to explore the potential impacts of different decisions, providing a clear comparison of outcomes.

## Before you begin

Role required: sn\_esg.program\_manager

## Procedure

1.  Navigate to **All** &gt; **Environmental, Social, and Governance** &gt; **ESG Workspace** &gt; **Lists** &gt; **Analysis contexts**.

2.  Select the Analysis context record that you want and navigate to the **Analysis** tab.

3.  Select the Analysis record that you want and then navigate to the **Forecast** tab.

4.  Select the information icon ![Information icon.](../../../reuse/icons/product-icons/circle-info-outline-24.svg) to open the forecast sidebar and fill in the parameter fields.

<table id="table_lrv_yw4_brb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Period

</td><td>

The timeframe used for simulating the adjusted forecast information.

</td></tr><tr><td>

Parameter

</td><td>

The parameters that were used in the formula.Original values used for the forecast are displayed for each of the parameter fields. You can adjust each parameter to model different interventions and their outcomes.

For example, if your formula is as follows:

```
(Total electricity consumption - Solar panel contribution) * Emission factor
```

, the following parameter fields would be available to adjust: Total electricity consumption, Solar panel contribution, Emission factor. By modifying these parameters, you can simulate various analyses to assess the impact of different sustainability interventions on emissions.

</td></tr></tbody>
</table>5.  Select save.

    The updated parameters are used to simulate the calculation based upon the updated values that were entered. The forecast graph shows the original standard forecast and the new adjusted forecast and the formula parameters for each are shown in the Formula parameters section.

6.  Repeat steps 4 and 5 until the new adjusted forecast and formula parameters meet your requirements.

7.  Select **Publish**.

    After publishing, you will not be able to make any changes to the parameters.


## What to do next

After creating and publishing multiple analyses and forecasts, you can compare the analyses and view a graph that captures the data for each analysis you select. For more information on viewing a Comparison graph see, [Create a forecast comparison graph](create-forecast-comparison.md). For more information on creating analyses, see [Create an analysis](create-a-scenario-analysis.md).

**Parent Topic:**[Set up analysis contexts and analyses](../concept/set-up-scenarios.md)

