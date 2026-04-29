---
title: getGlobalTarget\(String indicator, Object onDate\)
description: Returns the global target associated with the specified indicator for the specified date.
locale: en-US
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [PAFormulaUtils API, Get analytics methods in formulas, Formula indicators, Indicators, Configure fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# getGlobalTarget\(String indicator, Object onDate\)

Returns the global target associated with the specified indicator for the specified date.

|Name|Type|Description|
|----|----|-----------|
|indicator|String|Unique identifier of the indicator.|
|onDate|Object|Date for which to return the global target.|

|Type|Description|
|----|-----------|
|Number|Global target for the specified date and indicator.|

Example:

```
pa.getGlobalTarget($[[% of open overdue incidents]],score_start);
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

[getPersonalTarget\(String indicator, Object onDate\)](PAFU-getPersonalTarget_S_O.md)

[getScore\(String indicator, Object onDate\)](PAFU-getScore_S_O.md)

[PAFormulaUtils API](../concept/PAFormulaUtils.md)

