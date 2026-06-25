---
title: Performance Analytics indicators
description: Indicators \(KPIs\) define a performance measurement taken at regular intervals of a business service, an activity, or organizational behavior. These performance measurements result in a series of indicator scores over time.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/performance-analytics/c\_Indicators.html
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Performance Analytics indicators

Indicators \(KPIs\) define a performance measurement taken at regular intervals of a business service, an activity, or organizational behavior. These performance measurements result in a series of indicator scores over time.

\[Omitted video\] Description: Creating your first indicator

Watch this six-minute video to learn more about the different kinds of indicators and how to create them.

Key characteristics of indicators include:

-   Indicator scores can be generated automatically from a set of records defined in an [indicator source](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/performance-analytics-glossary.md), entered manually, or calculated from other indicators.
-   Indicator scores can be viewed or analyzed in Platform Analytics data visualizations and KPI Details. In the Core UI, view them in the Analytics Hub or in widgets on dashboards.

Indicators that are based directly on indicator sources are the most common type of indicator. These indicators are named automated indicators. Indicators that are calculated in a formula from the scores of other indicators are called formula indicators. Indicators whose scores are entered manually are called manual indicators. Manual indicators are meant to be used primarily for testing purposes. Lastly, as an advanced feature, you can create an indicator from an external data source.

In addition there are Data snapshots indicators. Data snapshots in Platform Analytics allows for multiple breakdowns while analyzing your indicators \(KPIs\). For more information, see [Data snapshots and multiple breakdowns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/multi-level-breakdowns.md).

For an example of an indicator, see the Number of open incidents automated indicator that is provided in the base system. This indicator measures the number of incidents that are open each day and saves these numbers over time. You can examine its indicator scores in KPI Details or the Core UI Analytics Hub. If you have the pa\_power\_user role, you can see the indicator record under Automated indicators and navigate from that record to the indicator source.

**Related topics**  


[Automated indicators](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/automated-indicators.md)

[Formula indicators](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/formula-indicators.md)

[Manual indicators](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/t_CreateAManualIndicator.md)

[Using Performance Analytics with external data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/pa-external-data.md)

