---
title: Parallel exports
description: Split outgoing data into multiple export sets and process export sets in parallel to reduce processing time.New topic
locale: en-US
release: australia
product: System Export Sets
classification: system-export-sets
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Export sets, Exports, Workflow Data Fabric]
---

# Parallel exports

Split outgoing data into multiple export sets and process export sets in parallel to reduce processing time.

Running a parallel export can be helpful when exports take a long time due to large datasets with time-consuming scripts.

Parallel export is most effective for exports with 50,000 or more records. If your export doesn't meet the minimum requirements, the system automatically uses standard export processing.

## How parallel exports work

When you enable parallel export, the system splits your data into multiple chunks and processes them concurrently to reduce processing time. The number of chunks depends on your instance node configuration and is calculated as: Number of chunks = \(Number of nodes\) × \(Scale factor\). The default scale factor is one, and a minimum of two chunks is required.

When you run a parallel export, the system creates multiple export sets, up to the value of the **glide.scheduled\_export.min\_rows\_for\_parallel\_export** system property \(default = 10\). For example:

-   A two-node cluster produces four export sets
-   A ten-node cluster produces 10 export sets

Each active node runs two Export Set Processor jobs every minute. These jobs:

1.  Poll the Parallel Export Sets Jobs queue
2.  Pick export sets from the queue
3.  Process the export sets

All jobs run concurrently, depending on the availability of worker threads.

## Parallel export record structure

Each parallel export creates a Parallel Export Set record. The form view shows:

-   All related export sets
-   Parallel export set jobs
-   Export histories

Parallel export requires 50,000 rows by default. This threshold enables parallel processing to be used only for large datasets where it provides significant performance benefits.

To customize this threshold, create the system property **glide.scheduled\_export.min\_rows\_for\_parallel\_export** with an integer value.

When the export runs with parallel export enabled:

-   A parallel export set record is created with a PESO prefix \(example: PESO010001\)
-   Multiple parallel export-set job records are created, one per chunk, with a PESJ prefix \(example: PESJ0010001, PESJ0010002\)
-   Multiple export history records are created, one per chunk
-   Each export history record contains an exported file attachment

The **Parallel Export Set** and **Parallel Export Set Job** fields on the export history records link back to the parallel export set and individual jobs.

Files from parallel exports are stored on the MID Server in a parallel subfolder: `{MID_Server}/agent/export/parallel/{configured_path}/`. File naming format includes the parallel export set number, export set name, timestamp, and sequential file number: Example: `PESO0100001_incident__20251204001638_1.xlsx`. The file number increments for each chunk \(\_1, \_2, \_3, and so on\).

