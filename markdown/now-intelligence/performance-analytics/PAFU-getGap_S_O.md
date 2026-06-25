---
title: getGap\(String indicator, Object onDate\)
description: Returns the global target gap for the specified indicator on the specified date.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/performance-analytics/PAFU-getGap\_S\_O.html
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [PAFormulaUtils API, Get analytics methods in formulas, Formula indicators, Indicators, Configure fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# getGap\(String indicator, Object onDate\)

Returns the global target gap for the specified indicator on the specified date.

The gap is the difference between the score on the specified date and the target. For an indicator with the MAXIMIZE direction, the gap is calculated as the score minus the target. For an indicator with the MINIMIZE direction or no direction, the gap is calculated as the target minus the score.

|Name|Type|Description|
|----|----|-----------|
|indicator|String|Unique identifier of the indicator for which to provide the gap information.|
|onDate|Object|Date of the score to use to compare against the target score.|

|Type|Description|
|----|-----------|
|Number|Difference between the score on the specified date and the global target score.|

Example:

```
var a = pa.getGap($[[% of open overdue incidents]], score_start) / pa.getGlobalTarget($[[% of open overdue incidents]],score_start);
var b = pa.getGap($[[Average age of last update of open incidents]], score_start) / pa.getGlobalTarget($[[Average age of last update of open incidents]], score_start);
var c = pa.getGap($[[Number of open incidents]], score_start) / pa.getGlobalTarget($[[Number of open incidents]], score_start);
var res = 100 - (100 * (a + b + c) / 3);
res;
```

**Parent Topic:**[PAFormulaUtils API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/PAFormulaUtils.md)

**Related topics**  


[getChange\(String indicator, Object fromDate, Object toDate\)]()

[getChangePercentage\(String indicator, Object fromDate, Object toDate\)]()

[getCurrentAggregateID\(\)]()

[getCurrentBreakdownID\(\)]()

[getCurrentBreakdownLevel2ID\(\)]()

[getCurrentElementID\(\)]()

[getCurrentElementLevel2ID\(\)]()

[getGlobalTarget\(String indicator, Object onDate\)]()

[getPersonalTarget\(String indicator, Object onDate\)]()

[getScore\(String indicator, Object onDate\)]()

[PAFormulaUtils API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/PAFormulaUtils.md)

