---
title: Create a JDBC type data source
description: Create a JDBC type data source record to define what data an import set should import.
locale: en-US
release: australia
product: System Import Sets
classification: system-import-sets
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Create a data source, Data sources, Import sets, Imports, Workflow Data Fabric]
---

# Create a JDBC type data source

Create a **JDBC** type data source record to define what data an import set should import.

## Before you begin

Role required: import\_admin

## About this task

For additional information, see [JDBC type data source](../reference/r_JDBCTypeDataSource.md#).

## Procedure

1.  Navigate to **All** &gt; **System Import Sets** &gt; **Administration** &gt; **Data Sources**.

2.  Click **New**.

3.  Complete the form.

<table id="table_tpf_3x3_z3b"><thead><tr><th>

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

**JDBC**.

</td></tr><tr><td>

Use import connection alias

</td><td>

Option to use per-configured connection details.

</td></tr><tr><td>

Import connection alias

</td><td>

Connection alias to use to connect to this data source. For additional details, see [Create an import connection alias](../reference/r_JDBCTypeDataSource.md#).

</td></tr><tr><td>

Use MID Server

</td><td>

MID Server to use to connect to this data source.

</td></tr><tr><td>

Format

</td><td>

Select one of the following formats: MySQL, Oracle, or SQLServer.

</td></tr><tr><td>

Instance name

</td><td>

Used to support dynamic port connectivity with SQL Server. To ensure connectivity, provide the instance name for a SQL Server that receives a new port number dynamically after each reboot. This field only appears when **SQLServer** is selected as a data source format.

</td></tr><tr><td>

Database name

</td><td>

Name of the database instance.

</td></tr><tr><td>

Database port

</td><td>

Port number for the database. Leave this field empty when using dynamic port connectivity with SQL Server.

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

Use integrated authentication

</td><td>

Selected to allow the JDBC connection to use the ID of the user configured for the Windows MID Server service for SQL Server authentication. For additional details, see [JDBC type data source](../reference/r_JDBCTypeDataSource.md#).

</td></tr><tr><td>

Username

</td><td>

User name for authentication on the JDBC server.

</td></tr><tr><td>

Password

</td><td>

Password for authentication on the JDBC server.

</td></tr><tr><td>

Server

</td><td>

Name of the server from which the tables will be imported.

</td></tr><tr><td>

Query

</td><td>

Type of query to run: **All rows from Table** or **Specific SQL**. If you select to run a SQL statement, the SQL statement field appears.

</td></tr><tr><td>

Query timeout

</td><td>

Number of seconds the JDBC driver will wait for a query \(SELECT\) to complete. Zero \(0\) means no timeout. If timeout is exceeded, the integration considers the JDBC result inaccessible and places it in an error state.

</td></tr><tr><td>

Connection timeout

</td><td>

Number of seconds before MID Server connection cache pool closes and removes it from the pool. Zero \(0\) means no timeout.

</td></tr><tr><td>

Table name

</td><td>

Name of the table from which the data is being exported.

</td></tr><tr><td>

SQL statement

</td><td>

SQL statement to extract the desired data from the database.

</td></tr><tr><td>

Use last run datetime

</td><td>

Controls the amount of data that is retrieved from a database during an import run. If unselected, then all rows in the table specified are imported, every time. You might want to use this setting if this is a one-time import, or if all the data in the target table is new. If selected, two additional fields appear, enabling you to select a datetime value to limit imported data to delta values only.

</td></tr><tr><td>

Last run datetime

</td><td>

The datetime value in this field is automatically populated from the database field you select below and represents the latest value from the previous run. This value acts as a dynamic filter to restrict the number of records retrieved to those records that have changed since the data source's last runtime.

</td></tr><tr><td>

Last run database field

</td><td>

Field name from the source table that will be used as the filter in the next run. This value may need to be case sensitive, depending on the target database type.

</td></tr><tr><td>

Additional Database Parameters

</td><td>

Optional parameters to add to the end of the URL generated for this data source. Semicolon-separated list of parameters. You may need to configure the form to view this field.

</td></tr></tbody>
</table>4.  Click **Submit**.


## What to do next

Define a transform map for the new data source and run an import.

**Parent Topic:**[Create a data source](../concept/c_CreateNewDataSource.md)

