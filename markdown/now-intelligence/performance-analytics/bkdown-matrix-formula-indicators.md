---
title: Breakdown matrices in formula indicators
description: Formula indicators inherit breakdown matrices from indicators in the formula.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/performance-analytics/bkdown-matrix-formula-indicators.html
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Formula indicators, Indicators, Configure fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Breakdown matrices in formula indicators

Formula indicators inherit breakdown matrices from indicators in the formula.

If all the indicators in the formula collect breakdown matrices, second-level breakdowns are available for the formula indicator. If none of the indicators in the formula collects breakdown matrices, second-level breakdowns are not available for the formula indicator. If only some of the indicators in the formula collect breakdown matrices, only those indicators can be broken down at a second level.

## Formula with two contributing indicators where breakdown matrices are calculated for one or both indicators

Consider the case when breakdown matrices are collected for the indicators 'Summed age of open incidents' and 'Number of open incidents.' You now create an indicator with the following formula:

```
[[Summed age of open incidents]]/[[Number of open incidents]]/24
```

On a particular day, the score for this formula indicator is 170, calculated as follows:

```
Summed age of open incidents with Category = Software and Priority = 2: 8,152 hours
Number of open incidents with Category = Software and Priority = 2: 2
Formula: 8152/2/24=170
```

What if the breakdown matrix is calculated only for 'Summed age of open incidents'? In this case, the 'Number of open incidents' is broken down only by Category and not by Priority. The score for the same formula indicator on the same day is 11, calculated as follows:

```
Summed age of open incidents with Category = Software and Priority = 2: 8,152 hours
Number of open incidents with Category = Software: 31
Formula: 8152/31/24=11
```

**Parent Topic:**[Formula indicators](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/formula-indicators.md)

**Related topics**  


[Create a formula indicator]()

[Get analytics methods in formulas]()

[Prevent a contributing indicator in a formula from following breakdowns]()

[Applying time series to result or to contributing indicators]()

[Detect indicators with no scores in a formula]()

[Indexing multiple indicators in a formula]()

[Changes to score\_start/end because of different user time zones]()

