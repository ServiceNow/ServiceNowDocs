---
title: Data snapshots jobs and tables
description: Several types of components are installed with activation of the Data snapshots plugin, including tables and scheduled jobs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/performance-analytics/ds-jobs-tables.html
release: brazil
product: Performance Analytics
classification: performance-analytics
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Data snapshots and multiple breakdowns, Configure fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Data snapshots jobs and tables

Several types of components are installed with activation of the Data snapshots plugin, including tables and scheduled jobs.

## Scheduled jobs installed

<table id="table_fps_5jt_fjc"><thead><tr><th>

Scheduled job

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Instance Eligibility Check Job for Data Snapshots

</td><td>

Daily job to check whether the instance is eligible for the Data snapshots feature. If so, Data snapshots are enabled on the instance.

 If you want to disable the Data snapshots feature, deactivate this job.

</td></tr><tr><td>

Instance readiness for Data snapshots

</td><td>

On demand job to enable Data snapshots for an instance. Called by the Instance Eligibility Check job for Data Snapshots.

</td></tr></tbody>
</table>## Scheduled data collections

The following jobs are defined on the Scheduled Data Collections \[sysauto\_dm\_cdc\_collector\] table. These jobs populate Data snapshots indicators with scores.

|Scheduled data collection|Description|
|-------------------------|-----------|
|First snapshot|Sets up the initial data for analysis by capturing the current state of the fact table. It runs one time, when a Data snapshots source is set up. It collects a snapshot of the facts table to prepare the system for daily updates.|
|Incremental all changes snapshots|Runs every 30 minutes on Data snapshots indicators whose data frequency is **All changes**.|
|Incremental daily snapshot|Runs every hour on Data snapshots sources whose frequency is **Daily**. Updates the final fact table once a day with the last change.|

To see how much time each job took, find the job in the Data Snapshots Statistics \[pa\_dm\_task\_telemetry\] table. Navigate to this table at **Platform Analytics Administration** &gt; **Data Collector** &gt; **Data Snapshots Job Logs**.

To see the details of each job that was run on a Data Snapshots data source, open the data source \[pa\_dm\_analytics\_source\] at **Platform Analytics Administration** &gt; **Data Sources** &gt; **Data Snapshots**. The logs are listed in the Data Snapshots Logs related list. For more information, see [Data snapshots logs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/performance-analytics/data-snapshots-logs.md).

## Tables installed

<table id="table_hps_5jt_fjc"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Data Snapshots Indicators

 \[pa\_datasnapshot\_indicator\]

</td><td>

Indicators created in Data snapshots

</td></tr><tr><td>

Data Snapshots Hierarchies

 \[pa\_cdc\_hierarchy\]

</td><td>

Reference table for record hierarchies used with Data Snapshots indicators. For more information, see [Building hierarchical queries](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/data-hierarchies.md).

</td></tr><tr><td>

Scheduled Data Collections

 \[sysauto\_dm\_cdc\_collector\]

</td><td>

Initial, daily, and all changes data collection jobs. You cannot add jobs to this table.

</td></tr><tr><td>

Data Snapshots Statistics

 \[pa\_dm\_task\_telemetry\]

</td><td>

Log records for Data snapshots collection jobs

</td></tr><tr><td>

Data Snapshots Exclusions

 \[pa\_cdc\_exclusions\]

</td><td>

List of tables that cannot be sources for Data snapshots indicators

</td></tr><tr><td>

Calculated Fields

 \[pa\_calculated\_field\]

</td><td>

Fields that show the difference between two date/time fields on a Data snapshots source table

</td></tr><tr><td>

Bucket Group Mappings

 \[pa\_dm\_bucket\_group\_mapping\]

</td><td>

Mappings of bucket groups to numeric or calculated fields on Data snapshots indicators

</td></tr></tbody>
</table>**Parent Topic:**[Data snapshots and multiple breakdowns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/performance-analytics/multi-level-breakdowns.md)

