---
title: PostgreSQL metadata collector
description: Provides read-only access to metadata from a PostgreSQL database.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configuring metadata collectors, Data Catalog, Workflow Data Fabric]
---

# PostgreSQL metadata collector

Provides read-only access to metadata from a PostgreSQL database.

The collector harvests metadata for PostgreSQL tables and columns, making them searchable and discoverable in the data catalog. Supports both self-hosted PostgreSQL instances and managed PostgreSQL instances, such as those hosted on AWS RDS.

## Authentication supported

Username and password authentication and AWS IAM authentication.

## Metadata cataloged

The PostgreSQL collector catalogs the following information.

**Note:** All versions of overloaded functions and stored procedures are cataloged. Each version has its own title in the catalog but a distinct identifier.

|Object|Information cataloged|
|------|---------------------|
|Columns|Name, Description, JDBC type, Column Type, Is Nullable, Default Value, Key type \(Primary, foreign\), column size, column index|
|Table|Name, description, primary key, schema|
|Table Index|Index Cardinality, Column name, Index Type, Index Name, is non Unique, Ordinal Position, Pages, Sort Sequence|
|Views|Name, description, SQL definition|
|Materialized View|Name, description, SQL definition|
|Schema|Identifier, Name|
|Database|Type, name, identifier, server, port, environment, JDBC URL|
|Function|Name, Description, Function Type|
|Stored Procedure|Name, Description, Stored Procedure Type|

When profiling and sampling parameters are enabled, the following additional column information is cataloged:

**Note:** The user/role must have read access to data to be able to harvest profiling information \(column statistics\).

<table id="table_cg5_n2k_13c"><thead><tr><th>

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

Catalog pages show relationships between the following data asset types:

<table id="table_okm_12k_13c"><thead><tr><th>

Data asset page

</th><th>

Relationship

</th></tr></thead><tbody><tr><td>

Table

</td><td>

Columns, Table Indexes

</td></tr><tr><td>

Columns

</td><td>

Table

</td></tr><tr><td>

Schema

</td><td>

-   Database that contains Schema
-   Table that is part of Schema
-   View that is part of Schema
-   Materialized View that is part of Schema

</td></tr><tr><td>

View

</td><td>

-   Schema that contains Views
-   Columns that are part of Views

</td></tr><tr><td>

Materialized View

</td><td>

-   Schema that contains Materialized Views
-   Columns that are part of Materialized Views

</td></tr></tbody>
</table>## Lineage for PostgreSQL

The collector identifies column-level lineage for Views and Materialized Views, tracing data sources from view columns to source table columns across SQL expressions and subqueries.

Establishes relationships between Views and source Table columns that:

-   Sort rows \(SQL ORDER BY\)
-   Filter rows \(SQL WHERE and HAVING clauses\)
-   Aggregate rows \(SQL GROUP BY\)

**Note:** View-to-table relationships can be established transitively through column-level relationships. Variable statement lineage isn’t supported.

-   **[Prepare to run the PostgreSQL collector](../task/prepare-to-run-postgresql-collector.md)**  
Create a PostgreSQL user and configure permissions before running the collector.
-   **[Create a PostgreSQL metadata collector](../task/create-postgresql-metadata-collector.md)**  
Create a collector to import metadata from PostgreSQL.

**Parent Topic:**[Configuring metadata collectors](configure-metadata-collectors-dc.md)

