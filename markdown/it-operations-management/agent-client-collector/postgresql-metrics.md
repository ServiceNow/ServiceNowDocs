---
title: PostgreSQL metrics
description: The following tables list and describe the metrics that are gathered as output from the specified PostgreSQL checks. Entries indicated as Featured metrics are high-visibility metrics that are displayed in the Operator Workspace Metric tab after an alert is generated. These metrics provide the operator with additional information to help them further explore the specified issue.
locale: en-US
release: xanadu
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Agent Client Collector Monitoring default checks and policies, Agent Client Collector Monitoring reference, Agent Client Collector Monitoring, Agent Client Collector, IT Operations Management]
---

# PostgreSQL metrics

The following tables list and describe the metrics that are gathered as output from the specified PostgreSQL checks. Entries indicated as **Featured metrics** are high-visibility metrics that are displayed in the Operator Workspace Metric tab after an alert is generated. These metrics provide the operator with additional information to help them further explore the specified issue.

<table id="table_ykl_4rw_gsb"><thead><tr><th>

Metric

</th><th>

Description

</th></tr></thead><tbody><tr><td>

pgsql.connections.active\(Featured metric\)

</td><td>

Provides metrics on the total active connections in the PostgreSQL database.

</td></tr><tr><td>

pgsql.connections.idle\(Featured metric\)

</td><td>

Provides metrics on the total idle connections on the PostgreSQL database.

</td></tr></tbody>
</table><table id="table_cnv_rsw_gsb"><thead><tr><th>

Metric

</th><th>

Description

</th></tr></thead><tbody><tr><td>

pgsql.db.size\(Featured metric\)

</td><td>

Provides metrics on the total disk size utilization for each of the PostgreSQL databases on the server.

</td></tr></tbody>
</table>|Metric|Description|
|------|-----------|
|pgsql.locks.AccessShareLock|Provides metrics on read-lock mode acquired automatically from queried tables.|
|pgsql.locks.ExclusiveLock|Provides metrics on read-lock mode acquired by LOCK TABLE table for IN EXCLUSIVE MODE statements.|

<table id="table_dbs_x4x_gsb"><thead><tr><th>

Metric

</th><th>

Description

</th></tr></thead><tbody><tr><td>

pgsql.tables\_size\(Featured metric\)

</td><td>

Provides metrics on the database table size on the server.

</td></tr></tbody>
</table><table id="table_ijk_3px_gsb"><thead><tr><th>

Metric

</th><th>

Description

</th></tr></thead><tbody><tr><td>

pgsql.statsbgwriter.buffers\_alloc

</td><td>

Provides metrics related to the number of allocated buffers.

</td></tr><tr><td>

pgsql.statsbgwriter.buffers\_backend

</td><td>

Provides metrics related to the number of buffers written directly by a backend.

</td></tr><tr><td>

pgsql.statsbgwriter.buffers\_backend\_fsync

</td><td>

Provides metrics related to the number of times a backend had to execute its own fsync call \(normally the background writer handles those, even when the backend performs its own write\).

</td></tr><tr><td>

pgsql.statsbgwriter.buffers\_checkpoint

</td><td>

Provides metrics related to the number of buffers written during checkpoints.

</td></tr><tr><td>

pgsql.statsbgwriter.buffers\_clean

</td><td>

Provides metrics related to the number of buffers written by the background writer.

</td></tr><tr><td>

pgsql.statsbgwriter.checkpoint\_sync\_time

</td><td>

Provides metrics related to the total amount of time spent in the portion of checkpoint processing where files are synchronized to disk, in milliseconds.

</td></tr><tr><td>

pgsql.statsbgwriter.checkpoint\_write\_time

</td><td>

Provides metrics related to the total amount of time spent in the portion of checkpoint processing where files are written to disk, in milliseconds.

</td></tr><tr><td>

pgsql.statsbgwriter.checkpoints\_req\(Featured metric\)

</td><td>

Provides metrics related to the number of requested checkpoints that have been performed.

</td></tr><tr><td>

pgsql.statsbgwriter.checkpoints\_timed\(Featured metric\)

</td><td>

Provides metrics related to the number of scheduled checkpoints that have been performed.

</td></tr><tr><td>

pgsql.statsbgwriter.maxwritten\_clean

</td><td>

Provides metrics related to the number of times the background writer stopped a cleaning scan because it had written too many buffers.

</td></tr></tbody>
</table><table id="table_x5y_dxx_gsb"><thead><tr><th>

Metric

</th><th>

Description

</th></tr></thead><tbody><tr><td>

pgsql.statsdb.blk\_read\_time\(Featured metric\)

</td><td>

Provides metrics related to the time spent reading data file blocks by backends in this database, in milliseconds.

</td></tr><tr><td>

pgsql.statsdb.blk\_write\_time\(Featured metric\)

</td><td>

Provides metrics related to the time spent writing data file blocks by backends in this database, in milliseconds.

</td></tr><tr><td>

pgsql.statsdb.blks\_hit\(Featured metric\)

</td><td>

Provides metrics related to the number of times disk blocks were found in the buffer cache, so that a read was not necessary. This only includes hits in the PostgreSQL buffer cache, not the operating system's file system cache.

</td></tr><tr><td>

