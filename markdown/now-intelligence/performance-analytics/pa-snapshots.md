---
title: Performance Analytics snapshots
description: Snapshots are the lists of records \(sys\_ids\) that are collected at the time that the scores for those records are collected. Snapshots enable users to drill down into the records from a Performance Analytics indicator visualization.
locale: en-US
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Automated indicators, Indicators, Configure fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Performance Analytics snapshots

Snapshots are the lists of records \(sys\_ids\) that are collected at the time that the scores for those records are collected. Snapshots enable users to drill down into the records from a Performance Analytics indicator visualization.

Only automated indicators can have snapshots. Snapshots are made only for those automated indicators that have **Collect records** enabled. The following features require records to be collected:

-   Drilling down into individual records from the scores on a Performance Analytics widget.
-   Showing records in Analytics Hub.
-   Showing records in KPI Details.

## Retention period

By default, snapshots are retained for 183 days. You can change this period either globally or for a specific indicator:

-   To change the global snapshot retention period, edit the system property **com.snc.pa.dc.keep\_snapshots\_for.frequency**. For more information, see [Performance Analytics properties](../reference/pa-properties.md).
-   To change the snapshot retention period for an indicator, configure **Override collection periods** in the "Collection periods" tab of the indicator form. For more information, see [Advanced indicator settings](../task/t_CreateAnAutomatedIndicator.md#).

**Parent Topic:**[Automated indicators](automated-indicators.md)

**Previous topic:**[Add a collection job to an indicator](../task/t_EditAJobForTheIndicator.md)

**Next topic:**[Create an automated indicator with a wizard](../task/t_CrtIndctrIndctrWzrd.md#)

