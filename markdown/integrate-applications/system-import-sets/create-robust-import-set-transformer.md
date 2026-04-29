---
title: Create a robust import set transformer
description: Define how information is sent from the source table to target tables via a Robust Transform Engine \(RTE\).
locale: en-US
release: australia
product: System Import Sets
classification: system-import-sets
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Robust Import Set Transformers, Import sets, Imports, Workflow Data Fabric]
---

# Create a robust import set transformer

Define how information is sent from the source table to target tables via a Robust Transform Engine \(RTE\).

## Before you begin

-   Role required: import\_transformer
-   [Create an ETL definition](create-etl-definitions.md).
-   [Create a robust transform definition](create-robust-transform-definitions.md).

## Procedure

1.  Navigate to **All** &gt; **System Import Sets** &gt; **Administration** &gt; **Robust Import Set Transformers**.

2.  Click **New**.

3.  Complete the form.

<table id="table_ynf_5jl_cjb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The name of the robust import set transformer.

</td></tr><tr><td>

Source table

</td><td>

The source table for the robust import set transformer.

</td></tr><tr><td>

Robust transform engine

</td><td>

Enables you to select an ETL definition or CMDB definition. For procedures to define an RTE, see [Create robust transform definitions](create-robust-transform-definitions.md).

</td></tr><tr><td>

Description

</td><td>

A description of the robust import set transformer.

</td></tr><tr><td>

Properties

</td><td>

Custom properties which can be used in processing the data.

</td></tr><tr><td>

Application

</td><td>

Application scope for this record.

</td></tr><tr><td>

Active

</td><td>

Selected if the robust import set transformer is currently active. Deselected if the robust import set transformer is not currently active.

</td></tr><tr><td>

Batch size

</td><td>

The number of import set rows the system processes at a time. For example, if an import set has 1000 rows and the batch size is 100, the system processes 10 batches of 100 rows each.

 The minimum batch size is 1. The maximum batch size depends on the row size and processing complexity. Consider starting with a batch size of 100 and adjusting from there.

</td></tr><tr><td>

Verbose

</td><td>

Enables some transform logs that show how transform operations are applied to records.

</td></tr></tbody>
</table>4.  Click **Submit**.


