---
title: Concurrent imports
description: Split incoming data into multiple import sets and transform the import sets concurrently to reduce processing time.
locale: en-US
release: australia
product: System Import Sets
classification: system-import-sets
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Import sets, Imports, Workflow Data Fabric]
---

# Concurrent imports

Split incoming data into multiple import sets and transform the import sets concurrently to reduce processing time.

Running a concurrent import can be helpful when order does not matter and imports take a long time due to large data sets with time-consuming scripts. If order matters, you can split the import into multiple partitions to ensure that each partition is processed in order.

**Note:** Concurrent imports add processing and monitoring overhead. Use them only with large data sets.

Enable concurrent imports only after fine-tuning all other parameters, such as database indexes and transformations.

## Scheduling concurrent imports

You enable concurrent imports by selecting **Concurrent Import** on the Scheduled Data Import form. For instructions, see [Schedule a data import](../task/t_ScheduleADataImport.md).

When the schedule runs a concurrent import, the system pulls the data from databases, Excel spreadsheets, CSV files, or other sources to a temporary staging table, and then transforms the data from the staging table to the target table.

When you run a concurrent import, the system creates multiple import sets, up to the value of the **glide.scheduled\_import.max.concurrent.import\_sets** system property \(default = 10\). For example, a two-node cluster produces four import sets, and a ten-node cluster produces ten import sets.

## Import Set Transformer job

Each active node runs two Import Set Transformer jobs every minute, and those jobs poll the Concurrent Import Sets Jobs queue, pick import sets from the queue, and transform those import sets. All jobs run concurrently, depending on the availability of worker threads.

## Concurrent Import Set record

Each concurrent import creates a Concurrent Import Set record. The form view shows all related import sets, concurrent import set jobs, and transform histories.

You can resume or reprocess any import set. For more information, see [Monitor concurrent import sets](../task/monitor-concurrent-import-sets.md).

## Concurrent Import Sets Jobs queue

After loading data, the system adds the import sets to the Concurrent Import Sets Jobs table. The Concurrent Import Sets Jobs table indicates the job type and status of each concurrent import set job.

For more information, see [Monitor concurrent import set jobs](../task/monitor-concurrent-import-set-jobs.md).

## Partitioning concurrent imports

You can partition import sets to maintain the processing order within each partition.

By default, the system allocates records to import sets in a round robin fashion. However, you can write a custom script to define a custom partition key that identifies the target import set. Every row with the same partition key adds to the same import set, and the data in that import set is processed in sequential order.

## Hierarchical imports

You can create a scheduled import set hierarchy by scheduling an import to run after another import set completes. One parent scheduled import can have many child scheduled imports, and each child scheduled import executes in the order specified. For concurrent scheduled imports, child scheduled imports can be started only after all Import Set Transformer jobs complete.

The last Import Set Transformer job starts the next import in the hierarchy.

The system generates an execution plan at the beginning of parent import process. Each import process uses the execution plan to fetch the next process to invoke. For concurrent imports, the last Import Set Transformer job fetches the next import and executes it.

## Synchronized inserts

Coalesce fields help define uniqueness among records. The transformation process checks for an existing record with the coalesce values and updates the existing record, if it exists, or inserts a new record if none exists. For more information, see [Updating records using coalesce](c_ImportSetCoalesce.md).

By default, concurrent imports allow each running import set to insert new records. When an import set inserts a record, it establishes a write lock on the target table to prevent other import sets from inserting the same record.

## Tables for concurrent imports

|Table|Description|
|-----|-----------|
|Concurrent Import Set \(sys\_concurrent\_import\_set\)|Stores details of each concurrent import set in import set records.|
|Concurrent Import Set Jobs \(sys\_concurrent\_import\_set\_job\)|Lists the import sets to be processed.|
|Execution Context for Scheduled import \(sys\_execution\_context\)|Specifies the execution context for each scheduled import. The execution context specifies the next scheduled import to use when processing a hierarchical scheduled import.|
|Hierarchical scheduled import execution plan \(sys\_execution\_plan\).|Stores the execution plan for hierarchical imports. The execution plan is a tree structure that identifies which scheduled import runs after the preceding scheduled input.|

## Domain Separation with concurrent imports

You can add the sys\_domain field to a scheduled import table to enable domain separation for the import set. Both import set loading and transform jobs run in the domain specified in the scheduled import set job.

