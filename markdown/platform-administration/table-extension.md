---
title: Table extension
description: Partition and preserve data sets for extended periods without overwriting.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/table-extension.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [table extension, database rotation, table shards, data partitioning]
breadcrumb: [Applying database rotation techniques, Data Management, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Table extension

Partition and preserve data sets for extended periods without overwriting.

Table extension is based around a base table and a number of shards. The shards are given a duration which determines the period of time across which data is written to each shard. Shards in a table extension don't rotate. Instead of the oldest shard being truncated and re-used, an extension creates new shards indefinitely. This way, data remains logically separated across shards due to creation date and no data is ever deleted.

## Advantages

Table extension partitions data across tables, which allows you to archive data while ensuring that tables stay reasonably-sized. The working set of data is reduced when queries include date-range filters that limit results to specific shards.

## Disadvantages

Table extension requires a union query when you query for a time range that spans multiple tables. Union queries are less efficient than queries against a single table. Improperly configured table extensions can cause the system to query across multiple extension tables unnecessarily, resulting in slower query performance and higher database load.

-   **[Apply table extension](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_TableExtensionExample.md)**  
Preserve data sets using table extension.

**Parent Topic:**[Applying database rotation techniques](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/c_DatabaseRotation.md)

**Related topics**  


[Activate database rotation]()

[Table rotation]()

