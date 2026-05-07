---
title: Fivetran metadata collector
description: Provides read-only access to metadata from a Fivetran account.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configuring metadata collectors, Data Catalog, Workflow Data Fabric]
---

# Fivetran metadata collector

Provides read-only access to metadata from a Fivetran account.

The collector harvests metadata from Fivetran assets, including connectors, jobs, groups, sources, and destinations. Supports impact analysis to understand how changes to upstream Fivetran connectors affect downstream systems.

## Metadata cataloged

The Fivetran collector catalogs the following information.

|Object|Information cataloged|
|------|---------------------|
|Groups|Name, Identifier, Creation date|
|Connectors|Identifier, Succeeded at datetime, Failed at datetime, Created at datetime, Sync frequency, Name, Version, Daily sync time, Schedule type, Setup state, Update state, Pause state, Sync state, Connector type, Connected by user identifier|
|Connector Jobs|Run state \(Failed time, Success time\)|
|Destination|Name, Setup status, Destination type, Identifier, Region|
|Data source|Data source configuration properties, as configuration key and value pairs.|
|Database tabular source|Database name, Server, Port, JDBC URL|
|Non-database tabular source|Datasource ID, Name|
|Database schema|Name|
|Destination database|Database name, Server, Port, JDBC URL|
|Columns|Name|

## Relationships between objects

Catalog pages show relationships between the following data asset types:

|Data asset page|Relationship|
|---------------|------------|
|Group|Destinations within group, Connectors within group|
|Connector|Source associated to connector, group that contains this connector, connector job which was initiated by this connector.|
|Connector Job|Connector|
|Fivetran Data Source|Tables that this Fivetran Data Source connects to via Source \(file or database\), Connector that connects to this Fivetran Data Source|
|Data Source|Tables within data source. For non-database sources, tabular sources connected via data source|
|Destination|Tables within destination, group that contains this destination|
|Table|Column within the table|
|Column|Table containing the column|

## Lineage for Fivetran

The collector identifies source columns from which destination columns derive their data through copy or load operations. Catalogs all database sources and destinations.

Supported data sources and connectors for cross-system lineage:

-   PostgreSQL
-   Salesforce
-   SQL Server

Supported database destinations for cross-system lineage:

-   Snowflake
-   SQL Server

|Object|Lineage available|
|------|-----------------|
|Source database columns and tables|Downstream destinations that source data from these columns and tables|

## Authentication supported

The collector authenticates using a Fivetran API key. The API key owner must have read access to destinations and connectors.

See the [Fivetran role-based access control documentation](https://fivetran.com/docs/getting-started/fivetran-dashboard/account-management/role-based-access-control#rolesinourrbacmodel) for details on API keys and permissions.

-   **[Prepare to run the Fivetran collector](../task/prepare-to-run-fivetran-collector.md)**  
Create a Fivetran API key before running the collector.
-   **[Create a Fivetran metadata collector](../task/create-fivetran-metadata-collector.md)**  
Create a collector to import metadata from Fivetran.

**Parent Topic:**[Configuring metadata collectors](configure-metadata-collectors-dc.md)

