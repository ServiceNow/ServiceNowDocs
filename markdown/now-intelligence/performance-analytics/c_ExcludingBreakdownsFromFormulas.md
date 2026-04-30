---
title: Prevent a contributing indicator in a formula from following breakdowns
description: You can select contributing indicators in a formula to not be broken down. When a user applies a breakdown to the formula indicator, the breakdown does not apply to these indicators.
locale: en-US
release: zurich
product: Performance Analytics
classification: performance-analytics
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Formula indicators, Indicators, Configure fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Prevent a contributing indicator in a formula from following breakdowns

You can select contributing indicators in a formula to not be broken down. When a user applies a breakdown to the formula indicator, the breakdown does not apply to these indicators.

When you apply a breakdown to a [formula indicator](performance-analytics-glossary.md#), such as on a breakdown dashboard, the breakdown applies to all [contributing indicators](performance-analytics-glossary.md#). You prevent a contributing indicator from being broken down using the syntax \{\{Indicator\}\}. You can also prevent a contributing indicator from following breakdowns by clearing the **Allow breakdowns** check box in the **Browse for an indicator** dialog. This dialog opens when you create

For example, consider the formula `[[Incidents]] / [[Customers]]`. If you apply a region breakdown to this indicator, and specify EU as the breakdown element, the formula indicator returns scores using the formula `[[Incidents > region = eu]] / [[Customers > region = eu]]`. However, to view the EU incidents divided by the total number of incidents across all regions, you can write the formula as `[[Incidents]] / {{Customers}}`. Using the \{\{Indicator\}\} format causes the Customers indicator to ignore breakdowns. This way, when you apply the region breakdown with the EU breakdown element, this formula indicator is equivalent to the formula `[[Incidents > region = eu]] / [[Customers]]`.

You can still specify a breakdown and element for a contributing indicator that does not follow breakdowns for the whole formula indicator. Consider the formula `[[Incidents]] / {{Customers > importance = high}}`. In this example, the formula denominator is always broken down to include only the high-importance customers. Any breakdown applied to the formula indicator, such as the region breakdown, does not apply to the Customers indicator.

**Parent Topic:**[Formula indicators](formula-indicators.md)

**Related topics**  


[Create a formula indicator](../task/t_CreateAFormulaIndicator.md)

[Get analytics methods in formulas](../task/get-indicator-analytics.md)

[Breakdown matrices in formula indicators](bkdown-matrix-formula-indicators.md)

[Applying time series to result or to contributing indicators](apply-time-series-result-components.md)

[Detect indicators with no scores in a formula](../task/detect-indicators-no-scores-formula.md)

[Indexing multiple indicators in a formula](index-indicators.md)

[Changes to score\_start/end because of different user time zones](time-zones-indicator-formulas.md)

