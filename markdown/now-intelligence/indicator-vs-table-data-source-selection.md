---
title: Indicator vs Table data source selection
description: After you submit a query to AI Data Explorer, the system checks the query for specific keywords that indicator whether to use table or indicator data. If there are no such keywords, it falls back on a default set in a system property.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/now-intelligence/indicator-vs-table-data-source-selection.html
release: zurich
topic_type: concept
last_updated: "2026-09-08"
reading_time_minutes: 3
keywords: [formula indicator, automated indicator, data source selection]
breadcrumb: [Questions and responses in an exploration, Use, AI Data Explorer, ServiceNow Otto for Platform Analytics, Platform Analytics]
---

# Indicator vs Table data source selection

After you submit a query to AI Data Explorer, the system checks the query for specific keywords that indicator whether to use table or indicator data. If there are no such keywords, it falls back on a default set in a system property.

Tables on the ServiceNow AI Platform® contain current data. To view trends in this data over time, you need an [indicator \(KPI\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/performance-analytics/performance-analytics-glossary.md). Indicators are calculated from table values that are collected over time.

**Important:** AI Data Explorer supports [automated indicators](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/performance-analytics/performance-analytics-glossary.md)and [formula indicators](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/performance-analytics/performance-analytics-glossary.md). It does not support manual or external indicators, [targets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/performance-analytics/performance-analytics-glossary.md), [thresholds](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/performance-analytics/performance-analytics-glossary.md), or [forecasts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/performance-analytics/performance-analytics-glossary.md). Benchmarking indicators are excluded from indicator search results, whether the benchmarking indicator is itself automated or is a contributor within a formula indicator.

The system searches your query for the following content to determine the appropriate data source type:

1.  Keywords
2.  Context, if present

If the query does not show whether table or indicator data is preferred, and there is no context, the system responds differently depending on whether AI Data Explorer is agentic. If AI Data Explorer is non-agentic, the system uses the fallback source type defined in the system property **sn\_query\_gen.default\_source\_type**. The default value is `table`. If AI Data Explorer is agentic, the agent uses textual clues to determine which data source type to use. Table data is the default.

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

If your current context is an indicator, the following follow-up questions cause the context to switch to a table data source:

-   Asking for record-level data
-   Asking for live values
-   Asking for more than 2 breakdowns, such as asking for a third breakdown in a follow-up question
-   Asking for a date range the indicator does not have

When the context switches from an indicator to a table, the system converts it to the table, conditions, and aggregate field of its [contributing indicators](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/view-formula-components.md). The context is not dropped, and neither is the formula passed through unconverted.

For indicator data sources, both automated and scripted breakdowns are supported, but only to two levels. If a query cannot be answered with fewer than three breakdowns, the system falls back to table data sources.

An indicator's support for combining more than one breakdown element in a single result depends on the indicator type. For a formula indicator, this depends on whether **Allow aggregation of multiple breakdown element scores** is selected on the indicator record. All contributing indicators must also support score aggregation. For an automated indicator, aggregate score support depends on the indicator's aggregate: Count and Sum support combining multiple breakdown elements, while Average and Count Distinct do not. If the matched indicator does not support combining the requested breakdown elements, the system uses only one of the requested elements to generate the result. It then notifies you that the result reflects a single breakdown element instead of the full combination you requested.

**Parent Topic:**[Questions and responses in an exploration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/ask-expl-questions.md)

**Related topics**  


[Create a Formula Indicator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/performance-analytics/t_CreateAFormulaIndicator.md)

[Create an automated indicator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/performance-analytics/t_CreateAnAutomatedIndicator.md)

