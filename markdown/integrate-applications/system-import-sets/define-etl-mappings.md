---
title: Define ETL entity mappings
description: Map the source entity to a target entity.
locale: en-US
release: xanadu
product: System Import Sets
classification: system-import-sets
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Create Extract Transform Load \(ETL\) definitions, Robust Import Set Transformers, Import sets, Imports, Creating integrations with applications]
---

# Define ETL entity mappings

Map the source entity to a target entity.

## Before you begin

Role required: import\_transformer

## About this task

You can optionally set the **Ignore** check box to exclude the entity mapping when performing data integrations using Robust Import Set Transformation \(RTE\).

## Procedure

1.  Navigate to **All** &gt; **System Import Sets** &gt; **Administration** &gt; **ETL Definitions**.

2.  Select an ETL definition.

3.  On the RTE Entity Mappings tab, click **New**.

4.  Complete the form.

<table id="table_qpv_j3v_3jb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the mapping.

</td></tr><tr><td>

Source Entity

</td><td>

Source entity for the mapping.

</td></tr><tr><td>

Target Entity

</td><td>

Target entity for the mapping.

</td></tr><tr><td>

Order

</td><td>

Order in which the mapping should be processed.

</td></tr><tr><td>

Is Conditional

</td><td>

Check box that designates that the mapping is conditional. Select the check box if the mapping is conditional and clear it if it is not.

</td></tr><tr><td>

Condition Script

</td><td>

Script that defines the conditions that must be met for the mapping. For an example of a conditional script, see [Temporary entity model](../concept/temp-entity-model.md).

</td></tr><tr id="application"><td>

Application

</td><td>

Application scope for this record.

</td></tr><tr><td>

Definition

</td><td>

Selected ETL entity that this mapping belongs to.

</td></tr><tr><td>

Ignore

</td><td>

Check box that designates if this ETL entity mapping should be ignored when performing data integrations using Robust Import Set Transformation \(RTE\). Select this check box if this ETL entity mapping should be ignored when running data integrations using RTE. Clear the check box if it should not \(default\).

 To learn more about data integrations, see:

-   [Importing data using import sets](../concept/c_ImportDataUsingImportSets.md)
-   [Robust Import Set Transformers](../concept/robust-import-set-transformers.md)


</td></tr></tbody>
</table>
