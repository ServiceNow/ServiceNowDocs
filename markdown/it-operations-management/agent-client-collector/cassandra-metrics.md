---
title: Cassandra metrics
description: The following table lists the metrics that are gathered as output from Cassandra checks. Entries indicated as Featured metrics are high-visibility metrics that are displayed in the Operator Workspace Metric tab after an alert is generated. These metrics provide the operator with additional information to help them further explore the specified issue.
locale: en-US
release: xanadu
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [Agent Client Collector Monitoring default checks and policies, Agent Client Collector Monitoring reference, Agent Client Collector Monitoring, Agent Client Collector, IT Operations Management]
---

# Cassandra metrics

The following table lists the metrics that are gathered as output from Cassandra checks. Entries indicated as **Featured metrics** are high-visibility metrics that are displayed in the Operator Workspace Metric tab after an alert is generated. These metrics provide the operator with additional information to help them further explore the specified issue.

|Metric type|Resource \(name of specific database, where relevant\)|Units|Metric type description|
|-----------|------------------------------------------------------|-----|-----------------------|
|cassandra.load \(featured metric\)| |byte|The disk space used by live data on a node.|
|cassandra.uptime \(featured metric\)| |seconds| |
|cassandra.heap.used \(featured metric\)| |byte| |
|cassandra.heap.total \(featured metric\)| |byte| |
|cassandra.exceptions| |count|Number of internal exceptions caught. Under normal exceptions this should be zero.|
|cassandra.key\_cache.size| |byte|Total size of occupied cache, in bytes.|
|cassandra.key\_cache.capacity| |byte|Cache capacity in bytes.|
|cassandra.key\_cache.hits| |count|Total number of cache hits.|
|cassandra.key\_cache.requests \(featured metric\)| |count|Total number of cache requests.|
|cassandra.key\_cache.hit\_rate \(featured metric\)| |count|All time cache hit rate.|
|cassandra.compactionstats.pending\_tasks| |count|The number of pending compactions.|
|cassandra.threadpool.ReadStage.active| |count|Number of tasks being actively worked on by this pool. Local reads run on this thread pool on this ReadStage.|
|cassandra.threadpool.ReadStage.pending| |count|Number of queued tasks queued up on this pool.|
|cassandra.threadpool.ReadStage.completed| |count|Number of tasks completed.|
|cassandra.threadpool.ReadStage.blocked| |count|Number of tasks that were blocked due to queue saturation.|
|cassandra.threadpool.MiscStage.active| |count|Number of tasks being actively worked on by this pool. Miscellaneous tasks run on this stage.|
|cassandra.threadpool.MiscStage.pending| |count|Number of queued tasks queued up on this pool.|
|cassandra.threadpool.MiscStage.completed| |count|Number of tasks completed.|
|cassandra.threadpool.MiscStage.blocked| |count|Number of tasks that were blocked due to queue saturation.|
|cassandra.threadpool.CompactionExecutor.active| |count|Number of tasks being actively worked on by this pool. Compactions are run on these threads.|
|cassandra.threadpool.CompactionExecutor.pending| |count|Number of queued tasks queued up on this pool.|
|cassandra.threadpool.CompactionExecutor.completed| |count|Number of tasks completed.|
|cassandra.threadpool.CompactionExecutor.blocked| |count|Number of tasks that were blocked due to queue saturation.|
|cassandra.threadpool.MutationStage.active| |count|Number of tasks being actively worked on by this pool. Responsible for all other writes.|
|cassandra.threadpool.MutationStage.pending| |count|Number of queued tasks queued up on this pool.|
|cassandra.threadpool.MutationStage.completed| |count|Number of tasks completed.|
|cassandra.threadpool.MutationStage.blocked| |count|Number of tasks that were blocked due to queue saturation.|
|cassandra.threadpool.MemtableReclaimMemory.active| |count|Number of tasks being actively worked on by this pool. Memtable recycling.|
|cassandra.threadpool.MemtableReclaimMemory.pending| |count|Number of queued tasks queued up on this pool.|
|cassandra.threadpool.MemtableReclaimMemory.completed| |count|Number of tasks completed.|
|cassandra.threadpool.MemtableReclaimMemory.blocked| |count|Number of tasks that were blocked due to queue saturation.|
|cassandra.threadpool.PendingRangeCalculator.active| |count|Number of tasks being actively worked on by this pool. Calculates token range.|
|cassandra.threadpool.PendingRangeCalculator.pending| |count|Number of queued tasks queued up on this pool.|
|cassandra.threadpool.PendingRangeCalculator.completed| |count|Number of tasks completed.|
|cassandra.threadpool.PendingRangeCalculator.blocked| |count|Number of tasks that were blocked due to queue saturation.|
|cassandra.threadpool.GossipStage.active| |count|Number of tasks being actively worked on by this pool. Handles gossip requests.|
|cassandra.threadpool.GossipStage.pending| |count|Number of queued tasks queued up on this pool.|
|cassandra.threadpool.GossipStage.completed| |count|Number of tasks completed.|
|cassandra.threadpool.GossipStage.blocked| |count|Number of tasks that were blocked due to queue saturation.|
|cassandra.threadpool.SecondaryIndexManagement.active| |count|Number of tasks being actively worked on by this pool. Performs updates to secondary indexes.|
|cassandra.threadpool.SecondaryIndexManagement.pending| |count|Number of queued tasks queued up on this pool.|
|cassandra.threadpool.SecondaryIndexManagement.completed| |count|Number of tasks completed.|
|cassandra.threadpool.SecondaryIndexManagement.blocked| |count|Number of tasks that were blocked due to queue saturation.|
|cassandra.threadpool.HintsDispatcher.active| |count|Number of tasks being actively worked on by this pool. Performs hinted hand off.|
|cassandra.threadpool.HintsDispatcher.pending| |count|Number of queued tasks queued up on this pool.|
|cassandra.threadpool.HintsDispatcher.completed| |count|Number of tasks completed.|
|cassandra.threadpool.HintsDispatcher.blocked| |count|Number of tasks that were blocked due to queue saturation.|
|cassandra.threadpool.RequestResponseStage.active| |count|Number of tasks being actively worked on by this pool. Coordinator requests to the cluster run on this thread pool.|
|cassandra.threadpool.RequestResponseStage.pending| |count|Number of queued tasks queued up on this pool.|
|cassandra.threadpool.RequestResponseStage.completed| |count|Number of tasks completed.|
|cassandra.threadpool.RequestResponseStage.blocked| |count|Number of tasks that were blocked due to queue saturation.|
|cassandra.threadpool.ReadRepairStage.active| |count|Number of tasks being actively worked on by this pool. Read repair happens on this thread pool.|
|cassandra.threadpool.ReadRepairStage.pending| |count|Number of queued tasks queued up on this pool.|
|cassandra.threadpool.ReadRepairStage.completed| |count|Number of tasks completed.|
|cassandra.threadpool.ReadRepairStage.blocked| |count|Number of tasks that were blocked due to queue saturation.|
|cassandra.threadpool.CounterMutationStage.active| |count|Number of tasks being actively worked on by this pool. Responsible for counter writes.|
|cassandra.threadpool.CounterMutationStage.pending| |count|Number of queued tasks queued up on this pool.|
|cassandra.threadpool.CounterMutationStage.completed| |count|Number of tasks completed.|
|cassandra.threadpool.CounterMutationStage.blocked| |count|Number of tasks that were blocked due to queue saturation.|
|cassandra.threadpool.MigrationStage.active| |count|Number of tasks being actively worked on by this pool. Runs schema migrations.|
|cassandra.threadpool.MigrationStage.pending| |count|Number of queued tasks queued up on this pool.|
|cassandra.threadpool.MigrationStage.completed| |count|Number of tasks completed.|
|cassandra.threadpool.MigrationStage.blocked| |count|Number of tasks that were blocked due to queue saturation.|
|cassandra.threadpool.MemtablePostFlush.active| |count|Number of tasks being actively worked on by this pool. Cleans up commit log after memtable is written to disk.|
|cassandra.threadpool.MemtablePostFlush.pending| |count|Number of queued tasks queued up on this pool.|
|cassandra.threadpool.MemtablePostFlush.completed| |count|Number of tasks completed.|
|cassandra.threadpool.MemtablePostFlush.blocked| |count|Number of tasks that were blocked due to queue saturation.|
|cassandra.threadpool.PerDiskMemtableFlushWriter\_0.active| |count|Number of tasks being actively worked on by this pool. Responsible for writing a spec \(there is one of these per disk 0-N\).|
|cassandra.threadpool.PerDiskMemtableFlushWriter\_0.pending| |count|Number of queued tasks queued up on this pool.|
|cassandra.threadpool.PerDiskMemtableFlushWriter\_0.completed| |count|Number of tasks completed.|
|cassandra.threadpool.PerDiskMemtableFlushWriter\_0.blocked| |count|Number of tasks that were blocked due to queue saturation.|
|cassandra.threadpool.ValidationExecutor.active| |count|Number of tasks being actively worked on by this pool. Performs validation compaction or scrubbing.|
|cassandra.threadpool.ValidationExecutor.pending| |count|Number of queued tasks queued up on this pool.|
|cassandra.threadpool.ValidationExecutor.completed| |count|Number of tasks completed.|
|cassandra.threadpool.ValidationExecutor.blocked| |count|Number of tasks that were blocked due to queue saturation.|
|cassandra.threadpool.Sampler.active| |count|Number of tasks being actively worked on by this pool. Responsible for re-sampling the index summaries of **SStables**.|
|cassandra.threadpool.Sampler.pending| |count|Number of queued tasks queued up on this pool.|
|cassandra.threadpool.Sampler.completed| |count|Number of tasks completed.|
|cassandra.threadpool.Sampler.blocked| |count|Number of tasks that were blocked due to queue saturation.|
|cassandra.threadpool.MemtableFlushWriter.active| |count|Number of tasks being actively worked on by this pool. Writes memtables to disk.|
|cassandra.threadpool.MemtableFlushWriter.pending| |count|Number of queued tasks queued up on this pool.|
|cassandra.threadpool.MemtableFlushWriter.completed| |count|Number of tasks completed.|
|cassandra.threadpool.MemtableFlushWriter.blocked| |count|Number of tasks that were blocked due to queue saturation.|
|cassandra.threadpool.InternalResponseStage.active| |count|Number of tasks being actively worked on by this pool. Responsible for intra-cluster callbacks.|
|cassandra.threadpool.InternalResponseStage.pending| |count|Number of queued tasks queued up on this pool.|
|cassandra.threadpool.InternalResponseStage.completed| |count|Number of tasks completed.|
|cassandra.threadpool.InternalResponseStage.blocked| |count|Number of tasks that were blocked due to queue saturation.|
|cassandra.threadpool.ViewMutationStage.active| |count|Number of tasks being actively worked on by this pool. Responsible for materialized view writes.|
|cassandra.threadpool.ViewMutationStage.pending| |count|Number of queued tasks queued up on this pool.|
|cassandra.threadpool.ViewMutationStage.completed| |count|Number of tasks completed.|
|cassandra.threadpool.ViewMutationStage.blocked| |count|Number of tasks that were blocked due to queue saturation.|
|cassandra.threadpool.AntiEntropyStage.active| |count|Number of tasks being actively worked on by this pool. Builds merkle tree for repairs.|
|cassandra.threadpool.AntiEntropyStage.pending| |count|Number of queued tasks queued up on this pool.|
|cassandra.threadpool.AntiEntropyStage.completed| |count|Number of tasks completed.|
|cassandra.threadpool.AntiEntropyStage.blocked| |count|Number of tasks that were blocked due to queue saturation.|
|cassandra.threadpool.CacheCleanupExecutor.active| |count|Number of tasks being actively worked on by this pool. Cache maintenance performed on this thread pool.|
|cassandra.threadpool.CacheCleanupExecutor.pending| |count|Number of queued tasks queued up on this pool.|
|cassandra.threadpool.CacheCleanupExecutor.completed| |count|Number of tasks completed.|
|cassandra.threadpool.CacheCleanupExecutor.blocked| |count|Number of tasks that were blocked due to queue saturation.|
|cassandra.message\_type.READ.dropped| |count|Number of dropped messages. Regular reads.|
|cassandra.message\_type.RANGE\_SLICE.dropped| |count|Number of dropped messages. Token range read.|
|cassandra.message\_type.\_TRACE.dropped| |count|Number of dropped messages. Tracing writes.|
|cassandra.message\_type.HINT.dropped| |count|Number of dropped messages. Hint replay.|
|cassandra.message\_type.MUTATION.dropped| |count|Number of dropped messages. Regular writes.|
|cassandra.message\_type.COUNTER\_MUTATION.dropped| |count|Number of dropped messages. Counter writes.|
|cassandra.message\_type.BATCH\_STORE.dropped| |count|Number of dropped messages. Batchlog write.|
|cassandra.message\_type.BATCH\_REMOVE.dropped| |count|Number of dropped messages. Batchlog cleanup \(after successfully applied\).|
|cassandra.message\_type.REQUEST\_RESPONSE.dropped| |count|Number of dropped messages. RPC Callbacks.|
|cassandra.message\_type.PAGED\_RANGE.dropped| |count|Number of dropped messages. Paged read.|
|cassandra.message\_type.READ\_REPAIR.dropped| |count|Number of dropped messages. Read repair.|
|cassandra.system\_traces.read\_count| |count|Number of read for this table.|
|cassandra.system\_traces.read\_latency| | |Local read latency for this table.|
|cassandra.system\_traces.write\_count| |count|Number of writes for this table.|
|cassandra.system\_traces.write\_latency| | |Local write latency for this table.|
|cassandra.system\_traces.pending\_flushes| |count|Estimated number of flush tasks pending for this table.|
|cassandra.system.read\_count \(featured metric\)| |count| |
|cassandra.system.read\_latency \(featured metric\)| |microseconds| |
|cassandra.system.write\_count \(featured metric\)| |count| |
|cassandra.system.write\_latency \(featured metric\)| |microseconds| |
|cassandra.system.pending\_flushes| |count| |
|cassandra.system\_distributed.read\_count| |count| |
|cassandra.system\_distributed.read\_latency| | | |
|cassandra.system\_distributed.write\_count| |count| |
|cassandra.system\_distributed.write\_latency| | | |
|cassandra.system\_distributed.pending\_flushes| |count| |
|cassandra.system\_schema.read\_count| |count| |
|cassandra.system\_schema.read\_latency| | | |
|cassandra.system\_schema.write\_count| |count| |
|cassandra.system\_schema.write\_latency| | | |
|cassandra.system\_schema.pending\_flushes| |count| |
|cassandra.system\_auth.read\_count| |count| |
|cassandra.system\_auth.read\_latency| | | |
|cassandra.system\_auth.write\_count| |count| |
|cassandra.system\_auth.write\_latency| | | |
|cassandra.system\_auth.pending\_flushes| |count| |

**Parent Topic:**[Agent Client Collector Monitoring default checks and policies](agent-policies-checks.md)

