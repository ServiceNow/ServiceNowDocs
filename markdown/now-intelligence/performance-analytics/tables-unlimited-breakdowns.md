---
title: Data snapshots sources and collection
description: Data snapshots include data sources for indicator score collection and the mapping between indicators and these sources.
locale: en-US
release: zurich
product: Performance Analytics
classification: performance-analytics
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Data snapshots and multiple breakdowns, Configure fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Data snapshots sources and collection

Data snapshots include data sources for indicator score collection and the mapping between indicators and these sources.

## Data Snapshot sources

For each automated indicator that successfully has Data snapshots activated, the Performance Analytics indicator and breakdown sources are replaced by a Data snapshots source. You can view the Data snapshots source for each indicator in the Indicators library \(**Platform Analytics** &gt; **Library** &gt; **Indicators**\). The source is given in the Source column. If the Data snapshots status is Enabled, this source is a Data snapshots source. Otherwise, it is the traditional indicator source. Data snapshots source names are in lower case with the individual words separated by underlines.

![Two automated indicators in the Indicator Library, showing sources when Data snapshots are enabled or not.](../image/data-snapshots-sources-in-library.png "Sources of one automated indicator with and one without Data snapshots enabled")

## Data snapshots data sources and logs

Data snapshots sources are available on the Data Snapshots \[pa\_dm\_analytics\_source\] table to users with the pa\_data\_collector, pa\_admin, or admin role. To open the data sources, navigate to **Platform analytics administration** &gt; **Data sources** &gt; **Data snapshots**. The records are mostly read-only, but you can disable the Data snapshots job in the **Data collection enabled** checkbox.

**Warning:** To re-enable the data snapshots job, contact Now Support.

Data snapshots source records include logs of the original enablement and all subsequent data collection jobs that are related to that data source.

## Data snapshots collection jobs

Data snapshots jobs are located in the Scheduled Data Collections \[sysauto\_dm\_cdc\_collector\] table and are accessible read-only to pa\_admin users. To open the jobs, navigate to **Platform analytics administration** &gt; **Data collector** &gt; **Data snapshots jobs**.

Classic Performance Analytics data collection jobs continue to run in parallel with Data snapshots collection jobs. The scores from the classic jobs are not used for indicators with Data snapshots enabled. The classic jobs still run to simplify rollback if necessary.

Data snapshots collection jobs copy a subset of the source table. These jobs also create a copy of every daily change for a record. These jobs may therefore result in increased storage use by Performance Analytics.

## Data snapshots job logs

All job logs are in the Data Snapshots Statistics \[pa\_dm\_task\_telemetry\] table. Open Data snapshot job logs at **Platform analytics administration** &gt; **Data collector** &gt; **Data snapshots job logs**. Whereas a Data snapshots data source record shows only the job logs related to that data source, the Data Snapshots Statistics list shows all Data snapshots job logs.

**Parent Topic:**[Data snapshots and multiple breakdowns](../concept/multi-level-breakdowns.md)

