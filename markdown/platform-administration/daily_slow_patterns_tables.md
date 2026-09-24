---
title: Daily Slow Patterns tables and fields
description: Tables and fields that Daily Slow Patterns populates with per-day performance telemetry, including trend, anomaly, and I/O tracking data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/daily\_slow\_patterns\_tables.html
release: brazil
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [Daily slow patterns, reference, Discovery]
breadcrumb: [Daily Slow Patterns, Stats Tools, System Diagnostics, Maintain and monitor, Administer the ServiceNow AI Platform]
---

# Daily Slow Patterns tables and fields

Tables and fields that Daily Slow Patterns populates with per-day performance telemetry, including trend, anomaly, and I/O tracking data.

## Daily slow patterns tables

Daily Slow Patterns populates a set of tables that store performance telemetry. For an overview of how the snapshot works, see [Daily Slow Patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/daily_slow_patterns.md). The following table describes each table.

|Table|Description|
|-----|-----------|
|Daily Pattern \[daily\_pattern\]|Base table for daily pattern snapshots. Includes the running-statistics values used to compute trends.|
|Daily Query Pattern \[daily\_query\_pattern\]|Daily snapshot of slow query patterns.|
|Daily Script Pattern \[daily\_script\_pattern\]|Daily snapshot of slow script patterns.|
|Daily Transaction Pattern \[daily\_transaction\_pattern\]|Daily snapshot of slow transaction patterns.|
|Daily Mutex Pattern \[daily\_mutex\_pattern\]|Daily snapshot of mutex contention patterns.|
|Daily Event Pattern \[dailyevent\_pattern\]|Daily snapshot of event patterns.|
|Daily IOStats \[daily\_iostats\]|Per-table daily changes for gets, inserts, updates, deletes, and selects, and their timings. This table is turned off by default.|

## Table I/O tracking property

The Daily IOStats \[daily\_iostats\] table is turned off by default. It's controlled by the **com.glide.stats.daily\_snapshot.diff\_iostats** system property, which defaults to `false`.

|Property|Description|Default|
|--------|-----------|-------|
|**com.glide.stats.daily\_snapshot.diff\_iostats**|Turns daily table I/O trend and anomaly tracking on or off. Set this property to `true` to populate and analyze `daily_iostats`.|`false`|

While the property is `false`, daily snapshot runs skip `daily_iostats` entirely. No rows are created or compared, and any rows left over from a period when it was turned on are cleaned up automatically. The z-score, significance, and running-counter fields apply to `daily_iostats` only after you turn the property on.

## Average, total, and count variants

Each trend value comes in three variants, distinguished by a field-name suffix. The following table describes each variant and the question it answers.

|Field suffix|Column label|Tracks|Question it answers|
|------------|------------|------|-------------------|
|None|\(avg\)|Per-call average duration|Did each run get slower or faster than usual?|
|`_total`|\(no modifier\)|Total duration for the day|Did this pattern consume more or less total time today?|
|`_count`|\(count\)|Execution count for the day|Did this pattern run more or less often today?|

**Note:** The field-name suffix and the column label are inverted by design. The field with no suffix carries the **\(avg\)** label, and the field with the `_total` suffix carries the unqualified label. When you build a report or filter on these columns, check both the field name and the column label rather than assuming one from the other.

The Daily Transaction Pattern \[daily\_transaction\_pattern\] and Daily IOStats \[daily\_iostats\] tables repeat this three-way split once for each tracked dimension, such as `business_rule_time`, `sql_time`, and `cpu_time` for transactions, or `gets`, `inserts`, and `selects` for I/O. Each column is a combination of a dimension and a variant, not a separate metric to understand on its own.

## Internal running counters

To compute deviation and z-score across days, the platform carries forward internal running counters from the previous snapshot. These fields include `welford_weight_sum`, `welford_day_count`, `welford_m2_accumulator`, and `overall_average`, along with their total, count, and per-dimension variants.

**Note:** The running-counter fields are intermediate values that the platform uses to compute the next day's snapshot. Their raw values aren't meaningful on their own, so don't surface them on dashboards or reports. The values meant for use are deviation, z-score, significance, and their percentile ranks.

