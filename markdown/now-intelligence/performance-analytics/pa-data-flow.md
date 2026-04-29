---
title: Performance Analytics data flow
description: Before you get started with Performance Analytics, understand how the data flows through the platform, ultimately resulting in your ability to visualize process improvements.
locale: en-US
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Implement Performance Analytics, Explore, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Performance Analytics data flow

Before you get started with Performance Analytics, understand how the data flows through the platform, ultimately resulting in your ability to visualize process improvements.

1.  Daily business operations and interactions generate data and populate the respective business process tables.

    Example: Submitting a new incident creates a record in the Incident table.

2.  Active scheduled jobs run regularly to take periodic snapshots of process behavior. Each job calculates indicator \(KPI\) scores, based on metadata in PA indicators and breakdowns. Over time, this continuous stream of scores builds a trend.

    Example: A collection job counts the number of incidents in the Incident table daily. After one month, a trend containing about 30 data points can be viewed.

3.  Data snapshots and scores are stored in Performance Analytics data tables. These tables are the source of all Performance Analytics visualizations.
4.  Widgets present indicator scores in a specific format, such as a trend line or a bar chart.

    Example: The Number of new incidents is an indicator you may want to track. This indicator can be visualized as a single score or a trend of daily readings over time by configuring the appropriate widget.

5.  Multiple Performance Analytics widgets are presented in a single Dashboard view, allowing stakeholders to view all relevant business process information in a single place.

![Diagram showing the flow of data in Performance Analytics, from generation to consumption](../image/pa-data-flow.png "Data flow in Performance Analytics")

**Parent Topic:**[Implement Performance Analytics](implementing-pa.md)

