---
title: Changes to score\_start/end because of different user time zones
description: For formula indicators, the values of the variables score\_start and score\_end are calculated based on the time zone of the user who is executing the formula. If users in different time zones execute the same formula, the values of score\_start and score\_end change.
locale: en-US
release: xanadu
product: Performance Analytics
classification: performance-analytics
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Formula indicators, Performance Analytics indicators, Configuring fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Changes to score\_start/end because of different user time zones

For formula indicators, the values of the variables `score_start` and `score_end` are calculated based on the time zone of the user who is executing the formula. If users in different time zones execute the same formula, the values of `score_start` and `score_end` change.

**Warning:** The date value of the `score_start` and `score_end` variables can shift when users from different time zones view the same formula.

Formulas can include `score_start` or `score_end` variables as parameters for indicators that the formula references. These variables represent the first and last second of the specific collection period being calculated for the referenced indicator. The values of the `score_start` and `score_end` variables are calculated from the difference between the time zone of the user executing the formula and the time zone of the database server, which is GMT. A user executes a formula whenever they view the formula indicator in a dashboard widget or on the Analytics Hub. As a result, the date value of the start or end of the collection period can shift when different users view the same formula.

## Different values of score\_end for different user time zones

Consider a formula indicator with a daily frequency and the following formula:

```
pa.getScore($[[Number of open incidents]], score_end);
```

Three different users view a dashboard widget with this formula indicator on 18 October. The database server considers `score_end` for 18 October to be 23:59:59 GMT on 18 October.

-   One user is in the Europe/Berlin time zone. Their `score_end` value is "2019-10-18 21:59:59", and the score for the date 18 October is returned.
-   One user is in the US/Pacific time zone. Their `score_end` value is "2019-10-19 06:59:59", and the score for the date 19 October is returned.
-   One user is in the GMT time zone. Their `score_end` value matches the database server, "2019-10-18 23:59:59", and the score for the date 18 October is returned.

**Parent Topic:**[Formula indicators](formula-indicators.md)

**Related topics**  


[Create a formula indicator](../task/t_CreateAFormulaIndicator.md)

[Get analytics methods in formulas](../task/get-indicator-analytics.md)

[Prevent a contributing indicator in a formula from following breakdowns](c_ExcludingBreakdownsFromFormulas.md)

[Breakdown matrices in formula indicators](bkdown-matrix-formula-indicators.md)

[Applying time series to result or to contributing indicators](apply-time-series-result-components.md)

[Detect indicators with no scores in a formula](../task/detect-indicators-no-scores-formula.md)

[Indexing multiple indicators in a formula](index-indicators.md)

[Performance Analytics variables](pa-scripts.md#)