pgsql.statsdb.blks\_read

</td><td>

Provides metrics related to the number of disk blocks read in this database.

</td></tr><tr><td>

pgsql.statsdb.checksum\_failures

</td><td>

Provides metrics related to the number of data page checksum failures detected in this database \(or on a shared object\), or 0 if data checksums are not enabled.

</td></tr><tr><td>

pgsql.statsdb.conflicts

</td><td>

Provides metrics related to the number of queries canceled due to conflicts with recovery in this database. Conflicts occur only on standby servers.

</td></tr><tr><td>

pgsql.statsdb.deadlocks\(Featured metric\)

</td><td>

Provides metrics related to the number of deadlocks detected in this database.

</td></tr><tr><td>

pgsql.statsdb.numbackends

</td><td>

Provides metrics related to the number of backends currently connected to this database. This is the only column in this view that returns a value reflecting the current state; all other columns return the accumulated values since the last reset.

</td></tr><tr><td>

pgsql.statsdb.temp\_bytes

</td><td>

Provides metrics related to the total amount of data written to temporary files by queries in this database. All temporary files are counted, regardless of why the temporary file was created, and regardless of the **log\_temp\_files** setting.

</td></tr><tr><td>

pgsql.statsdb.temp\_files

</td><td>

Provides metrics related to the number of temporary files created by queries in this database. All temporary files are counted, regardless of why the temporary file was created \(such as sorting or hashing\), and regardless of the **log\_temp\_files** setting.

</td></tr><tr><td>

pgsql.statsdb.tup\_deleted

</td><td>

Provides metrics related to the number of rows deleted by queries in this database.

</td></tr><tr><td>

pgsql.statsdb.tup\_fetched

</td><td>

Provides metrics related to the number of rows fetched by queries in this database.

</td></tr><tr><td>

pgsql.statsdb.tup\_inserted

</td><td>

Provides metrics related to the number of rows inserted by queries in this database.

</td></tr><tr><td>

pgsql.statsdb.tup\_returned

</td><td>

Provides metrics related to the number of rows returned by queries in this database.

</td></tr><tr><td>

pgsql.statsdb.tup\_updated

</td><td>

Provides metrics related to the number of rows updated by queries in this database.

</td></tr><tr><td>

pgsql.statsdb.xact\_commit

</td><td>

Provides metrics related to the number of transactions in this database that have been committed.

</td></tr><tr><td>

pgsql.statsdb.xact\_rollback

</td><td>

Provides metrics related to the number of transactions in this database that have been rolled back.

</td></tr></tbody>
</table><table id="table_vgv_tdy_gsb"><thead><tr><th>

Metric

</th><th>

Description

</th></tr></thead><tbody><tr><td>

pgsql.statsio.heap\_blks\_hit\(Featured metric\)

</td><td>

Provides metrics related to the number of buffer hits in this table.

</td></tr><tr><td>

pgsql.statsio.heap\_blks\_read

</td><td>

Provides metrics related to the number of disk blocks read from this table.

</td></tr><tr><td>

pgsql.statsio.idx\_blks\_hit

</td><td>

Provides metrics related to the number of buffer hits in all indexes in this table.

</td></tr><tr><td>

pgsql.statsio.idx\_blks\_read

</td><td>

Provides metrics related to the number of disk blocks read from all indexes in this table.

</td></tr><tr><td>

pgsql.statsio.tidx\_blks\_hit

</td><td>

Provides metrics related to the number of buffer hits in this table's TOAST table index \(if any\).

</td></tr><tr><td>

pgsql.statsio.tidx\_blks\_read

</td><td>

Provides metrics related to the number of disk blocks read from this table's TOAST table index.

</td></tr><tr><td>

pgsql.statsio.toast\_blks\_hit

</td><td>

Provides metrics related to the number of buffer hits in this table's TOAST table \(if any\).

</td></tr><tr><td>

pgsql.statsio.toast\_blks\_read

</td><td>

Provides metrics related to the number of disk blocks read from this table's TOAST table \(if any\).

</td></tr></tbody>
</table>|Metric|Description|
|------|-----------|
|pgsql.statstable.idx\_scan|Provides metrics related to the number of index scans initiated on this table.|
|pgsql.statstable.idx\_tup\_fetch|Provides metrics related to the number of live rows fetched by index scans.|
|pgsql.statstable.n\_dead\_tup|Provides metrics related to the estimated number of dead rows.|
|pgsql.statstable.n\_live\_tup|Provides metrics related to the estimated number of live rows.|
|pgsql.statstable.n\_tup\_del|Provides metrics related to the number of deleted rows.|
|pgsql.statstable.n\_tup\_hot\_upd|Provides metrics related to the number of rows HOT updated \(that is, with no separate index update required\).|
|pgsql.statstable.n\_tup\_ins|Provides metrics related to the number of inserted rows.|
|pgsql.statstable.n\_tup\_upd|Provides metrics related to the number of updated rows.|
|pgsql.statstable.seq\_scan|Provides metrics related to the number of sequential scans initiated on this table.|
|pgsql.statstable.seq\_tup\_read|Provides metrics related to the number of live rows fetched by sequential scans.|

**Parent Topic:**[Agent Client Collector Monitoring default checks and policies](agent-policies-checks.md)

