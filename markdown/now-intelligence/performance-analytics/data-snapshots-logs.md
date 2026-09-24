---
title: Data snapshots logs
description: Each Data snapshots job creates log entries describing the events that happened when that job ran.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/performance-analytics/data-snapshots-logs.html
release: brazil
product: Performance Analytics
classification: performance-analytics
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Data snapshots and multiple breakdowns, Configure fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Data snapshots logs

Each Data snapshots job creates log entries describing the events that happened when that job ran.

You can view the logs in two locations:

-   To view the logs associated with a specific Data snapshots data source, open the data source. The sources are located at **Platform analytics administration** &gt; **Data sources** &gt; **Data snapshots**. Alternatively, you can open the data source for an indicator from the Source column in the [Indicator library](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/your-kpis.md). The job logs for each source are listed in a related list on that source record.
-   To view all Data snapshots logs, open the Data Snapshots Logs \[syslog\_pa\_dm\] table. There is no navigation path.

**Note:** Do not confuse the Data snapshots logs with the Data Snapshots Statistics \[pa\_dm\_task\_telemetry\] records, which are accessible at **Platform Analytics Administration** &gt; **Data Collector** &gt; **Data Snapshots Job Logs**. Data Snapshots Statistics show the duration of job runs.

## First run job logs

Before the first job is run on a new data source, you get a message with an estimate of how much time the job will take.

\[Omitted image "all-activity-pre-job.png"\] Alt text: Pre-job log entry for new source.

When your data source changes, such as when you add fields, the snapshot is retaken. You get a similar message to the first run message.

\[Omitted image "change-loader-estimate.png"\] Alt text: New snapshot to load changes to data source table.

## Change mining logs

During both daily and "all changes" jobs, you get an initial message with a time estimate to score generation. If you are viewing the related list logs on a data source, you get incremental progress messages. At the end, you are told what records changed, how long the mining job took, and how long it is until the next one.

\[Omitted image "change-mining-short-log.png"\] Alt text: A change mining job with log entries for estimated and actual time to complete and time until next run.

\[Omitted image "change-mining-completion.png"\] Alt text: A completed change mining show showing changes.

**Parent Topic:**[Data snapshots and multiple breakdowns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/performance-analytics/multi-level-breakdowns.md)

