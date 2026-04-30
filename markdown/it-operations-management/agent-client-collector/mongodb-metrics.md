---
title: MongoDB metrics
description: The following table lists the metrics that are gathered as output from MongoDB checks. Entries indicated as Featured metrics are high-visibility metrics that are displayed in the Operator Workspace Metric tab after an alert is generated. These metrics provide the operator with additional information to help them further explore the specified issue.
locale: en-US
release: yokohama
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 9
breadcrumb: [Agent Client Collector Monitoring default checks and policies, Agent Client Collector Monitoring reference, Agent Client Collector Monitoring, Agent Client Collector, IT Operations Management]
---

# MongoDB metrics

The following table lists the metrics that are gathered as output from MongoDB checks. Entries indicated as **Featured metrics** are high-visibility metrics that are displayed in the Operator Workspace Metric tab after an alert is generated. These metrics provide the operator with additional information to help them further explore the specified issue.

|Metric type|Resource \(name of specific database, where relevant\)|Units|Metric type description|
|-----------|------------------------------------------------------|-----|-----------------------|
|mongodb.asserts.msg \(featured metric\)| |count|Number of message assertions raised since the MongoDB process started. Examine the log file for more information about these messages.|
|mongodb.asserts.regular \(featured metric\)| |count|Number of regular assertions raised since the MongoDB process started. Examine the log file for more information about these messages.|
|mongodb.asserts.rollovers| |count|Number of times that the rollover counters have rolled over since the last time the MongoDB process started.|
|mongodb.asserts.tripwire| | |Number of tripwire assertions raised since the MongoDB process started.|
|mongodb.asserts.user| |count|Number of "user asserts" that occurred since the last time the MongoDB process started.|
|mongodb.asserts.warning \(featured metric\)| |count|Number of warnings raised since the MongoDB process started.|
|mongodb.connections.available| |count|Number of unused incoming connections available.|
|mongodb.connections.current| |count|Number of incoming connections from clients to the database server.|
|mongodb.connections.totalCreated| |count|Count of all incoming connections created to the server.|
|mongodb.cursor.open.noTimeout| |count|Number of open cursors with the option **DBQuery.Option.noTimeout** set to prevent timeout after a period of inactivity.|
|mongodb.cursor.open.pinned| |count|Number of "pinned" open cursors.|
|mongodb.cursor.open.total \(featured metric\)| |count|Number of cursors that MongoDB is maintaining for clients. Because MongoDB exhausts unused cursors, typically this value is small or zero. However, if there is a queue, stale tailable cursors, or a large number of operations, this value may increase.|
|mongodb.cursor.timedOut| |count|Total number of cursors that have timed out since the server process started.|
|mongodb.databaseSizes.avgObjSize|admin|bytes|Average size of each document in bytes.|
|mongodb.databaseSizes.avgObjSize|config|bytes|Average size of each document in bytes.|
|mongodb.databaseSizes.avgObjSize|local|bytes|Average size of each document in bytes.|
|mongodb.databaseSizes.collections|admin|count|Number of collections in the database.|
|mongodb.databaseSizes.collections|config|count|Number of collections in the database.|
|mongodb.databaseSizes.collections|local|count|Number of collections in the database.|
|mongodb.databaseSizes.dataSize|admin|bytes|Total size of the uncompressed data held in the database. The **dataSize** decreases when you remove documents. For databases using the **WiredTiger** storage engine, **dataSize** may be larger than **storageSize** if compression is enabled. The **dataSize** decreases when documents shrink.|
|mongodb.databaseSizes.dataSize|config|bytes|Total size of the uncompressed data held in the database.|
|mongodb.databaseSizes.dataSize|local|bytes|Total size of the uncompressed data held in the database.|
|mongodb.databaseSizes.indexes|admin|count|Total number of indexes across all collections in the database.|
|mongodb.databaseSizes.indexes|config|count|Total number of indexes across all collections in the database.|
|mongodb.databaseSizes.indexes|local|count|Total number of indexes across all collections in the database.|
|mongodb.databaseSizes.indexSize|admin|bytes|Sum of the space allocated to all indexes in the database, including free index space.|
|mongodb.databaseSizes.indexSize|config|bytes|Sum of the space allocated to all indexes in the database, including free index space.|
|mongodb.databaseSizes.indexSize|local|bytes|Sum of the space allocated to all indexes in the database, including free index space.|
|mongodb.databaseSizes.objects|admin|count|Number of objects \(specifically, documents\) in the database across all collections.|
|mongodb.databaseSizes.objects|config|count|Number of objects \(specifically, documents\) in the database across all collections.|
|mongodb.databaseSizes.objects|local|count|Number of objects \(specifically, documents\) in the database across all collections.|
|mongodb.databaseSizes.storageSize|admin|bytes|This value does not decrease as you remove or shrink documents. This value may be smaller than **dataSize** for databases using the **WiredTiger** storage engine with compression enabled. **storageSize** does not include space allocated to indexes. See **indexSize** for the total index size.|
|mongodb.databaseSizes.storageSize|config|bytes|Sum of the space allocated to all collections in the database for document storage, including free space.|
|mongodb.databaseSizes.storageSize|local|bytes|Sum of the space allocated to all collections in the database for document storage, including free space.|
|mongodb.globalLock.activeClients.readers \(featured metric\)| |count|Number of active client connections performing read operations.|
|mongodb.globalLock.activeClients.total| |count|Total number of internal client connections to the database, including system threads as well as queued readers and writers. This metric will be higher than the total of **activeClients.readers** and **activeClients.writers** due to the inclusion of system threads.|
|mongodb.globalLock.activeClients.writers \(featured metric\)| |count|Number of active client connections performing write operations.|
|mongodb.globalLock.currentQueue.readers \(featured metric\)| |count|Number of operations that are currently queued and waiting for the read lock. A consistently small read queue, particularly of shorter operations, is not a cause for concern.|
|mongodb.globalLock.currentQueue.total| |count|Total number of operations queued waiting for the lock \(i.e., the sum of **globalLock.currentQueue.readers** and **globalLock.currentQueue.writers**\). A consistently small queue, particularly of shorter operations, is not a cause for concern. The **globalLock.activeClients** readers and writers information provides context for this data.|
|mongodb.globalLock.currentQueue.writers \(featured metric\)| |count|Number of operations that are currently queued and waiting for the write lock. A consistently small write queue, particularly of shorter operations, is not a cause for concern.|
|mongodb.globalLock.totalTime| |microseconds|Time, in microseconds, since the database last started and created the **globalLock**. This is approximately equivalent to the total server uptime.|
|mongodb.locks.Collection.acquireCount\_r| |count|Number of times the collection lock was acquired in the Intent Shared \(IS\) lock mode.|
|mongodb.locks.Collection.acquireCount\_w| |count|Number of times the collection lock was acquired in the Intent Exclusive \(IX\) lock mode.|
|mongodb.locks.Collection.acquireCount\_W| |count|Number of times the collection lock was acquired in the Exclusive \(X\) lock mode.|
|mongodb.locks.Database.acquireCount\_r| |count|Number of times the database lock was acquired in the Intent Shared \(IS\) lock mode.|
|mongodb.locks.Database.acquireCount\_w| |count|Number of times the database lock was acquired in the Intent Exclusive \(IX\) lock mode.|
|mongodb.locks.Database.acquireCount\_W| |count|Number of times the database lock was acquired in the Exclusive \(X\) lock mode.|
|mongodb.locks.Global.acquireCount\_r| |count|Number of times the global lock was acquired in the Intent Shared \(IS\) lock mode.|
|mongodb.locks.Global.acquireCount\_w| |count|Number of times the global lock was acquired in the Intent Exclusive \(IX\) lock mode.|
|mongodb.locks.Global.acquireCount\_W| |count|Number of times the global lock was acquired in the Exclusive \(X\) lock mode.|
|mongodb.mem.pageFaults| |count|Total number of page faults. The **extra\_info.page\_faults** counter may increase dramatically during moments of poor performance and may correlate with limited memory environments and larger data sets. Limited and sporadic page faults do not necessarily indicate an issue.|
|mongodb.mem.resident \(featured metric\)| |mebibyte|This value is roughly equivalent to the amount of RAM, in mebibyte \(MiB\), currently used by the database process. During normal use, this value tends to grow. In dedicated database servers, the number tends to approach the total amount of system memory.|
|mongodb.mem.virtual| |mebibyte|The quantity, in mebibyte \(MiB\), of virtual memory used by the mongod process.|
|mongodb.metrics.document.deleted| |count|Total number of documents deleted.|
|mongodb.metrics.document.inserted| |count|Total number of documents inserted.|
|mongodb.metrics.document.returned| |count|Total number of documents returned by queries.|
|mongodb.metrics.document.updated| |count|Total number of documents updated.|
|mongodb.metrics.getLastError.wtime\_num \(featured metric\)| |count|Total number of **getLastError** operations with a specified write concern \(w\) that wait for one or more members of a replica set to acknowledge the write operation \(a w value greater than 1.\)|
|mongodb.metrics.getLastError.wtime\_totalMillis \(featured metric\)| |miliseconds|Total amount of time in milliseconds that the mongod has spent performing **getLastError** operations with write concern \(w\) that wait for one or more members of a replica set to acknowledge the write operation \(a w value greater than 1.\)|
|mongodb.metrics.getLastError.wtimeouts \(featured metric\)| |count|Number of times that write concern operations have timed out as a result of the **wtimeout** threshold to **getLastError**. This number increments for both default and non-default write concern specifications.|
|mongodb.metrics.operation.scanAndOrder| |count|Total number of queries that return sorted numbers that cannot perform the sort operation using an index.|
|mongodb.metrics.queryExecutor.scanned| |count|Total number of index items scanned during queries and query-plan evaluation. This counter is the same as **totalKeysExamined** in the output of explain\(\).|
|mongodb.metrics.queryExecutor.scannedObjects| |count|Total number of documents scanned during queries and query-plan evaluation. This counter is the same as **totalDocsExamined** in the output of explain\(\).|
|mongodb.metrics.record.moves| | |A document that reports on data related to record allocation in the on-disk memory files.|
|mongodb.metrics.repl.apply.batches\_num| |count|Total number of batches applied across all databases.|
|mongodb.metrics.repl.apply.batches\_totalMillis| |count|Total amount of time in milliseconds the mongod has spent applying operations from the oplog.|
|mongodb.metrics.repl.apply.ops| |count|Total number of oplog operations applied. **metrics.repl.apply.ops** is incremented after each operation.|
|mongodb.metrics.repl.buffer.count| |count|Current number of operations in the oplog buffer.|
|mongodb.metrics.repl.buffer.maxSizeBytes| |bytes|Maximum size of the buffer. This value is a constant setting in the mongod, and is not configurable.|
|mongodb.metrics.repl.buffer.sizeBytes| |bytes|Current size of the contents of the oplog buffer.|
|mongodb.metrics.repl.network.bytes| |count|Total amount of data read from the replication sync source.|
|mongodb.metrics.repl.network.getmores\_num| |count|Reports the total number of **getmore** operations, which are operations that request an additional set of operations from the replication sync source.|
|mongodb.metrics.repl.network.getmores\_totalMillis| |count|Total amount of time required to collect data from **getmore** operations.|
|mongodb.metrics.repl.network.ops| |count|Total number of operations read from the replication source.|
|mongodb.metrics.repl.network.readersCreated| |count|Total number of oplog query processes created. MongoDB creates a new oplog query any time an error occurs in the connection, including a timeout, or a network operation. Furthermore, **metrics.repl.network.readersCreated** increments every time MongoDB selects a new source for replication.|
|mongodb.metrics.ttl.deletedDocuments| |count|Total number of documents deleted from collections with a **ttl** index.|
|mongodb.metrics.ttl.passes| |count|Total number of documents deleted from collections with a **ttl** index.|
|mongodb.network.bytesIn| |count|Total number of bytes that the server has received over network connections initiated by clients.|
|mongodb.network.bytesOut| |count|Total number of bytes that the server has sent over network connections initiated by clients.|
|mongodb.network.numRequests| |count|Total number of distinct requests that the server has received. Use this value to provide context for the **network.bytesIn** and **network.bytesOut** values to ensure that MongoDB's network utilization is consistent with expectations and application use.|
|mongodb.opcounters.command| |count|Total number of commands issued to the database since the mongod instance last started. **opcounters.command** counts all commands except the write commands: insert, update, and delete.|
|mongodb.opcounters.delete| |count|Total number of delete operations since the mongod instance last started.|
|mongodb.opcounters.getmore| |count|Total number of **getMore** operations since the mongod instance last started. This counter can be high even if the query count is low. Secondary nodes send **getMore** operations as part of the replication process.|
|mongodb.opcounters.insert| |count|Total number of insert operations received since the mongod instance last started.|
|mongodb.opcounters.query| |count|Total number of queries received since the mongod instance last started.|
|mongodb.opcounters.update| |count|Total number of update operations received since the mongod instance last started.|
|mongodb.opcountersRepl.command| |count|Total number of replicated commands issued to the database since the mongod instance last started.|
|mongodb.opcountersRepl.delete| |count|Total number of replicated delete operations since the mongod instance last started.|
|mongodb.opcountersRepl.getmore| |count|Total number of getMore operations since the mongod instance last started.|
|mongodb.opcountersRepl.insert \(featured metric\)| |count|Total number of replicated insert operations since the mongod instance last started.|
|mongodb.opcountersRepl.query \(featured metric\)| |count|Total number of replicated queries since the mongod instance last started.|
|mongodb.opcountersRepl.update| |count|Total number of replicated update operations since the mongod instance last started.|

**Parent Topic:**[Agent Client Collector Monitoring default checks and policies](agent-policies-checks.md)

