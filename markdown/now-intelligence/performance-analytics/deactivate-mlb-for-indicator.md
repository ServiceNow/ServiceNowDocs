---
title: Deactivate data snapshots for an indicator
description: You can turn data snapshots off or back on for an indicator, provided that indicator supports data snapshots.
locale: en-US
release: zurich
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Data snapshots and multiple breakdowns, Configure fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Deactivate data snapshots for an indicator

You can turn data snapshots off or back on for an indicator, provided that indicator supports data snapshots.

## Before you begin

Role required: pa\_data\_collector or higher

## About this task

The limitations of data snapshots could make an indicator unusable. In this case, you can deactivate data snapshots on that indicator. You can re-activate data snapshots on that indicator later. For more information, see [Limitations and requirements for data snapshots](../reference/limitations-mlb.md).

**Important:** An admin can disable data snapshots across an instance by setting the system property com.snc.pa.dm.enable.mlb to false.

## Procedure

1.  Navigate to **All** &gt; **Indicators** &gt; **Automated indicators** or **All** &gt; **Indicators** &gt; **Formula indicators**, depending on the indicator.

2.  Open the indicator that you want to restore to the previous indicator and breakdown sources and breakdown matrix.

3.  Select **Disable Data snapshots**.

4.  Select **Update**.


## What to do next

At any time in the future, you can reverse this procedure. The indicator is then moved to the new source type that supports data snapshots. If an admin disables data snapshots for an instance and then re-enables them, data snapshots are re-enabled automatically for those indicators that previously had them enabled.

**Parent Topic:**[Data snapshots and multiple breakdowns](../concept/multi-level-breakdowns.md)

