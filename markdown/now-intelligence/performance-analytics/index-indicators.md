---
title: Indexing multiple indicators in a formula
description: You can write a formula to measure what the gap is to the overall target of multiple, combined indicators. Such a formula indicator is called an 'index indicator'.
locale: en-US
release: zurich
product: Performance Analytics
classification: performance-analytics
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Formula indicators, Indicators, Configure fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Indexing multiple indicators in a formula

You can write a formula to measure what the gap is to the overall target of multiple, combined indicators. Such a formula indicator is called an 'index indicator'.

The performance of processes, services, groups, and other business entities are often tracked and monitored using more than one indicator. When viewing and analyzing performance of these processes, business services, or workgroups, the overall picture can be confusing and ambiguous. For example:

-   Although the scores for three indicators improved somewhat, the scores for 2 of them are still below target and 1 is above target.
-   The score for one indicator remained more or less the same and is still below target.
-   The score for one indicator did significantly deteriorate, but is fortunately just above target.

Looking at this information, the answers to the following questions are not clear:

-   Is the overall performance of the process/service/group still at or above the desired level?
-   Did the overall performance improve?

An index indicator can answer these questions. With an index indicator, the scores of multiple indicators are aggregated into one score. It is a weighted average of several indicators. If the weighted sum of these indicators is improving, the calculated score of the index formula goes up. As with any other indicator, the index indicator shows if the score is good or not and if the score has improved or not.

The principle behind an index indicator is to calculate a score value indexed to 100 for each indicator. When you have these indexed scores, you are mathematically allowed to calculate an overall average of them.

To be included in an index indicator, an indicator must have a direction and a target. The basic formula to calculate the indexed score for an indicator that has a **Maximize** direction is:

```
100 + (((actual score - target) / target) * 100)
```

For indicators that have a **Minimize** direction, the formula is:

```
100 - (((actual score - target) / target) * 100)
```

If you are weighting the indicators evenly, you can index the final aggregation to 100 instead of indexing the individual indicators to 100.

You can use methods of the PAFormulaUtils\(\) API to get the gap between score and target for the indicator from the Analytics Hub. For more information, see [Get analytics methods in formulas](../task/get-indicator-analytics.md):

```
pa.getGap(indicator, On date) / pa.getGlobalTarget(indicator, On date)
```

Because of the different operator for the different direction, if the score of an underlying indicator is improving \(up or down\), the index indicator score is increasing. Therefore, always set the direction of the index indicator to **Maximize**.

If no target value is set for an indicator, use a norm value instead. Indicators that have a target or norm value equal to 0 cannot be used in the index indicator, because it would require dividing by 0.

Set a target of 100 for each index indicator. This target is the calculated, overall, indexed score if all underlying indicators have an actual score equal to their target or norm value.

An index indicator is measuring what the gap is to the overall target of multiple, combined indicators. It is measuring the 'Percentage of Target Achievement'.

## Index indicator using PAFormulaUtils\(\) methods

In the following example, you want a single index that aggregates the gap between score and global target for the following indicators:

-   The percentage of incidents that are overdue.
-   The average age of the last update of open incidents.
-   The total number of open incidents.

To get this single index, you follow these steps to produce an index indicator:

1.  You navigate to **Performance Analytics** &gt; **Formula Indicators** and click **New**. Index indicators are a use case of formula indicators.
2.  You give the indicator a meaningful name, such as **Aggregate incident gap**.
3.  Because you are creating an index indicator, you set the **Direction** to **Maximize**.
4.  In the **Formula** field, you use the **Browse for a method** and **Browse for an indicator** functions to create the following formula:

    ```
    var a = pa.getGap($[[% of open overdue incidents]], score_start) / pa.getGlobalTarget($[[% of open overdue incidents]],score_start);
    var b = pa.getGap($[[Average age of last update of open incidents]], score_start) / pa.getGlobalTarget($[[Average age of last update of open incidents]], score_start);
    var c = pa.getGap($[[Number of open incidents]], score_start) / pa.getGlobalTarget($[[Number of open incidents]], score_start);
    var res = 100 - (100 * (a + b + c) / 3);
    res;
    ```

    The three indicators are weighted equally, so the aggregation is indexed to 100 instead of the individual indicators.


**Parent Topic:**[Formula indicators](formula-indicators.md)

**Related topics**  


[Create a formula indicator](../task/t_CreateAFormulaIndicator.md)

[Get analytics methods in formulas](../task/get-indicator-analytics.md)

[Prevent a contributing indicator in a formula from following breakdowns](c_ExcludingBreakdownsFromFormulas.md)

[Breakdown matrices in formula indicators](bkdown-matrix-formula-indicators.md)

[Applying time series to result or to contributing indicators](apply-time-series-result-components.md)

[Detect indicators with no scores in a formula](../task/detect-indicators-no-scores-formula.md)

[Changes to score\_start/end because of different user time zones](time-zones-indicator-formulas.md)

