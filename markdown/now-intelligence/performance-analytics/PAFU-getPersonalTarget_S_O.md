---
title: getPersonalTarget\(String indicator, Object onDate\)
description: Returns the personal target associated with the specified indicator for the specified date.
locale: en-US
release: zurich
product: Performance Analytics
classification: performance-analytics
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [PAFormulaUtils API, Get analytics methods in formulas, Formula indicators, Indicators, Configure fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# getPersonalTarget\(String indicator, Object onDate\)

Returns the personal target associated with the specified indicator for the specified date.

Use this method to obtain a personal index score. "Personal" refers to the active user who is looking at the Analytics Hub.

|Name|Type|Description|
|----|----|-----------|
|indicator|String|Unique identifier of the indicator.|
|onDate|Object|Date for which to return the personal target.|

|Type|Description|
|----|-----------|
|Number|Personal target for the specified date and indicator.|

Example:

```
var a = pa.getGap($[[% of open overdue incidents]], score_start) / pa.getPersonalTarget($[[% of open overdue incidents]],score_start);
var b = pa.getGap($[[Average age of last update of open incidents]], score_start) / pa.getPersonalTarget($[[Average age of last update of open incidents]], score_start);
var c = pa.getGap($[[Number of open incidents]], score_start) / pa.getPersonalTarget($[[Number of open incidents]], score_start);
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

[getGap\(String indicator, Object onDate\)](PAFU-getGap_S_O.md)

[getGlobalTarget\(String indicator, Object onDate\)](PAFU-getGlobalTarget_S_O.md)

[getScore\(String indicator, Object onDate\)](PAFU-getScore_S_O.md)

[PAFormulaUtils API](../concept/PAFormulaUtils.md)

