---
title: KPI Details
description: KPI Details is an exploratory view of indicators, used for more detailed analysis. It lets you see trends, predictions, breakdowns, and associated records for a specific indicator. The KPI Details page enables you to delve into the information behind your key performance indicators.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Platform Analytics]
---

# KPI Details

KPI Details is an exploratory view of indicators, used for more detailed analysis. It lets you see trends, predictions, breakdowns, and associated records for a specific indicator. The KPI Details page enables you to delve into the information behind your key performance indicators.

KPI Details lets you answer questions such as:

-   “Are daily new critical incidents rising since the last update?”
-   “Is the rise in critical incidents faster than the rise in P3 incidents?”
-   “What are the top 3 groups with the highest increase in critical incidents over the past quarter?”
-   “What specific incidents correspond to that spike in incidents last week?”
-   “What’s my usual \(median/ average/ total\) number of new incidents over the past 3 weeks? Past 2 months?”

Learn how to use KPI Details to accomplish the following tasks:

-   [Review the overall health of an indicator](../reference/chart-options.md).
-   [Explore trends for any indicator](../reference/kpi-details-components.md).
-   [Review individual records corresponding to any date](show-compare-edit-records.md#).
-   Manage [targets](kpi-details-targets.md) and [thresholds](kpi-details-thresholds.md#) for your indicators.

Enhance KPI Details by configuring notifications of significant trends in [KPI Signals](process-behavior-charts-for-kpis.md).

**Tip:** A free training for KPI Details is available from the [NOW Learning Center](https://nowlearning.service-now.com/lxp?id=overview&sys_id=5c6c5f8687963c14ed3b74c9cebb3514&type=course).

**Note:** Values between 10,000 and 999,999 are rounded off to the nearest thousand and abbreviated with a K, such as 11K for 11,234. Values between 1 million and 999,999,999 are rounded off to the nearest million and abbreviated with an M. Values of 1 billion and higher are rounded off to the nearest billion and abbreviated with a G.

-   **[View KPI Details](../../performance-analytics/task/view-kpi-details.md)**  
From a list of indicators, select an indicator to open its KPI Details page.
-   **[Examining indicators with KPI Details](../reference/kpi-details-components.md)**  
The KPI Details feature enables you to delve into the information behind your key performance indicators. Apply forecasts, trends, targets, and thresholds. Filter by breakdown element or apply time series aggregations.
-   **[Indicator targets in KPI Details](kpi-details-targets.md)**  
Targets are goals your organization wants to achieve. They show the difference between the desired and actual scores of an indicator on a certain date.
-   **[Indicator thresholds in KPI Details](kpi-details-thresholds.md#)**  
Thresholds define a normal range of scores for an indicator and alert you when certain events occurs, like when a score reaches an all-time high.
-   **[KPI Details Performance Analytics properties](../reference/kpi-details-pa-properties.md)**  
KPI Details supports several Performance Analytics properties. These system properties control the behavior of Performance Analytics elements in the context of KPI Details.
-   **[KPI Details UUIDs](kpi-details-uuids.md)**  
Every combination of breakdowns, elements, a time series aggregation, and a domain that you specify for an indicator has a unique identifier \(UUID\). To understand how the KPI Details and KPI Signals applications work, you should understand how these UUIDs are constructed.

**Parent Topic:**[Platform Analytics](../../performance-analytics/concept/c_performanceAnalyticsAndReporting.md)

