---
title: Oracle
description: The Oracle connector provides read-only access to data and metadata from an Oracle database.
locale: en-US
release: yokohama
product: Workflow Data Fabric Hub
classification: workflow-data-fabric-hub
topic_type: concept
last_updated: "2025-04-30"
reading_time_minutes: 1
breadcrumb: [Primary connectors, Managing zero copy connections in Workflow Data Fabric Hub, Workflow Data Fabric Hub, Data and Automation]
---

# Oracle

The Oracle connector provides read-only access to data and metadata from an Oracle database.

A connection admin can set up a connection to Oracle in the Workflow Data Fabric Hub and grant data stewards access to this connection. Data stewards can then use the established connection to create a data fabric table and map data from Oracle. This allows users to access Oracle data through the table list view or by using GlideRecord scripts. For details on creating data fabric tables and mapping data, see [Managing data fabric tables in Workflow Data Fabric Hub](managing-data-fabric-tables-wdf.md).

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

The following table lists supported Oracle data types and the default matching data types in a data fabric table.

**Important:** Oracle data types not included in the table aren't supported for data mapping in Workflow Data Fabric Hub.

|Oracle|Data fabric table|
|------|-----------------|
|number|Decimal|
|binary\_float|Floating Point Number|
|binary\_double|Floating Point Number|
|char|String|
|varchar2|String|
|nchar|String|
|nvarchar2|String|
|date|Basic Date/Time|
|timestamp|Basic Date/Time|
|timestamptz|Date/Time|
|bool\_sim|String|
|FLOAT\[\(p\)\]|Floating Point Number|
|TIMESTAMP\(p\) WITH TIME ZONE|Date/Time|

**Related topics**  


[Create an Oracle connection](../task/create-oracle-connection.md)

