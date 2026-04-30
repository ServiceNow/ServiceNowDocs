---
title: Data snapshot sources and collection
description: Data snapshots include data sources for indicator score collection and the mapping between indicators and these sources.
locale: en-US
release: yokohama
product: Performance Analytics
classification: performance-analytics
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Data snapshots and multiple breakdowns, Configuring fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Data snapshot sources and collection

Data snapshots include data sources for indicator score collection and the mapping between indicators and these sources.

## Mapping between indicators and Data Snapshot sources

For each indicator that successfully has Data snapshots activated, the Performance Analytics indicator and breakdown sources are replaced by a Data snapshots source. The mapping between these sources and indicators is visible in the Indicator to Data Snapshots Mapping \[pa\_cdc\_indicator\_analytics\_mapping\] table. The pa\_admin role is required for viewing. This table shows the Data snapshots data source for each indicator, along with the date when Data snapshots started to be supported for the indicator. This date is important, because multiple breakdown scores cannot be collected from before this date.

From the Data snapshots field, you can navigate to the data snapshots data sources.

## Data snapshots data sources

Data snapshots sources are available to users with the pa\_admin role on the Data Snapshots \[pa\_dm\_analytics\_source\] table. By default, the contents of this table are read-only. However, an admin user can add the **Enable data collection** checkbox to the form, in which case a pa\_data\_collector or pa\_admin user can enable or disable the data collection job.

## Data snapshots collection jobs

Data snapshots jobs are accessible read-only to pa\_admin users. To open the jobs, navigate to **Platform analytics administration** &gt; **Data collection** &gt; **Data snapshots**.

Classic Performance Analytics data collection jobs continue to run in parallel with data snapshots collection jobs. The scores from the classic jobs are not used for indicators with data snapshots enabled. The classic jobs still run to simplify rollback if necessary.

Data snapshots collection jobs copy a subset of the source table. These jobs also create a copy of every daily change for a record. These jobs may therefore result in increased storage use by Performance Analytics.

**Parent Topic:**[Data snapshots and multiple breakdowns](../concept/multi-level-breakdowns.md)

