---
title: getGap\(String indicator, Object onDate\)
description: Returns the global target gap for the specified indicator on the specified date.
locale: en-US
release: zurich
product: Performance Analytics
classification: performance-analytics
topic_type: reference
last_updated: "2025-07-31"
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

**Parent Topic:**[PAFormulaUtils API](../concept/PAFormulaUtils.md)

**Related topics**  


[getChange\(String indicator, Object fromDate, Object toDate\)](PAFU-getChange_S_O_O.md)

[getChangePercentage\(String indicator, Object fromDate, Object toDate\)](PAFU-getChangePercentage_S_O_O.md)

[getCurrentAggregateID\(\)](PAFU-getCurrentAggregateID.md)

[getCurrentBreakdownID\(\)](PAFU-getCurrentBreakdownID.md)

[getCurrentBreakdownLevel2ID\(\)](PAFU-getCurrentBreakdownLevel2ID.md)

[getCurrentElementID\(\)](PAFU-getCurrentElementID.md)

[getCurrentElementLevel2ID\(\)](PAFU-getCurrentElementLevel2ID.md)

[getGlobalTarget\(String indicator, Object onDate\)](PAFU-getGlobalTarget_S_O.md)

[getPersonalTarget\(String indicator, Object onDate\)](PAFU-getPersonalTarget_S_O.md)

[getScore\(String indicator, Object onDate\)](PAFU-getScore_S_O.md)

[PAFormulaUtils API](../concept/PAFormulaUtils.md)

