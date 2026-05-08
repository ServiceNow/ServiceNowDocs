---
title: Data source fields
description: In addition to common fields, other fields appear on the data source form, depending on the value of the Type field.
locale: en-US
release: australia
product: System Import Sets
classification: system-import-sets
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 11
breadcrumb: [Data sources, Import sets, Imports, Workflow Data Fabric]
---

# Data source fields

In addition to common fields, other fields appear on the data source form, depending on the value of the **Type** field.

## Common data source fields

These fields are common to all data sources.

<table id="table_ekt_wp2_h5"><thead><tr><th>

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

The type of data you are importing:-   From a remote **File**
-   From a **JDBC** database
-   Using **LDAP**
-   Using **OIDC**
-   Using **REST** to import data through the Integration Hub
-   From a **Data Stream** action through the Integration Hub
-   Using a **Custom** script

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

Application

</td><td>

Application scope for this record.

</td></tr></tbody>
</table>## File type data source fields

These additional fields appear on the data source form when the **Type** field value is **File**.

<table id="table_kg3_dr2_h5"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Format

</td><td>

Only the default XML-based file format \(.xlsx\) is supported, unless saved as "Strict Open XML Document."

</td></tr><tr><td>

Zipped

</td><td>

Selected if the import file is compressed.

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

The script used to parse a single line of input. As you type the script, script auto-complete presents the choices available to you. For more information, see [File type data sources](r_FileTypeDataSource.md).

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

Selected if child elements of the XML node or JSON object should be converted into additional columns. Unselected if the parent column value should be an XML or JSON fragment. For JSON, note that selecting this option expands objects only, not arrays. For nested array support, see [JSON file import examples](json-data-source-examples.md).

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
</table>## JDBC type data source fields

These additional fields appear on the data source form when the **Type** field value is **JDBC**.

|Field|Description|
|-----|-----------|
|Use MID Server|MID Server to use to connect to this data source.|
|Format|One of the following formats: MySQL, Oracle, or SQLServer.|
|Instance name|Used to support dynamic port connectivity with SQL Server. To ensure connectivity, provide the instance name for a SQL Server that receives a new port number dynamically after each reboot. This field only appears when **SQLServer** is selected as a data source format.|
|Database name|Name of the database instance.|
|Database port|Port number for the database. Leave this field empty when using dynamic port connectivity with SQL Server.|
|Use integrated authentication|Selected to allow the JDBC connection to use the ID of the user configured for the Windows MID Server service for SQL Server authentication. For additional details, see [JDBC type data source](r_JDBCTypeDataSource.md#).|
|Username|User name for authentication on the JDBC server.|
|Password|Password for authentication on the JDBC server.|
|Server|Name of the server from which the tables will be imported.|
|Query|Type of query to run: **All rows from Table** or **Specific SQL**. If you select to run a SQL statement, the SQL statement field appears.|
|Query timeout|Number of seconds the JDBC driver will wait for a query \(SELECT\) to complete. Zero \(0\) means no timeout. If timeout is exceeded, the integration considers the JDBC result inaccessible and places it in an error state.|
|Connection timeout|Number of seconds before MID Server connection cache pool closes and removes it from the pool. Zero \(0\) means no timeout.|
|Table name|Name of the table from which the data is being exported.|
|SQL statement|SQL statement to extract the desired data from the database.|
|Use last run datetime|Controls the amount of data that is retrieved from a database during an import run. If unselected, then all rows in the table specified are imported, every time. You might want to use this setting if this is a one-time import, or if all the data in the target table is new. If selected, two additional fields appear, enabling you to select a datetime value to limit imported data to delta values only.|
|Last run datetime|The datetime value in this field is automatically populated from the database field you select below and represents the latest value from the previous run. This value acts as a dynamic filter to restrict the number of records retrieved to those records that have changed since the data source's last runtime.|
|Last run database field|Field name from the source table that will be used as the filter in the next run. This value may need to be case sensitive, depending on the target database type.|
|Additional Database Parameters|Optional parameters to add to the end of the URL generated for this data source. Semicolon-separated list of parameters. You may need to configure the form to view this field.|

## LDAP type data source field

This additional field appears on the data source form when the **Type** field value is **LDAP**.

|Field|Description|
|-----|-----------|
|LDAP target|Target selected from the list of your LDAP OU definitions.|

## OIDC type data source field

This additional field appears on the data source form when the **Type** field value is **OIDC**.

|Field|Description|
|-----|-----------|
|Format|Defaults to **-- None --** and can't be changed.|

## REST \(Integration Hub\) type data source fields

These additional fields appear on the data source form when the **Type** field value is **REST \(IntegrationHub\)**.

<table id="table_z1s_xfn_y3b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Format

</td><td>

One of the following formats: Custom \(Parse by Script\), JSON, or XML.

</td></tr><tr><td>

Request action

</td><td>

Data source request action that will be invoked to get data. You can choose only published request actions. Click the link in the dialog box below to create/configure a new Data Source request action in Integration Hub. After the request action is published in Integration Hub, you can choose it as a **Request action** in the Data Source record. For more information, see [Define action properties](../task/define-action-properties.md).

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

The script used to parse a single line of input. As you type the script, script auto-complete presents the choices available to you. For more information, see [File type data sources](r_FileTypeDataSource.md).

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

Selected if child elements of the XML node or JSON object should be converted into additional columns. Unselected if the parent column value should be an XML or JSON fragment. For JSON, note that selecting this option expands objects only, not arrays. For nested array support, see [JSON file import examples](json-data-source-examples.md).

</td></tr><tr><td>

Data in single column

</td><td>

Selected to store data in a single column.

</td></tr><tr><td>

Xpath for each row

</td><td>

XPath expression that selects the nodes which become rows in the import table. The children of the selected nodes will become the columns in the rows.

</td></tr></tbody>
</table>## Data Stream \(Integration Hub\) type data source fields

These additional fields appear on the data source form when the **Type** field value is **Data Stream \(IntegrationHub\)**.

<table id="table_yxk_mv4_blb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

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

 This field is only available when the Data Stream action is configured to use a connection alias. For more information, see [Create a Connection and Credential alias](https://www.servicenow.com/docs/access?context=connection-alias&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

Data in single column

</td><td>

Selected to store data in a single column.

</td></tr><tr><td>

Data Stream action inputs

</td><td>

Additional fields may appear, based on the inputs defined in the **Data Stream action**.

</td></tr></tbody>
</table>## Custom \(Load by Script\) type data source field

This additional field appears on the data source form when the **Type** field value is **Custom \(Load by Script\)**.

|Field|Description|
|-----|-----------|
|Data Loader|Script used to load data. For more information, see [Custom \(Load by Script\) type data source](custom-type-data-source.md)|

**Parent Topic:**[Importing data using import sets](../concept/c_ImportDataUsingImportSets.md)

