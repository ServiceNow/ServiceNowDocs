---
title: Snowflake metadata collector
description: The Snowflake metadata collector provides read-only access to metadata from an external Snowflake account.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Configuring metadata collectors, Data Catalog, Workflow Data Fabric]
---

# Snowflake metadata collector

The Snowflake metadata collector provides read-only access to metadata from an external Snowflake account.

The collector harvests metadata from Snowflake Data Cloud. It collects tabular objects, Horizon objects such as policies and tags, and Snowflake data quality artifacts. It also harvests functions and stored procedures. The collector can gather column statistics and table query counts. In addition, it can harvest metadata for Streamlit applications.

## Metadata cataloged

The Snowflake collector catalogs the following information.

**Note:** The collector harvests all versions of overloaded functions and stored procedures. Each version has its own title/name in the catalog, but a distinct identifier.

<table id="table_wtx_nqh_phc"><thead><tr><th>

Object

</th><th>

Information cataloged

</th></tr></thead><tbody><tr><td>

Column

</td><td>

Name, Comments, Data Type, Is Nullable, Default Value, Key type \(Primary, foreign\)

</td></tr><tr><td>

Table

</td><td>

Name, Comments, Primary key, Schema, External URL \(Snowsight\)Extended metadata: Is Iceberg, Is dynamic, Is transient, Created Date, Last Modified Date, Last Updated By \(Snowflake LAST\_DDL\_BY\), Owner \(Snowflake role that owns table\), Definition Altered Date, Table Size

</td></tr><tr><td>

View

</td><td>

Name, Comments, Schema, External URL \(Snowsight\), Definition Altered Date, Last Modified By \(Snowflake LAST\_DDL\_BY\), Is Iceberg, Is dynamic, Is temporary, Created Date, Last Modified Date, Owner \(Snowflake role that owns table\), SQL definition

</td></tr><tr><td>

Materialized View

</td><td>

Name, Comments, Schema, External URL \(Snowsight\), Definition Altered Date, Last Modified By \(Snowflake LAST\_DDL\_BY\), Is Iceberg, Is dynamic, Is temporary, Created Date, Last Modified Date, Owner \(Snowflake role that owns table\)

</td></tr><tr><td>

Schema

</td><td>

Identifier, NameExtended metadata: Comments, Created date, Updated

</td></tr><tr><td>

Database

</td><td>

Type, Name, Identifier, Server, Port, Environment, JDBC URLExtended metadata: Comments

</td></tr><tr><td>

User-defined function\(this includes User-defined functions created in Snowpark\)

</td><td>

NameExtended metadata: Function Definition, Comments, Created Date, Owner \(Snowflake Role\), Snowflake Function Type \(Return Type\), Function Signature, Function Language, Packages, Runtime version, Updated

</td></tr><tr><td>

Stored Procedure\(this includes Stored Procedures created in Snowpark\)

</td><td>

NameExtended metadata: Function Definition, Owner \(Snowflake Role\), Comments, Return Type, Function Language, Packages, Created Date, Function signature, Snowflake Function Type, Runtime Version, Updated, Stored Procedure Type

</td></tr></tbody>
</table>## Relationships between objects

The harvested metadata includes catalog pages for the following data asset types. Each catalog page has a relationship to the other related data asset types.

|Data asset page|Relationships|
|---------------|-------------|
|Snowflake Row access policies|Tables|
|Snowflake Masking Policies|Columns, Tag value|
|Table|Columns, Tag value, Data Metric Function that analyzes, Views, Tables, or Functions which the Table depends on|
|Snowflake Tags|Tag value|
|Columns|Table, Tag Value, System Tag Value|
|View|Schema that contains Views, Columns that are part of Views, Data Metric Function that analyzes View, Views, Tables, or Functions which the View depends on|
|Materialized View|Schema that contains Materialized Views, Columns that are part of Materialized Views|
|Schema|Database that contains Schema, Table that is part of Schema, View that is part of Schema, Materialized View that is part of Schema, Streamlit app that is part of schema|
|Streamlit App|Schema that contains Streamlit App|
|Database|Schema contained in Database|
|Data Metric Function|Table or View analyzed by this Snowflake Data Metric Function, Table, Views, Tables, or Functions which the Function depends on|

## Lineage and dependencies for Snowflake

The following lineage information is collected by the Snowflake collector. Note that any lineage for SQL Statements defined via variable statements are not supported.

Important things to note:

-   Any lineage for SQL Statements defined via variable statements are not supported.
-   The collector traces these relationships from a View’s columns to ultimate source Table columns across SQL expressions and subqueries.

<table id="table_dvy_vzm_phc"><thead><tr><th>

Object

</th><th>

Lineage available

</th></tr></thead><tbody><tr><td>

