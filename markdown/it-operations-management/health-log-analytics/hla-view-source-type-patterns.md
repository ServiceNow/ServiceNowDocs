---
title: Review the patterns extracted from a source type in Health Log Analytics
description: View all learned patterns extracted from a source type in a source type structure, together with the log sources in which these patterns appeared. Reviewing these patterns can provide valuable insights into the log message patterns that Health Log Analytics tracks for each source type and log source.
locale: en-US
release: xanadu
product: Health Log Analytics
classification: health-log-analytics
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
keywords: [ServiceNow, Health Log Analytics, HLA, source type structure, source types, patterns, log sources, log messages, Aggregated Log Patterns]
breadcrumb: [Set up data inputs for Health Log Analytics manually, Health Log Analytics data input setup, Configuring Health Log Analytics, Health Log Analytics, ITOM Health, IT Operations Management]
---

# Review the patterns extracted from a source type in Health Log Analytics

View all learned patterns extracted from a source type in a source type structure, together with the log sources in which these patterns appeared. Reviewing these patterns can provide valuable insights into the log message patterns that Health Log Analytics tracks for each source type and log source.

## Before you begin

Role required: evt\_mgmt\_admin

## Procedure

1.  Navigate to **All** &gt; **Health Log Analytics** &gt; **Source Type Structures**.

2.  Select a source type in the **Source type name** column.

3.  On the Source Type form, select the **Aggregated Log Patterns** related list.

    The tab shows the following data for each pattern that was extracted from this source type. The displayed data is updated every hour.

    |Column|Description|
    |------|-----------|
    |Pattern text|The content of the aggregated pattern.|
    |Sources|The sources in which the pattern appeared.|
    |Domain|The domain to which the pattern belongs.|


**Parent Topic:**[Set up data inputs for Health Log Analytics manually](hla-data-input-setup-manual.md)

