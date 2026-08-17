---
title: Teradata metadata collector
description: The Teradata metadata collector harvests read-only metadata from a Teradata account.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/teradata-metadata-collector.html
release: australia
topic_type: concept
last_updated: "2026-06-18"
reading_time_minutes: 3
keywords: [Teradata]
breadcrumb: [Configuring metadata collectors, Data Catalog, Workflow Data Fabric]
---

# Teradata metadata collector

The Teradata metadata collector harvests read-only metadata from a Teradata account.

The collector harvests metadata from Teradata, including user defined functions, stored procedures, triggers, user defined types, and user defined methods.

## Authentication supported

The collector authenticates to Teradata using [username and password](https://docs.teradata.com/r/ODBC-Driver-for-Teradata-User-Guide/June-2022/Network-Security/Authentication-Mechanisms). Before running the collector, set up a dedicated database user with the required permissions. See [Prepare to run the Teradata Collector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/prepare-to-run-teradata-collector.md).

## Metadata cataloged

<table id="table_dw4_fmc_qjc"><thead><tr><th>

Object

</th><th>

Information cataloged

</th></tr></thead><tbody><tr><td>

Database

</td><td>

Type, Name, JDBC URL Extended metadata: Created By, Created At, Updated By, Updated At, Owner name, Space allocation \(permanent, spool, temporary\), Description

</td></tr><tr><td>

Table

</td><td>

Name, Description, Primary Key, Foreign Key, Sample rows \(if data sampling is enabled\) Extended metadata: Created By, Created At, Updated By, Updated At, Size

</td></tr><tr><td>

Table index

</td><td>

Index Cardinality, Column name, Index Type, Index Name, Is Non Unique, Column Ordinal Position, Pages, Column Sort Sequence

</td></tr><tr><td>

Schema

</td><td>

Name

</td></tr><tr><td>

Column

</td><td>

Name, Description, Data Type, Is Nullable

</td></tr><tr><td>

View

</td><td>

Name, Description, SQL definition, Created By, Created At, Updated By, Updated At

</td></tr><tr><td>

User defined functions

</td><td>

Name, Function type Extended metadata: Definition, Deterministic characteristic, Null-call characteristic, Description, Number of parameters, Source file language, Data access, Parameter style, Execution protection mode, Platform type, Character type, Created, Created By, Last Modified, Last Modified By, External File Reference

</td></tr><tr><td>

SQL stored procedures

</td><td>

Name, Description, Stored procedure type, Definition Extended metadata: Created, Created By, Last Modified, Last Modified By

</td></tr><tr><td>

External stored procedures

</td><td>

Name, Stored procedure type Extended metadata: Definition, Application category, Description, Number of parameters, External file reference, Execution protection mode, Character type, Platform type, Source file language, Parameter style, Data access

</td></tr><tr><td>

Triggers

</td><td>

Name, Fired at instant Extended metadata: Created By, Created At, Updated By, Updated At, Name, Evaluation type, Fired on event, Trigger enabled, Order number, Definition, Trigger Comment, Subject Table Name, Action Time, Trigger Definition

</td></tr><tr><td>

User defined types

</td><td>

Extended metadata: Name, Type, Default transform group, Ordering form, Ordering Category, Default null specified for array, All operators supported, Encryption supported, Compression supported, Instantiable, Final

</td></tr><tr><td>

User defined methods

</td><td>

Name, Description, Number of parameters, Source file language, Data access, Parameter style, Deterministic characteristic, Null-call characteristic, Execution protection mode, Character type, Platform type

</td></tr></tbody>
</table>Profiling and sampling specific information.

If you include the profiling and sampling specific parameters while running the collector, the following additional information is harvested for columns.

**Note:** Users or roles must have read access to data to harvest profiling information \(column statistics\).

<table id="table_ew4_fmc_qjc"><thead><tr><th>

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
-   Maximum Value \(sample\) sorted numerically or alphabetically \(z–a\)
-   Minimum Length \(sample\)
-   Minimum Value \(sample\) sorted numerically or alphabetically \(a–z\)
-   Non-null Values \(sample\)
-   Sample String Values \(first 5 items in a column\)

</td></tr><tr><td>

Table

</td><td>

-   Row Count
-   Sample Count \(target sample size\)

</td></tr></tbody>
</table>## Relationships between objects

By default, the harvested metadata includes catalog pages for the following resource types. Each catalog page has a relationship to the other related resource types. If the metadata presentation for this data source has been customized, you might see other resource pages and relationships.

<table id="table_hw4_fmc_qjc"><thead><tr><th>

Resource page

</th><th>

Relationship

</th></tr></thead><tbody><tr><td>

Table

</td><td>

-   Columns contained in tables
-   Table indexes

</td></tr><tr><td>

Columns

</td><td>

-   Table
-   Table indexes

</td></tr><tr><td>

Table indexes

</td><td>

Columns

</td></tr><tr><td>

Trigger

</td><td>

Table triggers on tables

</td></tr><tr><td>

Schema

</td><td>

-   Database that contains schema
-   Table that is part of schema

</td></tr><tr><td>

Database

</td><td>

Schema contained in database

</td></tr></tbody>
</table>## Lineage for Teradata

The Teradata collector collects the following lineage information.

**Note:** Lineage for SQL statements defined via variable statements is not supported.

<table id="table_lw4_fmc_qjc"><thead><tr><th>

Object

</th><th>

Lineage available

</th></tr></thead><tbody><tr><td>

View

</td><td>

The collector identifies the associated column in an upstream view or table: -   Where the data is sourced from
-   That sort the rows via ORDER BY
-   That filter the rows via WHERE/HAVING
-   That aggregate the rows via GROUP BY

</td></tr><tr><td>

Stored procedure

</td><td>

The collector identifies: -   The associated column in an upstream view or table
-   Where the data is sourced from
-   That sort the rows via ORDER BY
-   That filter the rows via WHERE/HAVING
-   That aggregate the rows via GROUP BY
-   The downstream table that has its data updated

 Lineage is not available in the following cases:

 -   The SQL statement in stored procedures contains the SELECT INTO clause
-   Stored procedures with multiple insert statements
-   Stored procedures used to create tables or transient tables created during the execution scope of a stored procedure

</td></tr></tbody>
</table>-   **[Prepare to run the Teradata Collector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/prepare-to-run-teradata-collector.md)**  
Create a dedicated Teradata user with the permissions required for the metadata collector to harvest metadata from a target database.
-   **[Create a Teradata metadata collector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/create-teradata-metadata-collector.md)**  
Create a collector to import metadata from Teradata.

**Parent Topic:**[Configuring metadata collectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/configure-metadata-collectors-dc.md)

