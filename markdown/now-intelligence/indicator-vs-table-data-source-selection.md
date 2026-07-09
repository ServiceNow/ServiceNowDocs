---
title: Indicator vs Table data source selection
description: After you submit a query to AI Data Explorer, the system checks the query for information whether to use table or indicator data. If there is no such information, it falls back on a default set in a system property.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/now-intelligence/indicator-vs-table-data-source-selection.html
release: zurich
topic_type: concept
last_updated: "2026-06-23"
reading_time_minutes: 1
breadcrumb: [Questions and responses in an exploration, Use, AI Data Explorer, Now Assist in Platform Analytics, Platform Analytics]
---

# Indicator vs Table data source selection

After you submit a query to AI Data Explorer, the system checks the query for information whether to use table or indicator data. If there is no such information, it falls back on a default set in a system property.

Tables on the ServiceNow AI Platform® contain current data. To view trends in this data over time, you need an [indicator \(KPI\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/performance-analytics/performance-analytics-glossary.md). Indicators are calculated from table values that are collected over time.

**Important:** AI Data Explorer supports only [automated indicators](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/performance-analytics/performance-analytics-glossary.md). It does not support Performance Analytics indicator [targets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/performance-analytics/performance-analytics-glossary.md), [thresholds](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/performance-analytics/performance-analytics-glossary.md), or [forecasts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/performance-analytics/c_ForecastingData.md).

The system calculates which data source is appropriate for your query based on the following, in order of decreasing priority:

1.  Keywords
2.  Context, if present
3.  Fallback value in system property

Keywords in the query have the highest priority. To influence the choice, include the following keywords:

-   To use an indicator as the data source:
    -   indicator
    -   indicators
    -   KPI
    -   key performance indicator
-   To use a table as the data source:
    -   table
    -   list
    -   live data
    -   live query
    -   right now
    -   at this time
    -   this moment
    -   as of today

If your query is a follow-up question or launched from a data visualization, you already start with a context. If the system returns a successful result from the same source as the context, it keeps that source type. If the context has both an indicator and a table, the system goes with the more recent source type.

If the query does not show whether table or indicator data is preferred, the system uses the fallback source type defined in the system property **sn\_query\_gen.default\_source\_type**. The default value is `table`.

For indicator data sources, both automated and scripted breakdowns are supported, but only to two levels. If a query cannot be answered with fewer than three breakdowns, the system falls back to table data sources.

**Parent Topic:**[Questions and responses in an exploration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/ask-expl-questions.md)

