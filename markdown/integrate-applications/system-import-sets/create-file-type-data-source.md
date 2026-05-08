---
title: Create a File type data source
description: Create a File type data source record to define what data an import set should import.
locale: en-US
release: australia
product: System Import Sets
classification: system-import-sets
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Create a data source, Data sources, Import sets, Imports, Workflow Data Fabric]
---

# Create a File type data source

Create a **File** type data source record to define what data an import set should import.

## Before you begin

Role required: import\_admin

## About this task

For additional information, see [File type data sources](../reference/r_FileTypeDataSource.md).

## Procedure

1.  Navigate to **All** &gt; **System Import Sets** &gt; **Administration** &gt; **Data Sources**.

2.  Click **New**.

3.  Complete the form.

<table id="table_wpk_1v3_z3b"><thead><tr><th>

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

**File**.

</td></tr><tr><td>

Format

</td><td>

Only the default XML-based file format \(.xlsx\) is supported, unless saved as "Strict Open XML Document."

</td></tr><tr><td>

Zipped

</td><td>

Selected if the import file is compressed.

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

File retrieval method

</td><td>

The retrieval method for this file.

</td></tr><tr><td>

File path

</td><td>

The path to the file to import.You can include a system property value in this field using the format `${system.property.name}`. When the connection is made, the variable is replaced with the value of the specified property.

**Note:** For files retrieved using HTTP or HTTPS, the **glide.ds.file.http.variable\_replacement** property must be true to use system property expansion.

 For example, you can specify the **File path** value `/countries.csv?key=${datasource.apikey}`. When the connection is made, the value of the **datasource.apikey** system property is passed as the value for the **key** parameter.

 **Note:** For HTTP and HTTPS protocols, the file path is automatically URL encoded. Do not specify a URL-encoded file path when using either of these protocols.

</td></tr><tr><td>

CSV delimiter

</td><td>

The delimiter character for the CSV file.

</td></tr><tr><td>

Parsing script

</td><td>

The script used to parse a single line of input. As you type the script, script auto-complete presents the choices available to you. For more information, see [File type data sources](../reference/r_FileTypeDataSource.md).

</td></tr><tr><td>

Sheet number

</td><td>

The Excel sheet number to load data.

</td></tr><tr><td>

Header row

</td><td>

The Excel row number to load the column labels.

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

</td></tr><tr><td>

SCP authentication method

</td><td>

Choice to authenticate with a username and password or with a public key.**Note:** You cannot authenticate to data sources with a public-private key pair. Use a username and password authentication instead.

</td></tr><tr><td>

Server

</td><td>

Name of the server from which the tables will be imported.

</td></tr><tr><td>

Port

</td><td>

Port to use to connect to the specified server. This field appears if you select HTTP or HTTPS as the file retrieval method.

</td></tr><tr><td>

Username

</td><td>

User name for authentication on the JDBC server.

</td></tr><tr><td>

Password

</td><td>

Password for authentication on the JDBC server.

</td></tr><tr><td>

Private keyfile

</td><td>

Keyfile when using legacy SCP public-private keyfiles. **Note:**

-   You cannot authenticate to data sources with a public-private key pair. Use username and password authentication instead.
-   Do not use this legacy option. Although it is available for use, it is not supported.


</td></tr><tr><td>

System keystore

</td><td>

Selected to validate the certificate from the FTPS server against all saved certificates. This certificate may be any type supported by the instance. If not selected, the instance uses the Java default certificate to validate the FTPS server. This field is available only for data sources with a **File retrieval method** value of **FTPS**. All FTPS file retrieval methods are supported, including Auth TLS, Auth SSL, Implicit SSL, and Implicit TLS.

</td></tr></tbody>
</table>4.  Click **Submit**.


## What to do next

Define a transform map for the new data source and run an import.

**Parent Topic:**[Create a data source](../concept/c_CreateNewDataSource.md)

