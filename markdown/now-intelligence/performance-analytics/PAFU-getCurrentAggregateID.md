---
title: getCurrentAggregateID\(\)
description: Returns the time series aggregate identifier \(sys\_id\) from the indicator of the current formula. The sys\_id is returned dynamically, as the selection in the Analytics Hub changes.
locale: en-US
release: yokohama
product: Performance Analytics
classification: performance-analytics
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [PAFormulaUtils API, Get analytics methods in formulas, Formula indicators, Indicators, Configuring fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
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

**Parent Topic:**[PAFormulaUtils API](../concept/PAFormulaUtils.md)

**Related topics**  


[getChange\(String indicator, Object fromDate, Object toDate\)](PAFU-getChange_S_O_O.md)

[getChangePercentage\(String indicator, Object fromDate, Object toDate\)](PAFU-getChangePercentage_S_O_O.md)

[getCurrentBreakdownID\(\)](PAFU-getCurrentBreakdownID.md)

[getCurrentBreakdownLevel2ID\(\)](PAFU-getCurrentBreakdownLevel2ID.md)

[getCurrentElementID\(\)](PAFU-getCurrentElementID.md)

[getCurrentElementLevel2ID\(\)](PAFU-getCurrentElementLevel2ID.md)

[getGap\(String indicator, Object onDate\)](PAFU-getGap_S_O.md)

[getGlobalTarget\(String indicator, Object onDate\)](PAFU-getGlobalTarget_S_O.md)

[getPersonalTarget\(String indicator, Object onDate\)](PAFU-getPersonalTarget_S_O.md)

[getScore\(String indicator, Object onDate\)](PAFU-getScore_S_O.md)

[PAFormulaUtils API](../concept/PAFormulaUtils.md)

