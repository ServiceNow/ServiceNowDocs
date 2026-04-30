---
title: Formula indicators
description: Formula indicators use data from other indicators to calculate new metrics.
locale: en-US
release: yokohama
product: Performance Analytics
classification: performance-analytics
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Indicators, Configuring fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Formula indicators

Formula indicators use data from other indicators to calculate new metrics.

Unlike automated indicators, formula indicators are not based on an indicator source that is populated during data collection. The score of a formula indicator is calculated from a mathematical statement that includes data from one or more other indicators. This data can be the score of an indicator or a PAFormulaUtils\(\) calculated value for the indicator. For example, a formula can include the gap, or difference, between the score of an indicator and the indicator target value set in the Analytics Hub or KPI Details.

**Important:** Formula indicator scores are calculated when a user views the indicator on a dashboard or in KPI Details or the Analytics Hub.

Create a formula indicator in these cases:

-   To calculate a score from multiple indicators, such as the average of two indicators.
-   To extract a calculated value of an indicator from the PAFormulaUtils\(\) API and perform operations on that value.
-   To measure the gap to the overall target of multiple, combined indicators \(an index indicator\).

**Tip:** Training is available for creating and using formula indicators. See the course [Formula Indicators Overview](https://learning.servicenow.com/lxp/en/now-intelligence/formula-indicators-overview?id=learning_course_prev&course_id=11419783871cb1105aa9ca2d0ebb35b3) in the NOW Learning Center.

-   **[Create a formula indicator](../task/t_CreateAFormulaIndicator.md)**  
Create a formula indicator to produce a new computed score from one or more other indicators. Besides indicator scores, the formula can include calculations such as the gap between an indicator score and the indicator target.
-   **[Get analytics methods in formulas](../task/get-indicator-analytics.md)**  
To insert a calculated value from the Analytics Hub into a formula, use a method in the formula.
-   **[Prevent a contributing indicator in a formula from following breakdowns](c_ExcludingBreakdownsFromFormulas.md)**  
You can select contributing indicators in a formula to not be broken down. When a user applies a breakdown to the formula indicator, the breakdown does not apply to these indicators.
-   **[Breakdown matrices in formula indicators](bkdown-matrix-formula-indicators.md)**  
Formula indicators inherit breakdown matrices from indicators in the formula.
-   **[Applying time series to result or to contributing indicators](apply-time-series-result-components.md)**  
For a formula indicator, a time series aggregation can apply either to each indicator in the formula individually or to the formula result.
-   **[Detect indicators with no scores in a formula](../task/detect-indicators-no-scores-formula.md)**  
As the formula creator, you can handle contributing indicators that have null scores. First set the formula indicator to calculate the formula even when it contains a null score.
-   **[Indexing multiple indicators in a formula](index-indicators.md)**  
You can write a formula to measure what the gap is to the overall target of multiple, combined indicators. Such a formula indicator is called an 'index indicator'.
-   **[Changes to score\_start/end because of different user time zones](time-zones-indicator-formulas.md)**  
For formula indicators, the values of the variables `score_start` and `score_end` are calculated based on the time zone of the user who is executing the formula. If users in different time zones execute the same formula, the values of `score_start` and `score_end` change.

**Parent Topic:**[Performance Analytics indicators](c_Indicators.md)