Column in View

</td><td>

The collector identifies the associated column in an upstream view or table:

 -   Where the data is sourced from
-   That sort the rows via ORDER BY
-   That filter the rows via WHERE/HAVING
-   That aggregate the rows via GROUP BY

</td></tr><tr><td>

User-defined function

</td><td>

A Function and:

 -   Views referenced in Function
-   Tables referenced in Function
-   Functions referenced in Function

 A View and Function referencing View

</td></tr><tr><td>

Stored Procedure

</td><td>

The collector identifies:

 -   The associated column in an upstream view or table
    -   Where the data is sourced from
    -   That sort the rows via ORDER BY
    -   That filter the rows via WHERE/HAVING
    -   That aggregate the rows via GROUP BY
-   The downstream table that has its data updated by this stored procedure.

 Note: The following stored procedures are not supported:

 -   Stored procedures with multitable inserts. However, multiple separate insert statements that insert into one table *are supported*.
-   Stored procedure with multiple SELECT and INSERT statements not separated by a semicolon delimiter.
-   Stored procedures used to create tables or any transient tables created during the execution scope of a stored procedure.

</td></tr></tbody>
</table>Dependencies

The Snowflake collector catalogs dependencies between tables, views, and functions using the Snowflake Account Usage view OBJECT\_DEPENDENCIES. See the Snowflake documentation for more information about the OBJECT\_DEPENDENCIES view.

If you include the profiling and sampling specific parameters while running the collector, the following additional information is harvested for Columns.

**Note:** The user/role must have read access to data to be able to harvest profiling information \(column statistics\).

<table id="table_bvx_ddp_13c"><thead><tr><th>

Object

</th><th>

Information cataloged

</th></tr></thead><tbody><tr><td>

Column

</td><td>

-   Average Length \(sample\)
-   Average Value \(sample\)
-   Data Distribution
-   Distinct Values
-   Estimated Distinct Values
-   Estimated Non-null Values
-   Maximum Length \(sample\)
-   Maximum Value \(sample\) sorted numerically or alphabetically \(z-a\)
-   Minimum Length \(sample\)
-   Minimum Value \(sample\) sorted numerically or alphabetically \(a-z\)
-   Non-null Values \(sample\)
-   Sample String Values \(first 5 items in a column\)

</td></tr><tr><td>

Table

</td><td>

-   Row Count
-   Sample Count \(Target sample size\)

</td></tr></tbody>
</table>Following additional information is cataloged when you run the collector with the Collect Snowflake policy information and Collect Snowflake tag information options enabled.

|Object|Information cataloged|
|------|---------------------|
|Columns|Snowflake masking policies|
|Snowflake Tags|Name, Allowed Values, Comments|
|Snowflake Tag Values|Name, Value|
|Snowflake Masking Policies|Name, Comments , Date created, Snowflake tags, Owner, Type, Policy body, Schema, Database|
|Snowflake Row access policies|Name, Comments , Date created, Snowflake tags, Owner, Type, Policy body, Schema, Database|

Following additional information is cataloged when you run the collector with the Collect Snowflake table usage information and Table usage lookback days options enabled.

|Object|Information cataloged|
|------|---------------------|
|Table|Query Count|

Following additional information about [data quality metrics](https://docs.snowflake.com/en/user-guide/data-quality-system-dmfs) is cataloged when you run the collector with the Collect data metric function information option enabled.

<table id="table_yqd_rxb_n3c"><thead><tr><th>

Object

</th><th>

Information cataloged

</th></tr></thead><tbody><tr><td>

Data Metric Function

</td><td>

-   Identifier: Name of the function
-   Title: Name of the function
-   Description
-   Body Definition of the function

</td></tr><tr><td>

Table

</td><td>

-   Schedule: cron expressions
-   Data metric function observations: function name, column arguments, most recent metric time, value

</td></tr></tbody>
</table>Following additional information is cataloged when you run the collector with theCollect Streamlit app information option enabled.

<table id="table_u5h_vxb_n3c"><thead><tr><th>

Object

</th><th>

Information cataloged

</th></tr></thead><tbody><tr><td>

Snowflake Streamlit App

</td><td>

-   Identifier: App Name
-   Title: App Title
-   Description: App comments
-   Main file
-   Root location
-   Date Created
-   Owner

</td></tr></tbody>
</table>-   **[Prepare to run the Snowflake collector](../task/prepare-to-run-the-snowflake-collector.md)**  
Set up authentication and grant role permissions to enable Snowflake metadata collection.
-   **[Create a Snowflake metadata collector](../task/create-snowflake-metadata-collector.md)**  
Create a collector to import metadata from Snowflake.

**Parent Topic:**[Configuring metadata collectors](configure-metadata-collectors-dc.md)

