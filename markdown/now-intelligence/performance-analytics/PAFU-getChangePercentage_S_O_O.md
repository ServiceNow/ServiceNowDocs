---
title: getChangePercentage\(String indicator, Object fromDate, Object toDate\)
description: Returns the percentage of change in the score of an indicator between two specified dates.
locale: en-US
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [PAFormulaUtils API, Get analytics methods in formulas, Formula indicators, Indicators, Configure fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# getChangePercentage\(String indicator, Object fromDate, Object toDate\)

Returns the percentage of change in the score of an indicator between two specified dates.

|Name|Type|Description|
|----|----|-----------|
|indicator|String|Unique identifier of the indicator for which to calculate the percentage of change.|
|fromDate|Object|Initial date of the comparison.|
|toDate|Object|End date of the comparison|

|Type|Description|
|----|-----------|
|Number|Percent change of the specified indicator between the two specified dates.|

Example:

```
var lastPeriod = new GlideDateTime(score_start.getYear() + '-' + score_start.getMonth() + '-01');
lastPeriod.addDaysUTC(-1);
pa.getChangePercentage($[[Number of open incidents]], lastPeriod, score_start);
```

**Parent Topic:**[PAFormulaUtils API](../concept/PAFormulaUtils.md)

**Related topics**  


[getChange\(String indicator, Object fromDate, Object toDate\)](PAFU-getChange_S_O_O.md)

[getCurrentAggregateID\(\)](PAFU-getCurrentAggregateID.md)

[getCurrentBreakdownID\(\)](PAFU-getCurrentBreakdownID.md)

[getCurrentBreakdownLevel2ID\(\)](PAFU-getCurrentBreakdownLevel2ID.md)

[getCurrentElementID\(\)](PAFU-getCurrentElementID.md)

[getCurrentElementLevel2ID\(\)](PAFU-getCurrentElementLevel2ID.md)

[getGap\(String indicator, Object onDate\)](PAFU-getGap_S_O.md)

[getGlobalTarget\(String indicator, Object onDate\)](PAFU-getGlobalTarget_S_O.md)

[getPersonalTarget\(String indicator, Object onDate\)](PAFU-getPersonalTarget_S_O.md)

[getScore\(String indicator, Object onDate\)](PAFU-getScore_S_O.md)

[PAFormulaUtils API](../concept/PAFormulaUtils.md)

