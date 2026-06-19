---
title: Deactivate Data snapshots
description: You can turn Data snapshots off or back on for an indicator, provided that indicator supports Data snapshots. An admin can turn the feature off for an instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/performance-analytics/deactivate-mlb-for-indicator.html
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Data snapshots and multiple breakdowns, Configure fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Deactivate Data snapshots

You can turn Data snapshots off or back on for an indicator, provided that indicator supports Data snapshots. An admin can turn the feature off for an instance.

## Before you begin

Role required: pa\_data\_collector or higher

## About this task

The limitations of Data snapshots could make an indicator unusable. In this case, you can deactivate Data snapshots on that indicator. You can re-activate Data snapshots on that indicator later. For more information, see [Limitations and requirements for Data snapshots](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/limitations-mlb.md).

**Important:** An admin can disable Data snapshots across an instance by setting the system property com.snc.pa.dm.enable.mlb to false. They should also turn off the Instance Eligibility Check for Data Snapshots job.

## Procedure

1.  Navigate to **All** &gt; **Indicators** &gt; **Automated indicators** or **All** &gt; **Indicators** &gt; **Formula indicators**, depending on the indicator.

2.  Open the indicator that you want to restore to the previous indicator and breakdown sources and breakdown matrix.

3.  Select **Disable Data snapshots**.

4.  Select **Update**.


## What to do next

At any time in the future, you can reverse this procedure. The indicator is then moved to the new source type that supports Data snapshots. If an admin disables Data snapshots for an instance and then re-enables them, data snapshots are re-enabled automatically for those indicators that previously had them enabled.

**Parent Topic:**[Data snapshots and multiple breakdowns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/multi-level-breakdowns.md)

