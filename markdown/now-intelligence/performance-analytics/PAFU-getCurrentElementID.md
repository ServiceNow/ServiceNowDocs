---
title: getCurrentElementID\(\)
description: Returns the level 1 breakdown element identifier \(sys\_id\) from the indicator of the current formula. The sys\_id is returned dynamically, as the selection in the Analytics Hub changes.
locale: en-US
release: xanadu
product: Performance Analytics
classification: performance-analytics
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [PAFormulaUtils API, Get analytics methods in formulas, Formula indicators, Performance Analytics indicators, Configuring fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# getCurrentElementID\(\)

Returns the level 1 breakdown element identifier \(sys\_id\) from the indicator of the current formula. The sys\_id is returned dynamically, as the selection in the Analytics Hub changes.

Use this method when altering a formula for a specific element. For example, use the method when running a query to count different attributes, such as excluding scores for changes from groups that do not change.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_txf_htl_mfb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

Dynamic level 1 breakdown element ID from the indicator of the current formula as it changes with your selection in the Analytics Hub. If there is no level 1 breakdown element ID, the method does not return a value.

</td></tr></tbody>
</table>Example:

```
var res = [[Number of open incidents]];
if(pa.getCurrentBreakdownID() == 'baec0752bf130100b96dac808c0739ed' && pa.getCurrentElementID() == '8a4dde73c6112278017a6a4baf547aa7')
  {
  res = 0;
  }
res;
```

**Parent Topic:**[PAFormulaUtils API](../concept/PAFormulaUtils.md)

**Related topics**  


[getChange\(String indicator, Object fromDate, Object toDate\)](PAFU-getChange_S_O_O.md)

[getChangePercentage\(String indicator, Object fromDate, Object toDate\)](PAFU-getChangePercentage_S_O_O.md)

[getCurrentAggregateID\(\)](PAFU-getCurrentAggregateID.md)

[getCurrentBreakdownID\(\)](PAFU-getCurrentBreakdownID.md)

[getCurrentBreakdownLevel2ID\(\)](PAFU-getCurrentBreakdownLevel2ID.md)

[getCurrentElementLevel2ID\(\)](PAFU-getCurrentElementLevel2ID.md)

[getGap\(String indicator, Object onDate\)](PAFU-getGap_S_O.md)

[getGlobalTarget\(String indicator, Object onDate\)](PAFU-getGlobalTarget_S_O.md)

[getPersonalTarget\(String indicator, Object onDate\)](PAFU-getPersonalTarget_S_O.md)

[getScore\(String indicator, Object onDate\)](PAFU-getScore_S_O.md)

[PAFormulaUtils API](../concept/PAFormulaUtils.md)

