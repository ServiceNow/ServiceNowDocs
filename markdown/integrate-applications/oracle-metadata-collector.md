---
title: Oracle metadata collector
description: The Oracle metadata collector provides read-only access to metadata from an external Oracle account.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Configuring metadata collectors, Data Catalog, Workflow Data Fabric]
---

# Oracle metadata collector

The Oracle metadata collector provides read-only access to metadata from an external Oracle account.

The collector harvests metadata for Oracle objects, such as tables and columns, from an Oracle database, making them searchable and discoverable in the data catalog. It is suitable for both self-hosted Oracle instances and managed Oracle instances, like those hosted on AWS RDS.

## Metadata cataloged

The Oracle collector catalogs the following information.

**Note:** The collector harvests all versions of overloaded functions and stored procedures. Each version has its own title/name in the catalog, but a distinct identifier.

|Object|Information cataloged|
|------|---------------------|
|Columns|Name, JDBC type, Column Type, Is Nullable, Default Value, Key type \(Primary, Foreign\), Column size, Column index Extended metadata: Comment|
|Table|Name, Primary key, Schema Extended metadata: Comment|
|Table Index|Index Cardinality, Column name, Index Type, Index Name, is non Unique, Ordinal Position, Pages, Sort Sequence|
|Views|Name, Definitions, SQL Definition Extended metadata: Description|
|Schema|Identifier, Name|
|Database|Type, Name, Identifier, Server, Port, Environment, JDBC URL|
|Function|Name, Description, Function Type Extended metadata: Function definition, Package Name|
|Stored Procedure|Name, Description, Stored Procedure Type Extended metadata: Procedure Definition, Package Name|
|Synonym|Identifier Extended metadata: Name|
|Package|Name, Specification Extended metadata: Body definition, Package Body|
|Public Synonym \(accessible to all users in database\)|Identifier, Name|

If you include the profiling and sampling specific parameters while running the collector, the following additional information is harvested for Columns.

**Note:** The user/role must have read access to data to be able to harvest profiling information \(column statistics\).

<table id="table_vyl_pjk_13c"><thead><tr><th>

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
</table>## Relationships between objects

The harvested metadata includes catalog pages for the following data asset types. Each catalog page has a relationship to the other related data asset types.

|Data asset page|Relationship|
|---------------|------------|
|Table|Columns, Table Indexes|
|Columns|Table|
|Schema|Database that contains Schema, Table that is part of Schema|
|Database|Schema contained in Database|
|Synonym|The schema which contains the synonym, The table, view, function, procedure, or package the synonym is for|
|Package|Schema that contains package Extended metadata: Stored Procedures contained in package, Functions contained in package|
|Database|Public synonym contained in database|

## Lineage for Oracle

The following lineage information is collected by the Oracle collector. To harvest lineage from referenced objects located in another server, you must set up the Linked host parameter while running the collector.

**Note:**

Any lineage for SQL Statements defined via variable statements are not supported.

<table id="table_qvv_pgk_13c"><thead><tr><th>

Object

</th><th>

Lineage available

</th></tr></thead><tbody><tr><td>

Column in View

</td><td>

The collector identifies: -   The associated column in an upstream view or table
    -   Where the data is sourced from
    -   That sort the rows via ORDER BY
    -   That filter the rows via WHERE/HAVING
    -   That aggregate the rows via GROUP BY
-   The downstream table that has its data updated by this function.

</td></tr><tr><td>

User-defined function

</td><td>

A Function and: -   Views referenced in Function
-   Tables referenced in Function
-   Functions referenced in Function
-   Stored procedures referenced in function

 A View and: -   Function referencing View

 The collector identifies: -   The associated column in an upstream view or table
    -   Where the data is sourced from
    -   That sort the rows via ORDER BYThat filter the rows via WHERE/HAVING
    -   That aggregate the rows via GROUP BY
-   The downstream table that has its data updated by this Stored Procedure.

</td></tr><tr><td>

Stored Procedure

</td><td>

A Stored Procedure and: -   Views referenced in Stored Procedure
-   Tables referenced in Stored Procedure
-   Functions referenced in Stored Procedure
-   Stored procedures referenced in Stored Procedure

 A View and: -   Stored Procedure referencing View

 The collector identifies: -   The associated column in an upstream view or table
    -   Where the data is sourced from
    -   That sort the rows via ORDER BY
    -   That filter the rows via WHERE/HAVING
    -   That aggregate the rows via GROUP BY
-   The downstream table that has its data updated by this Stored Procedure.

The following stored procedures are not supported: -   Stored procedures with multitable inserts. However, multiple separate insert statements that insert into one table are supported.
-   Stored procedure with multiple SELECT and INSERT statements not separated by a semicolon delimiter.
-   Stored procedures used to create tables or any transient tables created during the execution scope of a stored procedure.

</td></tr></tbody>
</table>## Oracle version supported

The collector supports Oracle database version 19.0.0.0.

## Authentication supported

The Oracle collector supports username/password authentication to Oracle.

-   **[Prepare to run the Oracle collector](../task/prepare-to-run-oracle-collector.md#)**  
Set up database user permissions and configure advanced features before running the collector.
-   **[Create an Oracle metadata collector](../task/create-oracle-metadata-collector.md)**  
Create a collector to import metadata from Oracle.

**Parent Topic:**[Configuring metadata collectors](configure-metadata-collectors-dc.md)

