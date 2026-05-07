---
title: BigQuery metadata collector
description: The BigQuery metadata collector provides read-only access to metadata from an external BigQuery account.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring metadata collectors, Data Catalog, Workflow Data Fabric]
---

# BigQuery metadata collector

The BigQuery metadata collector provides read-only access to metadata from an external BigQuery account.

The collector harvests metadata for BigQuery datasets, projects, tables, and columns in a BigQuery instance and make it searchable and discoverable in the data catalog. The collector also harvests column-level lineage relationships between tables and views.

## Metadata cataloged

The BigQuery collector catalogs the following information.

|Object|Information cataloged|
|------|---------------------|
|Datasets|ID, name, description, labels \(note these are key/value pairs\), created date, last modified date, default table expiry, default partition expiry, data location|
|Projects|Name|
|Tables|Name, Description, Created date, Last modified date, Default table expiration, Data location, Labels, Type \(Standard, External, Snapshot, Model\), Partitioned on field, Clustered by columns for standard and snapshot tables, Partition type \(range or time\) requires partition filter - Range \(Start, end, interval\) Time \(Partition type \(hour, day, month, year\), expiration\)|
|Columns|Name, Description, Data Type, Is Nullable, Column size|
|View|Name, description, created date, default table expiration, last modified date, data location, default collation, labels, view SQL, clustered by columns for materialized|

## Relationships between objects

Catalog pages show relationships between the following data asset types:

|Data asset page|Relationships|
|---------------|-------------|
|Datasets|Tables, Views|
|Projects|Dataset|
|Tables|Column, Labels|
|Columns|Table, View|
|Views|Column|
|Label Value|Table, View, Project, Dataset|

## Lineage for BigQuery

The following lineage information is collected by the BigQuery collector.

<table id="table_ncz_psc_xhc"><thead><tr><th>

Object

</th><th>

Lineage available

</th></tr></thead><tbody><tr><td>

View Column

</td><td>

The collector identifies the associated column in an upstream view or table:

 -   Where the data is sourced from
-   That sort the rows via ORDER BY
-   That filter the rows via WHERE/HAVING
-   That aggregate the rows via GROUP BY

</td></tr></tbody>
</table>-   **[Prepare to run the BigQuery collector](../task/prepare-to-run-bigquery-collector.md)**  
Create a service account and configure authentication before running the collector.
-   **[Create a BigQuery metadata collector](../task/create-bigquery-metadata-collector.md)**  
Create a collector to import metadata from BigQuery.

**Parent Topic:**[Configuring metadata collectors](configure-metadata-collectors-dc.md)

