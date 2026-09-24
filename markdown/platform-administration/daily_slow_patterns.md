---
title: Daily Slow Patterns
description: Daily Slow Patterns takes a daily rollup of platform performance-pattern data and computes day-over-day trend and anomaly signals for each pattern. You can then determine whether a query, script, or transaction pattern is increasing in frequency or duration over time.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/daily\_slow\_patterns.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 4
keywords: [Daily slow patterns, performance telemetry, Discovery]
breadcrumb: [Stats Tools, System Diagnostics, Maintain and monitor, Administer the ServiceNow AI Platform]
---

# Daily Slow Patterns

Daily Slow Patterns takes a daily rollup of platform performance-pattern data and computes day-over-day trend and anomaly signals for each pattern. You can then determine whether a query, script, or transaction pattern is increasing in frequency or duration over time.

## Requirements

Accessing Daily Slow Patterns requires the admin role.

Daily Slow Patterns requires the Daily Stats Snapshot \(com.glide.stats.daily\_snapshot\) plugin, which is not active by default. To activate it, navigate to **All** &gt; **System Diagnostics** &gt; **Plugins**, search for the plugin by its ID, and install it.

## Access Daily Slow Patterns

To access Daily Slow Patterns, navigate to **All** &gt; **System Diagnostics** &gt; **Stats** &gt; **Daily Slow Patterns**.

**Note:** There is no dedicated dashboard for daily slow patterns data. To analyze patterns across types, query the individual snapshot tables directly or build a custom report. For a list of the available tables, see [Daily Slow Patterns tables and fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/daily_slow_patterns_tables.md).

## Processing overview

The platform tracks performance patterns in memory, including slow queries, scripts, transactions, mutex contention, events, and table I/O. The live pattern aggregates reflect only the totals accumulated since each pattern last reset, which can be minutes or months earlier.

Daily Slow Patterns runs once per day. Rather than capturing a single live total, it computes what changed since the previous day and stores the result as a daily record. This lets you compare a pattern against its own history and identify whether its frequency or duration is shifting over time.

The feature also provides an on-demand comparison that computes a difference between any two points in time. For example, you can capture pattern state before a Discovery run starts and compare it against the state when the run completes.

**Note:** An on-demand comparison reflects all activity on the instance during the selected window, not the activity of a single process. Use it in controlled conditions where other instance activity is limited.

## What data is stored

The daily snapshot tables store performance telemetry only. This telemetry describes how the platform performs, not the data that your users work with. Stored values include execution counts, durations, timing breakdowns, table and script identifiers, mutex and event names, query hashes, and the running-statistics values used to compute trends.

**Important:** The daily snapshot tables contain performance telemetry only. They don't contain business data or customer record data. This distinction supports audit and compliance responses, including FedRAMP and SOC responses, that classify these tables as operational telemetry rather than customer data.

Two fields are an exception to the telemetry-only classification, because both capture diagnostic samples verbatim from live traffic. The following table describes these fields.

|Field|What it can contain|
|-----|-------------------|
|`daily_query_pattern.executable_sql`|A reconstructed, runnable copy of a sampled slow query. Placeholder values are replaced with the values passed at run time. If a query filtered on a literal value, such as a caller name or a case number, that value appears in this field.|
|`daily_pattern.url`|The request URL and the full dumped request parameters for the sampled transaction. Submitted form or record field values can appear here.|

Access to all daily snapshot tables requires the admin role, which limits who can read these values. The values in these two fields are still real customer data after an admin can read them. If your compliance posture prohibits retaining literal record or parameter values, treat `executable_sql` and `url` as sensitive. Scope retention for them separately, even in admin-only tables.

## Trend and anomaly signals

For each pattern, the daily snapshot computes a z-score, a significance value, and a deviation value, along with a percentile rank for each. These values help you find and confirm patterns whose behavior changed. The following list describes what each value tells you:

-   Z-score: how statistically unusual today's value is for a pattern, measured as the number of standard deviations from that pattern's running mean. A value near 0 is typical, and values further from 0 are more unusual.
-   Significance: an operational impact score that combines the z-score with how much of the metric happened that day. Sort or filter on significance to find what changed today.
-   Deviation: how far today's value falls from the pattern's running mean, expressed in the metric's own units.

Each of these values comes in three variants that track different questions about the same pattern: a per-call average, a daily total, and a daily count. The variants can move independently. For example, a pattern that runs far more often than usual changes the count variant. If each run takes its typical time, the average variant stays near 0.

## Data accumulation and reliability

The reliability of z-scores, deviation, and significance rankings increases as more daily snapshots accumulate for a pattern.

**Note:** Z-scores, deviation, and significance rankings aren't meaningful until enough daily snapshots have accumulated after installation. On a newly installed instance, no history exists yet, so these values can't describe a pattern's real variability.

The following points describe how the values behave over time:

-   On the first day a pattern is seen, no variance can be measured yet, so deviation is 0 and the z-score is 0 by definition.
-   For the first several days, the running standard deviation is based on very few samples and is statistically noisy. A single unusual day can move the mean and deviation disproportionately.
-   The platform doesn't enforce a fixed warm-up period. As a practical guideline, treat z-scores and significance rankings as informational rather than actionable until a pattern has accumulated at least several weeks of daily snapshots.

