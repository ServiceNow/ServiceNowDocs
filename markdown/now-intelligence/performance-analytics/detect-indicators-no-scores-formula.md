---
title: Detect indicators with no scores in a formula
description: As the formula creator, you can handle contributing indicators that have null scores. First set the formula indicator to calculate the formula even when it contains a null score.
locale: en-US
release: yokohama
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Formula indicators, Indicators, Configuring fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Detect indicators with no scores in a formula

As the formula creator, you can handle contributing indicators that have null scores. First set the formula indicator to calculate the formula even when it contains a null score.

## Before you begin

Role required: pa\_power\_user, admin

## About this task

The formulas in formula indicators typically contain one or more other indicators. If one of those indicators has no score, by default the formula is not calculated and the formula indicator returns no score. However, several use cases exist for identifying the indicator that has no score instead of having the formula indicator return null. First enable the formula to be calculated when an indicator in the formula has no score. Then you can assign a value to an indicator with no score.

## Procedure

1.  Open the formula indicator of interest.

2.  Select **Allow formula component to be null**.

3.  In the **Formula**, add an `if{} else {}` statement that ascribes a value to an indicator when it has no score.


## Field indicator with Allow formula component to be null

Consider the following formula indicators for a collection period when there are no closed incidents, so the indicator Number of closed incidents has no score.

Formula 1:

```
[[Number of open incidents]] / [[Number of closed incidents]]
```

Formula 2:

```

[[Formula 1]] + 23
```

Formula 3:

```

if ([[Formula 1]] == null) { 23 } else { 11 }
```

Formula 4:

```

[[Formula 2]] || 64
```

Formula 5:

```

(([[Formula 1]] == null && [[Formula 2]] == null) ? 11 : 18)
```

If **Allow formula component to be null** is not selected for any of the formula indicators, none of them have scores.

If **Allow formula component to be null** is selected for all of the formula indicators, they have the following scores:

-   Formula 1 = null
-   Formula 2 = 23
-   Formula 3 = 23
-   Formula 4 = 64
-   Formula 5 = 11

Formula 2, Formula 3, Formula 4, and Formula 5 represent four different ways to handle the null score.

**Parent Topic:**[Formula indicators](../concept/formula-indicators.md)

**Related topics**  


[Create a formula indicator](t_CreateAFormulaIndicator.md)

[Get analytics methods in formulas](get-indicator-analytics.md)

[Prevent a contributing indicator in a formula from following breakdowns](../concept/c_ExcludingBreakdownsFromFormulas.md)

[Breakdown matrices in formula indicators](../concept/bkdown-matrix-formula-indicators.md)

[Applying time series to result or to contributing indicators](../concept/apply-time-series-result-components.md)

[Indexing multiple indicators in a formula](../concept/index-indicators.md)

[Changes to score\_start/end because of different user time zones](../concept/time-zones-indicator-formulas.md)

