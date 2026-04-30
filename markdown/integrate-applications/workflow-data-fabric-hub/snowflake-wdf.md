---
title: Snowflake
description: The Snowflake connector provides read-only access to data and metadata from an external Snowflake account.
locale: en-US
release: yokohama
product: Workflow Data Fabric Hub
classification: workflow-data-fabric-hub
topic_type: concept
last_updated: "2025-04-30"
reading_time_minutes: 1
breadcrumb: [Primary connectors, Managing zero copy connections in Workflow Data Fabric Hub, Workflow Data Fabric Hub, Data and Automation]
---

# Snowflake

The Snowflake connector provides read-only access to data and metadata from an external Snowflake account.

A connection admin can set up a connection to Snowflake in the Workflow Data Fabric Hub and grant data stewards access to this connection. Data stewards can then use the established connection to create a data fabric table and map data from Snowflake. This allows users to access Snowflake data through the table list view or by using GlideRecord scripts. For details on creating data fabric tables and mapping data, see [Managing data fabric tables in Workflow Data Fabric Hub](managing-data-fabric-tables-wdf.md).

The connector has been enhanced to improve the performance of the following Glide queries and list view operations. These improvements allow the majority of queries to be executed at the data source.

-   Sort
-   Limit
-   Filter
-   GroupBy
-   avg\(\)
-   count\(\)
-   max\(\)
-   min\(\)
-   sum\(\)
-   References

## Supported data types

The following table lists supported Snowflake data types and the default matching data types in a data fabric table.

**Important:** Snowflake data types not included in the table aren't supported for data mapping in Workflow Data Fabric Hub.

|Snowflake|Data fabric table|
|---------|-----------------|
|int|Decimal|
|byteint|Decimal|
|char|String|
|character|String|
|varchar|String|
|varchar\_default|String|
|string|String|
|text|String|
|date|Date|
|timestamp|Basic Date/Time|
|timestamp\_tz|Date/Time|
|boolean|True/False|
|datetime|Date/Time|
|numeric|Decimal|
|integer|Decimal|
|bigint|Decimal|
|smallint|Decimal|
|tinyint|Decimal|

**Related topics**  


[Create a Snowflake connection](../task/create-snowflake-connection.md)

