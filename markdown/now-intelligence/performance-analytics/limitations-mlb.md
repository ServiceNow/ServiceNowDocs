---
title: Limitations and requirements for Data snapshots
description: Several features of indicators and breakdowns are not supported with Data snapshots and multiple breakdowns.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/performance-analytics/limitations-mlb.html
release: brazil
product: Performance Analytics
classification: performance-analytics
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Data snapshots and multiple breakdowns, Configure fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Limitations and requirements for Data snapshots

Several features of indicators and breakdowns are not supported with Data snapshots and multiple breakdowns.

## Instance-level limitations

|Limitation or unsupported feature|Notes|
|---------------------------------|-----|
|Database requirements|Only instances with the [RaptorDB Professional \(PostgreSQL\) database](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/raptordb.md) are supported, not Oracle or MariaDB/MySQL. \(Checked when plugin is activated.\)|
|Domain separation|Domain-separated instances are not supported.|

Instances with RaptorDB Professional have the Data Snapshots \(com.snc.pa.mlb\) plugin installed automatically. If the instance is domain separated, the Data snapshots feature is turned off.

## Table-level limitations

|Limitation or unsupported feature|Notes|
|---------------------------------|-----|
|System tables|System tables \(named `sys_*`\) are not supported.|
|Benchmarking indicators|Not supported|

## Indicator- and breakdown-level limitations

<table id="table_indicator-limitations"><thead><tr><th>

Limitation or unsupported feature

</th><th>

Notes

</th></tr></thead><tbody><tr><td>

Benchmarking indicators

</td><td>

Not supported

</td></tr><tr><td>

Indicators with no conditions

</td><td>

Not supported

</td></tr><tr><td>

Scripted breakdown mappings/aggregations

</td><td>

Not supported

</td></tr><tr><td>

Breakdowns/aggregations on string and numeric type fields are not supported

</td><td>

The same limitations apply as with classic Performance Analytics breakdowns and indicators: Breakdowns on Choice fields that are strings or integers are supported. Only purely string and numeric fields are not supported. For example, a breakdown on Incident.Category would be supported because Category is a Choice field. A breakdown on Short Description would not be supported, because that is purely a string.

</td></tr><tr><td>

Only some query operators are supported

</td><td>

Unsupported operators for each field type on the source:-   Boolean/ChoiceTable/Reference: ISEMPTYSTRING
-   SysClassName: INSTANCEOF
-   String: MATCH\_PAT and MATCH\_RGX
-   Currency: NOT\_EQUALS, LESS\_THAN, GREATER\_THAN, LESS\_THAN\_OR\_EQUALS, GREATER\_THAN\_OR\_EQUALS, BETWEEN, EQUALS
-   Relative Dates: LESS\_THAN, LESS\_THAN\_EQ, GREATER\_THAN, GREATER\_THAN\_EQ, BETWEEN

</td></tr><tr><td>

Formula indicators

</td><td>

All [contributing indicators](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/performance-analytics/performance-analytics-glossary.md) must support Data snapshots.

</td></tr><tr><td>

Formula methods

</td><td>

Formula indicators that use methods in their formulas are not supported.

</td></tr><tr><td>

Manual or external indicators or breakdowns

</td><td>

Only [automated indicators](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/performance-analytics/performance-analytics-glossary.md), [formula indicators](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/performance-analytics/performance-analytics-glossary.md), and [automated breakdowns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/performance-analytics/performance-analytics-glossary.md) are supported. All contributing indicators in a formula indicator must be supported for the formula indicator to be supported.

</td></tr><tr><td>

Indicators based on [database views](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/performance-analytics/performance-analytics-glossary.md)

</td><td>

Only supported when the join conditions do not include fields other than sys\_id.

</td></tr><tr><td>

Database view prefix limitations

</td><td>

If the indicator source is a database view and there is an uppercase character in the database view prefix, the indicator is not supported. Also, if the two tables in the database view have the same prefix, the indicator is not supported.

</td></tr><tr><td>

Indicators with more than 250 breakdown/aggregation fields

</td><td>

Only 250 levels of breakdown are supported.

</td></tr><tr><td>

Converted indicators whose collection jobs have more than one timezone

</td><td>

If the indicator time zone and the source time zone do not match, the source time zone is used. If possible, an All Activity source is used, thus supporting intraday data collection.

</td></tr><tr><td>

Historical processing

</td><td>

Only data collected after the enablement date is supported. Attempts to apply more than two levels of breakdown to older data do not return any results.

</td></tr><tr><td>

Breakdown matrices

</td><td>

Not applicable. All breakdown combinations are supported by design.

</td></tr><tr><td>

Collection periods set on data collector

</td><td>

All collections are daily or intraday, depending on the Data snapshots source.

</td></tr></tbody>
</table>## Field-level limitations \(Indicator, breakdown, source, and data collector fields\)

|Limitation or unsupported feature|Notes|
|---------------------------------|-----|
|Label for unmatched|The **Label for unmatched** option on breakdown sources is ignored with Data snapshots.|
|Value when nil|The **Value when nil** option on automated indicators is ignored with Data snapshots.|
|Security type|Data snapshots does not support the security type defined in the breakdown source.|
|Data collection job settings|Start/end periods, specific time configurations, and other settings do not affect Data snapshots. All data collection is daily. Only the timezone set on the data collection record has an effect.|
|Bucket groups|Not supported|
|Related list conditions|Related list conditions do not apply with Data snapshots|
|Targets and Thresholds|Support only up to two filters.|
|KPI Signals|Support only one filter.|
|Indicator scorecard visualizations|Support only up to two filters.|
|Scoresheets|Manual changes to scoresheets for indicators that are enabled for Data snapshots have no effect.|
|String fields in indicator or source conditions|4000-character limit|

**Parent Topic:**[Data snapshots and multiple breakdowns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/performance-analytics/multi-level-breakdowns.md)

