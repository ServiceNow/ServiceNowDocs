---
title: Breakdown and indicator Performance Analytics properties
description: These properties set limits on breakdown elements and indicators, mostly in the context of visualizations.
locale: en-US
release: xanadu
product: Performance Analytics
classification: performance-analytics
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Performance Analytics properties, Performance Analytics reference, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Breakdown and indicator Performance Analytics properties

These properties set limits on breakdown elements and indicators, mostly in the context of visualizations.

<table id="table_i4n_swz_gbb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

com.snc.pa.scoresheet.max\_elements

</td><td>

Maximum number of [breakdown elements](../concept/performance-analytics-glossary.md#) of a breakdown that can be shown in a scoresheetDefault: 500

</td></tr><tr><td>

com.snc.pa.breakdown\_element\_cutoff

</td><td>

Maximum number of elements that a breakdown can have where the Analytics Hub and KPI Details show its scoreless elements.

 An element is scoreless when it meets one of these conditions:

-   For real-time scores, the element has never had a score.

-   For a formula indicator, the element has never had a score in one or more of the [contributing indicators](../concept/performance-analytics-glossary.md#).

-   For the collected scores of an automated indicator, the element has never had a score. However, if the number of elements that would still be displayed exceeds the **com.snc.pa.breakdown\_element\_cutoff** value, only the elements that have a score or change value on the selected date are displayed. For more information and examples, see [Collected scores and com.snc.pa.breakdown\_element\_cutoff](../concept/collected-element-display-cutoff.md).


 **Note:** This parameter does not affect whether unmatched elements are shown.

 Default: 50

</td></tr><tr><td>

com.snc.pa.scorecards.max\_breakdown\_elements

</td><td>

Maximum number of breakdown elements in Analytics Hub lists

 Default: 1000

 Maximum: 10,000. Any value set above 10,000 is treated as 10,000.

 **Tip:** If this value is not high enough for your indicators, consider redesigning your Performance Analytics solution.

</td></tr><tr><td>

com.snc.pa.scorecard.breakdown.chart.max\_rows

</td><td>

Number of breakdown elements in visualizationsDefault: 10

</td></tr><tr><td>

com.snc.pa.thresholds.frequency\_intervals\_in\_the\_past\_limit

</td><td>

Maximum number of frequency intervals in the past that a threshold check job analyzesDefault: 2

</td></tr><tr><td>

com.snc.pa.scorecard.max\_record\_num

</td><td>

Number of records to be loaded automatically on the records tab of the Analytics Hub for a single indicator. If the number of records exceeds the value of this property, records are not automatically loaded. In this case, the user is presented with a message and a button to load all records.

 Default: 50,000

</td></tr><tr><td>

com.snc.pa.breakdown\_element\_ui\_max\_records

</td><td>

Deprecated in Analytics Hub. Limit for the number of elements to be fetched for a breakdown. Used for the lookup fields \(breakdown dashboard, old detailed scorecard, and so on.\)

 Default: 100

</td></tr><tr><td>

com.snc.pa.target\_batch\_operation\_limit

</td><td>

Applies only to KPI Details: The maximum number of targets that can be inserted or updated in one bulk action on the Targets Configuration page. If you face timeouts while inserting or updating targets in bulk, consider reducing this limit.

 Default: 100

</td></tr><tr><td>

com.snc.pa.widget.max\_widget\_indicators

</td><td>

Maximum number of widget indicators, in addition to the main indicator that can be added to a widgetDefault: 7

</td></tr><tr><td>

com.snc.pa.widgets.respect\_acl

</td><td>

Restrict widget visibility following the ACLs of indicators and breakdowns. True\|false.-   Default on new instances: true
-   Default on upgraded instances from before Quebec: false

</td></tr></tbody>
</table>**Parent Topic:**[Performance Analytics properties](pa-properties.md)

