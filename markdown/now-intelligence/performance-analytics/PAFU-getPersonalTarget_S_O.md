---
title: getPersonalTarget\(String indicator, Object onDate\)
description: Returns the personal target associated with the specified indicator for the specified date.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/performance-analytics/PAFU-getPersonalTarget\_S\_O.html
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: reference
last_updated: "2026-03-12"
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

**Parent Topic:**[PAFormulaUtils API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/PAFormulaUtils.md)

**Related topics**  


[getChange\(String indicator, Object fromDate, Object toDate\)]()

[getChangePercentage\(String indicator, Object fromDate, Object toDate\)]()

[getCurrentAggregateID\(\)]()

[getCurrentBreakdownID\(\)]()

[getCurrentBreakdownLevel2ID\(\)]()

[getCurrentElementID\(\)]()

[getCurrentElementLevel2ID\(\)]()

[getGap\(String indicator, Object onDate\)]()

[getGlobalTarget\(String indicator, Object onDate\)]()

[getScore\(String indicator, Object onDate\)]()

[PAFormulaUtils API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/PAFormulaUtils.md)

