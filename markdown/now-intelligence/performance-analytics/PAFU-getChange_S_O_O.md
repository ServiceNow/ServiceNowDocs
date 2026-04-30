---
title: getChange\(String indicator, Object fromDate, Object toDate\)
description: Returns the change in the score of an indicator between two specified dates.
locale: en-US
release: xanadu
product: Performance Analytics
classification: performance-analytics
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [PAFormulaUtils API, Get analytics methods in formulas, Formula indicators, Performance Analytics indicators, Configuring fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# getChange\(String indicator, Object fromDate, Object toDate\)

Returns the change in the score of an indicator between two specified dates.

|Name|Type|Description|
|----|----|-----------|
|indicator|String|Unique identifier of the indicator for which to calculate the change.|
|fromDate|Object|Initial date of the comparison.|
|toDate|Object|End date of the comparison.|

|Type|Description|
|----|-----------|
|Number|Difference in the specified indicator score between the two dates.|

## Change from the beginning of the month to the last collection period

In this example, we have the indicator Number of open incidents, whose scores are collected daily. The fromDate parameter is the first second of the current month, constructed by taking the timestamp of the last collection period \(`score_start`\), extracting the year and the month from the timestamp, and appending the numeral 01 for the day. The toDate parameter is the timestamp of the beginning of the last collection period, which would be the first second of the previous day, depending on timezone differences.

```
pa.getChange($[[Number of open incidents]], new GlideDateTime(score_start.getYear() + '-' + score_start.getMonth() + '-01'), score_start);
```

**Parent Topic:**[PAFormulaUtils API](../concept/PAFormulaUtils.md)

**Related topics**  


[getChangePercentage\(String indicator, Object fromDate, Object toDate\)](PAFU-getChangePercentage_S_O_O.md)

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

