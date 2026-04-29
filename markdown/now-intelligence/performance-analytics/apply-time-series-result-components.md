---
title: Applying time series to result or to contributing indicators
description: For a formula indicator, a time series aggregation can apply either to each indicator in the formula individually or to the formula result.
locale: en-US
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Formula indicators, Indicators, Configure fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Applying time series to result or to contributing indicators

For a formula indicator, a time series aggregation can apply either to each indicator in the formula individually or to the formula result.

Decide how time series aggregation apply with the **Apply time series to result** option. You can select or disable this option in the **Other** properties tab of a formula indicator record. This option applies to any time series aggregation you apply to the indicator in Core UI [Performance Analytics widgets](c_Widgets.md) and Analytics Hub, or in [Data visualizations in Platform Analytics](analytics-center-data-visualizations.md). This option also applies to the default time series if one is set on the indicator.

**Note:**

-   The default time series applies only on the Analytics Hub and KPI Details. If you do not select a time series aggregation on a widget or data visualization, the default time series does not apply.
-   For the setting to take effect on the Analytics Hub or KPI Details, you must choose a real aggregate, if the indicator does not have a default time series set. If the time series is just the indicator frequency \(daily, weekly, and so on\), the**Apply time series to result** setting does not apply.

When **Apply time series to result** is checked, first the formula is evaluated and then the selected time series is applied to the final result. When **Apply time series to result** is not checked, each [contributing indicator](performance-analytics-glossary.md#) is evaluated and the default time series is applied to it. Then the formula is evaluated. The results between the two settings can differ significantly. Neither setting is wrong, but you have to think carefully about what you are measuring before making your choice.

## Applying a time series to result compared to applying it to contributing indicators

Consider the formula indicator "% of new P1 incidents". Every day this indicator calculates the percentage of new incidents that are Priority 1 - Critical:

\( \[\[Number of new incidents &gt; Priority = 1 - Critical\]\] / \[\[Number of new incidents\]\] \) \* 100

You decide that you want the result to display a 7-day running average by default on the Analytics Hub. In the **Other** tab of the indicator record, you select the 7d running AVG default time series. You apply the time series to the result. ![The Other properties tab of a Formula Indicator record showing Default time series and Apply time series to result fields](../image/formula-indic-default-ts.png)

In the resulting calculation, the formula is resolved for each day. Then the average of the result is taken for that day and the previous six days:

\(\(New P1/All newDay 1 \* 100\) + \(New P1/All newDay 2 \* 100\)+ … \(New P1/All newDay 7 \*100\)\) / 7

You aren't sure if you want the 7-day average of the final result or the average 7-day average of each indicator. So, you copy the previous formula indicator, with the same time series, but with **Apply time series to result** unchecked. Now, the time series is applied to the `Number of new incidents > Priority = 1 - Critical` and `Number of new incidents` contributing indicators separately before the formula is resolved:

\(New P1Day 1 + New P1Day 2 + … New P1Day 7\) / \(All newDay 1 + All newDay 2 + … All newDay 7\) \* 100

You plot both formula indicators in a time series widget to see the difference in outcome between the two settings. Because the default time series only applies on the Analytics Hub, you also add the 7d running AVG time series to the widget:![Same formula applied to same data, but with a time series applied to each contributing indicator versus a time series applied to the result](../image/formula-indic-ts-apply-result-vs-components.png)

**Parent Topic:**[Formula indicators](formula-indicators.md)

**Related topics**  


[Create a formula indicator](../task/t_CreateAFormulaIndicator.md)

[Get analytics methods in formulas](../task/get-indicator-analytics.md)

[Prevent a contributing indicator in a formula from following breakdowns](c_ExcludingBreakdownsFromFormulas.md)

[Breakdown matrices in formula indicators](bkdown-matrix-formula-indicators.md)

[Detect indicators with no scores in a formula](../task/detect-indicators-no-scores-formula.md)

[Indexing multiple indicators in a formula](index-indicators.md)

[Changes to score\_start/end because of different user time zones](time-zones-indicator-formulas.md)

[Applying time series aggregations](applying-time-series-aggregations.md#)

