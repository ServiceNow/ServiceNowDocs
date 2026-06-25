---
title: getScore\(String indicator, Object onDate\)
description: Returns the score of the specified indicator for the specified date.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/performance-analytics/PAFU-getScore\_S\_O.html
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [PAFormulaUtils API, Get analytics methods in formulas, Formula indicators, Indicators, Configure fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# getScore\(String indicator, Object onDate\)

Returns the score of the specified indicator for the specified date.

|Name|Type|Description|
|----|----|-----------|
|indicator|String|Unique identifier of the indicator whose score is to be retrieved.|
|onDate|Object|Date for which to return the score.|

|Type|Description|
|----|-----------|
|Number|Score for the specified date and indicator.|

Example:

```
pa.getScore($[[Number of open incidents]], score_end);
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

[getPersonalTarget\(String indicator, Object onDate\)]()

[PAFormulaUtils API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/PAFormulaUtils.md)

