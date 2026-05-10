---
title: Create a REST \(Integration Hub\) type data source
description: Create a REST \(IntegrationHub\) type data source record to define what data an import set should import from a REST API.
locale: en-US
release: australia
product: System Import Sets
classification: system-import-sets
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Create a data source, Data sources, Import sets, Imports, Workflow Data Fabric]
---

# Create a REST \(Integration Hub\) type data source

Create a **REST \(IntegrationHub\)** type data source record to define what data an import set should import from a REST API.

## Before you begin

Roles required: import\_admin and action\_designer

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

**REST \(IntegrationHub\)**.

</td></tr><tr><td>

Format

</td><td>

One of the following formats: Custom \(Parse by Script\), JSON, or XML.

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

Request action

</td><td>

Data source request action that will be invoked to get data. You can choose only published request actions. Click the link in the dialog box below to create/configure a new Data Source request action in Integration Hub. After the request action is published in Integration Hub, you can choose it as a **Request action** in the Data Source record. For more information, see [Define action properties](define-action-properties.md).

</td></tr><tr><td>

Support pagination

</td><td>

Selected to enable pagination for the request action. Pagination helps you reduce processing overhead by processing a specified number of records at a time, instead of processing all records at once.

</td></tr><tr><td>

Limit

</td><td>

Maximum number of records per page. For example, to process 50 records at a time, enter a **Limit** of 50.

</td></tr><tr><td>

Offset

</td><td>

The initial offset used for pagination. The offset is the starting record number. For example, to process 50 records at a time, starting with the first record, enter a **Limit** of 50 and an **Offset** of 0.

</td></tr><tr><td>

Parsing script

</td><td>

Type the script used to parse a single line of input. Three parameters are available in this function:-   **line**: the current line to be parsed by the script
-   **lineNumber**: the line number of the current line in the entire response payload
-   **result**: output result


</td></tr><tr><td>

Path for each row

</td><td>

The path expression used to select JSON objects, which will become rows in the import set table. The path should be `//` for JSON objects.

</td></tr><tr><td>

Discard Arrays

</td><td>

Selected to discard JSON arrays as a value. Unselected to serialize JSON arrays as a value.

</td></tr><tr><td>

Expand node children

</td><td>

Selected if child elements of the XML node or JSON object should be converted into additional columns. Unselected if the parent column value should be an XML or JSON fragment. For JSON, note that selecting this option expands objects only, not arrays. For nested array support, see [JSON file import examples](../reference/json-data-source-examples.md).

</td></tr><tr><td>

Data in single column

</td><td>

Selected to store data in a single column.

</td></tr><tr><td>

Xpath for each row

</td><td>

XPath expression that selects the nodes which become rows in the import table. The children of the selected nodes will become the columns in the rows.

</td></tr></tbody>
</table>4.  Click **Submit**.


## What to do next

Define a transform map for the new data source and run an import.

-   **[Define action properties](define-action-properties.md)**  
Create and configure a Data Source request action in Integration Hub. After the request action is published in Integration Hub, you can choose it as a **Request action** in the Data Source record.

**Parent Topic:**[Create a data source](../concept/c_CreateNewDataSource.md)

