---
title: System properties
description: These system properties control the behavior of the Data Management capabilities.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Reference, Data Management, Tables and data, Configure core features, Administer]
---

# System properties

These system properties control the behavior of the Data Management capabilities.

## Archive rule and destroy rule properties

Rules to prevent the archive process from consuming too many system resources have been automated. You can manually change the system behavior.

The archive process uses a producer and consumer model. Records are queued for archiving in the Archive Job Execution Chunks \[sys\_archive\_run\_chunk\] table in batches.

-   The ArchiveProducerJob creates chunks of sys\_ids records that need to be archived. Each chunk contains records pertaining to a single archive rule. The maximum number of records in a chunk is specified by the property **glide.db.archive.chunk\_size**. The maximum number of records for a single rule across all chunks is specified by **glide.db.archive.max.rule.records**.
-   The producer starts up 4 \(default\) ArchiverJob consumers. The exact number of consumers is specified by **glide.db.archiving.max\_consumer\_workers**.
-   Consumers read and process chunks of sys\_ids. The number of chunks each consumer processes is specified by **glide.db.archive.max.batches**. The chunks processed by each consumer may be from different archive rules.
-   Consumers repeat reading chunks of sys\_ids until none remain or the limit of chunks a consumer can process \(specified by **glide.db.archive.max.batches**\) is reached, after which it shuts down and schedules another consumer.
-   If a chunk remains in the running state longer than what's specified in **glide.db.archive.chunk.max.process.time**, the system assumes that the consumer abruptly terminated, and it changes the chunk’s status to error. This doesn't stop or end any running consumers.

**Note:** The archive and destroy properties listed in the table are not used if the Archive Job Execution Chunks \[sys\_archive\_run\_chunk\] table is deleted.

To manually control how many records the archive rule and destroy processes at one interval, you can change these default settings by [adding the following system properties](../../reference-pages/reference/r_AvailableSystemProperties.md#).

|Name|Description|Type|Default Value|
|----|-----------|----|-------------|
|glide.db.archive.chunk\_size|Number of unique identifiers added to each record in the Archive Job Execution Chunks \[sys\_archive\_run\_chunk\] table. The record is formatted as CSV values in the keys field of the Archive Job Execution Chunk \(sys\_archive\_run\_chunk.do\) form.|Integer|1000|
|glide.db.archive.chunk.max.process.time|Number of milliseconds a record can remain in the Active state in the Archive Job Execution Chunks \[sys\_archive\_run\_chunk\] table. The time is the difference between the system time and the value of the **Start** field in the Archive Job Execution Chunks \[sys\_archive\_run\_chunk\] table.|Integer|600000|
|glide.db.archive.max.rule.records|Maximum number of records to batch per consumer, per rule.|Integer|10000|
|glide.db.archive.debug|Option that enables verbose logging when copying the column definitions from the original table to the archive table.|true \| false|false|
|glide.db.archive.max.batches|Number of chunks, which are records from the Archive Job Execution Chunks \[sys\_archive\_run\_chunk\] table, processed by a consumer before it shuts down and schedules another consumer.|Integer|10|
|glide.db.archiving.max\_consumer\_workers|The maximum number of concurrent consumers cluster-wide.|Integer|4|

## Table cleaner properties

To set table cleaner system properties, navigate to the System Properties \[sys\_properties\] table and add the property.

<table id="table_pkw_2hy_mxb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configure the number of days table cleaner must wait before attempting to reprocess a slow rule.

 `glide.db.tablecleaner.days_before_slow_rule_reattempt`

</td><td>

When a table cleaner rule has a query that takes longer than 30 seconds to complete, the entire table cleaner job is stopped. By default, table cleaner waits two days before including that rule in the table cleaner job again.You can change the default waiting period by adding this property.

-   Type: integer
-   Default value: 2

</td></tr><tr><td>

Configure a time limit for a table cleaner rule.

 `glide.db.tablecleaner.chunk_delete_max_time_spent`

</td><td>

Limits how long the cleaner spends trying to batch-delete records per rule during a single run. The value is given in seconds and defaults to 1200 \(20 minutes\), which means the table cleaner runs hourly for a maximum of 20 minutes.You can change the default time limit by adding this property.

-   Type: integer
-   Default value: 1200

</td></tr></tbody>
</table>**Parent Topic:**[Data Management reference](../../managing-data/reference/data-management-reference.md)

