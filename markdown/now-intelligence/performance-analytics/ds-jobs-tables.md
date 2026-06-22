---
title: Data snapshots jobs and tables
description: Several types of components are installed with activation of the Data snapshots plugin, including tables and scheduled jobs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/performance-analytics/ds-jobs-tables.html
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: reference
last_updated: "2026-05-12"
reading_time_minutes: 1
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
</table>## Tables installed

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

Reference table for record hierarchies used with Data Snapshots indicators. For more information, see [Building hierarchical queries](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/table-administration-and-data-management/data-hierarchies.md).

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

</td></tr></tbody>
</table>**Parent Topic:**[Data snapshots and multiple breakdowns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/multi-level-breakdowns.md)

