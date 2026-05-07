---
title: Amazon Redshift metadata collector
description: Amazon Redshift metadata collector provides read-only access to metadata from an Amazon Redshift database.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring metadata collectors, Data Catalog, Workflow Data Fabric]
---

# Amazon Redshift metadata collector

Amazon Redshift metadata collector provides read-only access to metadata from an Amazon Redshift database.

The Amazon Redshift collector harvests metadata for Redshift tables and columns.

## Metadata cataloged

The Amazon Redshift collector catalogs the following information.

**Note:** All versions of overloaded functions and stored procedures are cataloged. Each version has its own title in the catalog but a distinct identifier.

|Object|Information cataloged|
|------|---------------------|
|Columns|Name, Description, JDBC type, Column Type, Is Nullable, Default Value, Key type \(Primary, foreign\), column size, column index|
|Table|Name, description, primary key, schema|
|Views|Name, description, SQL definition|
|Schema|Identifier, Name|
|Database|Type, name, identifier, server, port, environment, JDBC URL|
|Function|Name, Description, Function Type|
|Stored Procedure|Name, Description, Stored Procedure Type|

## Relationships between objects

Catalog pages show relationships between the following data asset types:

|Data asset page|Relationship|
|---------------|------------|
|Table|Columns|
|Columns|Table|
|Schema|Database that contains Schema, Table that is part of Schema|
|Database|Schema contained in Database|

## Lineage for Redshift

The following lineage information is collected by the Redshift collector:

<table id="table_asy_kyn_33c"><thead><tr><th>

Object

</th><th>

Lineage available

</th></tr></thead><tbody><tr><td>

View \(column-level\)

</td><td>

The collector traces data flow from view columns to source table columns across SQL expressions and sub queries. View → Table column relationships The collector captures lineage when views: -   Sort rows \(ORDER BY\)
-   Filter rows \(WHERE, HAVING\)
-   Aggregate rows \(GROUP BY\)

</td></tr><tr><td>

Stored Procedure

</td><td>

The collector identifies: -   The associated column in an upstream view or table:
    -   Where the data is sourced from
    -   That sort the rows via ORDER BY
    -   That filter the rows via WHERE/HAVING
    -   That aggregates the rows via GROUP BY
-   The downstream table that has its tables updated.

 The following stored procedures aren’t supported: -   Stored procedures with multitable inserts. However, multiple separate insert statements that insert into one table are supported.
-   Stored procedure with multiple SELECT and INSERT statements not separated by a semicolon delimiter

</td></tr></tbody>
</table>## Authentication supported

The collector supports username and password authentication to Redshift.

-   **[Prepare to run the Amazon Redshift collector](../task/prepare-to-run-amazon-redshift-collector.md)**  
Create a Redshift user and configure permissions before running the collector.
-   **[Create an Amazon Redshift metadata collector](../task/create-amazon-redshift-metadata-collector.md)**  
Create a collector to import metadata from Amazon Redshift.

**Parent Topic:**[Configuring metadata collectors](configure-metadata-collectors-dc.md)

