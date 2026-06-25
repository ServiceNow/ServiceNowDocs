---
title: getCurrentAggregateID\(\)
description: Returns the time series aggregate identifier \(sys\_id\) from the indicator of the current formula. The sys\_id is returned dynamically, as the selection in the Analytics Hub changes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/performance-analytics/PAFU-getCurrentAggregateID.html
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [PAFormulaUtils API, Get analytics methods in formulas, Formula indicators, Indicators, Configure fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# getCurrentAggregateID\(\)

Returns the time series aggregate identifier \(sys\_id\) from the indicator of the current formula. The sys\_id is returned dynamically, as the selection in the Analytics Hub changes.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_wxf_2ml_ffb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

Dynamic time series aggregate ID from the indicator of the current formula as it changes with your selection in the Analytics Hub. If there is no time series aggregate ID, the method does not return a value.

</td></tr></tbody>
</table>Example:

```
var res = [[Number of open incidents]];
if(pa.getCurrentAggregateID() == '89ea4c11d7001100ba986f14ce6103dc')
  {
    res = 0;
  }
res;
```

**Parent Topic:**[PAFormulaUtils API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/PAFormulaUtils.md)

**Related topics**  


[getChange\(String indicator, Object fromDate, Object toDate\)]()

[getChangePercentage\(String indicator, Object fromDate, Object toDate\)]()

[getCurrentBreakdownID\(\)]()

[getCurrentBreakdownLevel2ID\(\)]()

[getCurrentElementID\(\)]()

[getCurrentElementLevel2ID\(\)]()

[getGap\(String indicator, Object onDate\)]()

[getGlobalTarget\(String indicator, Object onDate\)]()

[getPersonalTarget\(String indicator, Object onDate\)]()

[getScore\(String indicator, Object onDate\)]()

[PAFormulaUtils API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/PAFormulaUtils.md)

