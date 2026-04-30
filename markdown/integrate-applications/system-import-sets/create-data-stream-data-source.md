---
title: Create a Data Stream \(Integration Hub\) type data source
description: Create a Data Stream \(IntegrationHub\) type data source record to define what complex data an import set should import from a Data Stream action.
locale: en-US
release: yokohama
product: System Import Sets
classification: system-import-sets
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Create a data source, Data sources, Import sets, Imports, Data and Automation]
---

# Create a Data Stream \(Integration Hub\) type data source

Create a **Data Stream \(IntegrationHub\)** type data source record to define what complex data an import set should import from a Data Stream action.

## Before you begin

Role required: import\_admin and action\_designer

## Procedure

1.  Navigate to **All** &gt; **System Import Sets** &gt; **Administration** &gt; **Data Sources**.

2.  Click **New**.

3.  Complete the form.

<table id="table_e4j_sz3_z3b"><thead><tr><th>

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

Data Stream \(Integration Hub\) type data source.

</td></tr><tr><td>

Data Stream action

</td><td>

-   ![Select Data Stream action](../image/select-data-stream-action.png) Selected to use an existing published Data Stream action from Integration Hub.
-   ![Select published Data Stream action or create new Data Stream action](../image/create-data-stream-action.png) Selected for one of the following reasons:
    -   If you select a published Data Stream action, click this button to open the Data Stream action in Integration Hub.
    -   If you don't select a Data Stream action, click this button to create and publish a new Data Stream action in Integration Hub.
 **Note:** Data Stream actions require a subscription for production use.

</td></tr><tr><td>

Connection

</td><td>

Specify the connection alias for the Data Stream action. You can use the default parent alias or select any of its children's aliases. Available child aliases are listed in the menu.

 This field is only available when the Data Stream action is configured to use a connection alias. For more information, see [Create a Connection and Credential alias](https://www.servicenow.com/docs/access?context=connection-alias&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

</td></tr><tr><td>

Data in single column

</td><td>

Selected to store data in a single column.

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

Data Stream action inputs

</td><td>

Additional fields may appear, based on the inputs defined in the **Data Stream action**.

</td></tr></tbody>
</table>4.  Click **Submit**.


## What to do next

Define a transform map for the new data source and run an import.

