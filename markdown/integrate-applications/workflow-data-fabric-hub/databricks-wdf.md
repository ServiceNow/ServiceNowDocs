---
title: Databricks
description: The Databricks connector provides read-only access to data and metadata from the Databricks data analytics platform.
locale: en-US
release: yokohama
product: Workflow Data Fabric Hub
classification: workflow-data-fabric-hub
topic_type: concept
last_updated: "2025-04-30"
reading_time_minutes: 1
breadcrumb: [Primary connectors, Managing zero copy connections in Workflow Data Fabric Hub, Workflow Data Fabric Hub, Data and Automation]
---

# Databricks

The Databricks connector provides read-only access to data and metadata from the Databricks data analytics platform.

A connection admin can set up a connection to Databricks in the Workflow Data Fabric Hub and grant data stewards access to this connection. Data stewards can then use the established connection to create a data fabric table and map data from Databricks. This allows users to access Databricks data through the table list view or by using GlideRecord scripts. For details on creating data fabric tables and mapping data, see [Managing data fabric tables in Workflow Data Fabric Hub](managing-data-fabric-tables-wdf.md).

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

The following table lists supported Databricks data types and the default matching data types in a data fabric table.

**Important:** Databricks data types not included in the table aren't supported for data mapping in Workflow Data Fabric Hub.

|Databricks|Data fabric table|
|----------|-----------------|
|bigint|Long Integer String|
|int|Long Integer String|
|smallint|Long Integer String|
|tinyint|Long Integer String|
|timestamp\_ntz|Basic Date/Time|
|char|Char|
|timestamp|Basic Date/Time|
|date|Date|
|decimal|Decimal|
|string|String|
|boolean|True/False|
|double|Floating Point Number|
|float|Floating Point Number|

**Related topics**  


[Create a Databricks connection](../task/create-databricks-connection.md)

