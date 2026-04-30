---
title: Table extension
description: Partition and preserve data sets for extended periods without overwriting.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Database rotation, Data Management, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Table extension

Partition and preserve data sets for extended periods without overwriting.

Table extension is based around a base table and a number of shards. The shards are given a duration which determines the period of time across which data is written to each shard. Shards in a table extension don't rotate. Instead of the oldest shard being truncated and re-used, an extension creates new shards indefinitely. This way, data remains logically separated across shards due to creation date and no data is ever deleted.

You typically specify the time parameter \(duration\) of the process, but may alternatively specify the number of tables \(rotations\). After the last table in a rotation is written, new tables are added and old tables are archived. Using table extension, tables are never overwritten.

An advantage of table extension is to partition data across tables. It also allows you to archive data while ensuring that tables stay reasonably-sized. The working set of data is reduced when a date is known for the query.

The disadvantage is that table extension requires a union query when you query for a time range that spans multiple tables. Union queries are less efficient than queries against a single table.

Consider using table extension when you have sequentially-written tables or insert-only type tables \(there are exceptions to this parameter\). Table extension is also useful in tables where data is needed for long periods of time.

-   **[Apply table extension](../../platform-performance/task/t_TableExtensionExample.md)**  
Preserve data sets using table extension.

**Parent Topic:**[Database rotation](../../database-rotation/concept/c_DatabaseRotation.md)

**Related topics**  


[Activate database rotation](../../database-rotation/task/t_ActivateDatabaseRotation.md)

[Table rotation](../../platform-performance/concept/c_TableRotation.md)

