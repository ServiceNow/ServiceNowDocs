---
title: Parallel exports
description: Split outgoing data into multiple export sets and process them in parallel to reduce processing time.New topic
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/system-export-sets/parallel-exports.html
release: australia
product: System Export Sets
classification: system-export-sets
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Export sets, Exports, Workflow Data Fabric]
---

# Parallel exports

Split outgoing data into multiple export sets and process them in parallel to reduce processing time.

Use parallel exports when exports take a long time due to large datasets with time-consuming scripts.

Parallel export is most effective for exports with 50,000 or more records. This is controlled by the **glide.scheduled\_export.min\_rows\_for\_parallel\_export** property \(default = 50,000\). If your export has fewer rows than this threshold, the system automatically uses standard export processing.

## How parallel exports work

When you enable parallel export, the system splits the data into multiple chunks and processes them concurrently. The number of chunks processed depends on available worker threads in the parallel job queue. Each chunk is queued as a separate Parallel Export Set Job and processed as worker threads become available.

Parallel export set jobs are processed via a shared queue. Processing depends on:

1.  Available worker threads in the job queue
2.  Queue polling and job pickup by available workers
3.  Concurrent execution as worker threads become available

All jobs run concurrently, depending on the availability of worker threads.

## Parallel export record structure

Each parallel export creates a Parallel Export Set record. The form view shows:

-   All related export sets
-   Parallel export set jobs
-   Export histories

By default, parallel export requires 50,000 rows. This threshold enables parallel processing to be used only for large datasets where it provides significant performance benefits.

To customize this threshold, create the system property **glide.scheduled\_export.min\_rows\_for\_parallel\_export** with an integer value.

When the export runs with parallel export enabled:

-   A parallel export set record is created with a PES prefix \(for example, `PES010001`\)
-   Multiple parallel export-set job records are created, one per chunk, with a PESJ prefix \(for example, `PESJ010001`, `PESJ010002`\)
-   Multiple export history records are created, one per chunk
-   Each export history record contains an exported file attachment

The **Parallel Export Set** and **Parallel Export Set Job** fields on the export history records link back to the parallel export set and individual jobs.

Files from parallel exports are stored on the MID Server in a parallel sub-folder: `{MID_Server}/agent/export/parallel/{configured_path}/`. File naming format includes the parallel export set number, export set name, timestamp, and sequential file number: For example: `PES0100001_incident__20251204001638_1.xlsx`. The file number increments for each chunk \(\_1, \_2, \_3, and so on\).

