---
title: getCurrentBreakdownLevel2ID\(\)
description: Returns the level 2 breakdown identifier \(sys\_id\) from the indicator of the current formula. The sys\_id is returned dynamically, as the selection in the Analytics Hub changes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/performance-analytics/PAFU-getCurrentBreakdownLevel2ID.html
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [PAFormulaUtils API, Get analytics methods in formulas, Formula indicators, Indicators, Configure fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# getCurrentBreakdownLevel2ID\(\)

Returns the level 2 breakdown identifier \(sys\_id\) from the indicator of the current formula. The sys\_id is returned dynamically, as the selection in the Analytics Hub changes.

Use this method to obtain the sys\_id of the level 2 breakdown when altering the formula for a specific breakdown.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_kdn_jpm_mfb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

Dynamic level 2 breakdown ID from the indicator of the current formula as it changes with your selection in the Analytics Hub. If there is no level 2 breakdown ID, the method does not return a value.

</td></tr></tbody>
</table>Example:

```
var res = [[Number of open incidents]];
if(pa.getCurrentBreakdownLevel2ID() == 'baec0752bf130100b96dac808c0739ed' && pa.getCurrentElementLevel2ID() == '8a4dde73c6112278017a6a4baf547aa7')
  {
  res = 0;
  }
res;
```

**Parent Topic:**[PAFormulaUtils API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/PAFormulaUtils.md)

**Related topics**  


[getChange\(String indicator, Object fromDate, Object toDate\)]()

[getChangePercentage\(String indicator, Object fromDate, Object toDate\)]()

[getCurrentAggregateID\(\)]()

[getCurrentBreakdownID\(\)]()

[getCurrentElementID\(\)]()

[getCurrentElementLevel2ID\(\)]()

[getGap\(String indicator, Object onDate\)]()

[getGlobalTarget\(String indicator, Object onDate\)]()

[getPersonalTarget\(String indicator, Object onDate\)]()

[getScore\(String indicator, Object onDate\)]()

[PAFormulaUtils API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/PAFormulaUtils.md)

