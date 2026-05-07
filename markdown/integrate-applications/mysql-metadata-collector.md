---
title: MySQL metadata collector
description: The MySQL metadata collector provides read-only access to metadata from an external MySQL database.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring metadata collectors, Data Catalog, Workflow Data Fabric]
---

# MySQL metadata collector

The MySQL metadata collector provides read-only access to metadata from an external MySQL database.

This collector is designed to directly harvest metadata from your MySQL server. It is suitable for both self-hosted MySQL instances and managed MySQL instances, such as those hosted on AWS RDS. This collector also works with MariaDB instances.

## Metadata cataloged

The collector catalogs the following information.

|Object|Information cataloged|
|------|---------------------|
|Columns|Name, Description, JDBC type, Column Type, Is Nullable, Default Value, Key type \(Primary, foreign\), column size, column index|
|Table|Name, description, primary key, schema|
|Table Index|Index Cardinality, Column name, Index Type, Index Name, is non Unique, Ordinal Position, Pages, Sort Sequence|
|Views|Name, description, SQL definition|
|Schema|Identifier, Name|
|Database|Type, name, identifier, server, port, environment, JDBC URL|
|Function|Name, Description, Function Type|
|Stored Procedure|Name, Description, Stored Procedure Type|

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
</table>## Relationships between objects

The harvested metadata includes catalog pages for the following data asset types. Each catalog page has a relationship to the other related data asset types.

|Data asset page|Relationship|
|---------------|------------|
|Table|Columns, Table Indexes|
|Columns|Table|
|Schema|Database that contains Schema, Table that is part of Schema|
|Database|Schema contained in Database|

## Authentication supported

The MySQL collector supports username/password authentication to MySQL.

-   **[Prepare to run the MySQL collector](../task/prepare-to-run-mysql-collector.md)**  
Create a MySQL user and grant permissions before running the collector.
-   **[Create a MySQL metadata collector](../task/create-mysql-metadata-collector.md)**  
Create a collector to import metadata from MySQL.

**Parent Topic:**[Configuring metadata collectors](configure-metadata-collectors-dc.md)

