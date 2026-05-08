---
title: Create a Custom \(Load by Script\) type data source
description: Create a Custom \(Load by Script\) type data source record to define what data an import set should import.
locale: en-US
release: australia
product: System Import Sets
classification: system-import-sets
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Create a data source, Data sources, Import sets, Imports, Workflow Data Fabric]
---

# Create a Custom \(Load by Script\) type data source

Create a **Custom \(Load by Script\)** type data source record to define what data an import set should import.

## Before you begin

Role required: import\_admin

## About this task

For additional information, see [Custom \(Load by Script\) type data source](../reference/custom-type-data-source.md).

## Procedure

1.  Navigate to **All** &gt; **System Import Sets** &gt; **Administration** &gt; **Data Sources**.

2.  Click **New**.

3.  Complete the form.

<table id="table_ih5_mbj_z3b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

A unique name for this data source.

</td></tr><tr><td>

Import set table label

</td><td>

A label for the import set staging table to use.

</td></tr><tr><td>

Import set table name

</td><td>

The ServiceNow AI Platform uses the label you entered to construct a unique table name. This prevents namespace collision with an already existing table.

</td></tr><tr><td>

Type

</td><td>

**Custom \(Load by Script\)**.

</td></tr><tr><td>

Use Batch Import

</td><td>

If selected, specifies that loading data should be batched when you click **Load data** or **Test load 20 records**.

</td></tr><tr><td>

Batch Size

</td><td>

Specifies how big the batches should be. Appears only when the **Use Batch Import** field is selected.The **glide.import\_set\_load\_usebatch** and **glide.import\_set\_load\_batch\_size** properties affects these fields. The priority order for the properties and fields are as follows: If the property is set, use the property value. If not, use the field value. If neither property is set, use the default batch size of 1000.

-   For example, if **glide.import\_set\_load\_usebatch** = **true** and **glide.import\_set\_load\_batch\_size** = **200**, use 200 as the batch size, regardless of the field values.
-   For example, if **glide.import\_set\_load\_usebatch** = **true** and the **glide.import\_set\_load\_batch\_size** property is not set, use the default batch size of 1000.
-   For example, if the **glide.import\_set\_load\_usebatch** property is not set and the **Use Batch Import** field = **true**, use the **Batch Size** field value \(or the default of 1000 if the **Batch Size** field value is not set\)
-   For example, if the **glide.import\_set\_load\_usebatch** property = false and the **Use Batch Import** field = true, do not use batch import, since the property is set to false.


</td></tr><tr><td>

Enable parallel loading

</td><td>

Option to use parallel data loading.

</td></tr><tr><td>

Parallel loading script

</td><td>

Script used for parallel data loading. Appears only when **Enable parallel loading** is selected. For more information, see [Custom \(Load by Script\) type data source](../reference/custom-type-data-source.md).

</td></tr><tr><td>

Data Loader

</td><td>

Script used to load data. For more information, see [Custom \(Load by Script\) type data source](../reference/custom-type-data-source.md).

</td></tr></tbody>
</table>4.  Click **Submit**.


## What to do next

Define a transform map for the new data source and run an import.

**Parent Topic:**[Create a data source](../concept/c_CreateNewDataSource.md)

