---
title: Data interfaces
description: Data interfaces provide stable contracts for accessing data from single tables or combined sources through JOIN or UNION operations.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-25"
reading_time_minutes: 3
breadcrumb: [Explore, Data Products, Workflow Data Fabric]
---

# Data interfaces

Data interfaces provide stable contracts for accessing data from single tables or combined sources through JOIN or UNION operations.

A data interface defines the schema, field names, and data types that consumers use to query data. Interfaces act as stable access layers between consumers and underlying data sources. When source systems change, the data interface schema remains consistent and protects dashboards, workflows, and applications from breaking changes.

## How data interfaces work

Data interfaces map source data to a target schema that consumers query. The data interface defines which columns appear, their names, and their data types.

A data interface can expose data from a single ServiceNow table, a single Data Fabric Table connected to an external system, or multiple sources combined through JOIN or UNION operations.

Consumers query the data interface without requiring knowledge about which source systems provide the data. The data interface handles connections to sources, applies column mappings, and returns results in the defined schema. ![Sample data interface](../image/wdf-data-interface-overview.png)

## Combination methods

|Method|Description|When to use|
|------|-----------|-----------|
|Single table|Exposes one source table through a governed interface with consistent naming and documentation.|Provide controlled access to a ServiceNow tables or external tables when no combination is required.|
|JOIN|Combines related data from multiple tables based on matching column values. The current release supports INNER JOIN operations.|Merge customer data with order data, match purchase orders with approval records, or create comprehensive entity views across systems.|
|UNION|Stacks rows from multiple tables with similar structures into one unified result. The current release supports UNION operations.|Combine data from multiple regions, aggregate similar data across systems, or consolidate records from different sources.|

## Schema stability

Data interfaces provide schema permanency. After publication, the data interface maintains its structure even when underlying source tables change.

This stability protects consumers from breaking changes. A dashboard built on a data interface continues working when you upgrade or replace a source system. Workflows that query a data interface don't break when column names change in source tables.

When you extend a data interface by adding new columns, existing queries continue working. Consumers retrieve only the columns they originally queried, plus any new columns they choose to include.

## Data interfaces and data products

You can query data interfaces directly from workflows or dashboards. More commonly, data products package interfaces and provide additional metadata, documentation, and access controls.

Multiple data products can include a single interface. For example, a Customer Profile interface might be part of a Customer 360 data product and also included in a Sales Analytics data product.

## Data interfaces and external sources

Data interfaces can access external data through Data Fabric Tables. These tables provide zero-copy access to external databases such as Snowflake, Databricks, and Oracle. Data stays in the source system but can be queried through ServiceNow.

When you create a data interface using JOIN or UNION with Data Fabric Tables, the system generates intermediate tables for the operation. These intermediate tables are implementation details that remain hidden from the Data Catalog. Consumers interact only with the published interface.

## Querying data interfaces

Consumers access data interfaces through multiple channels:

-   Flow Designer for building automated workflows
-   Dashboard Builder for creating visualizations and reports
-   APIs for programmatic access from applications and scripts
-   AI Data Explorer for natural language queries

## What to explore next

To learn more about data interfaces, see:

-   [Managing data interfaces](manage-data-interfaces_wdf.md)
-   [Managing data products](manage-data-products-wdf.md)

