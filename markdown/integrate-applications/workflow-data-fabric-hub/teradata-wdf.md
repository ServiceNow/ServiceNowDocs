---
title: Teradata
description: The Teradata connector provides read-only access to data and metadata from a Teradata source.
locale: en-US
release: zurich
product: Workflow Data Fabric Hub
classification: workflow-data-fabric-hub
topic_type: concept
last_updated: "2025-10-01"
reading_time_minutes: 1
breadcrumb: [Primary connectors, Manage zero copy connections, Workflow Data Fabric Hub, Workflow Data Fabric]
---

# Teradata

The Teradata connector provides read-only access to data and metadata from a Teradata source.

A connection admin can set up a connection to Teradata in the Workflow Data Fabric Hub and grant data stewards access to this connection. Data stewards can then use the established connection to create a data fabric table and map data from Teradata. This allows users to access Teradata data through the table list view or by using GlideRecord scripts. For details on creating data fabric tables and mapping data, see [Managing data fabric tables in Workflow Data Fabric Hub](managing-data-fabric-tables-wdf.md).

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

The following table lists supported Teradata data types and the default matching data types in a data fabric table.

**Important:** Teradata data types not included in the table aren't supported for data mapping in Workflow Data Fabric Hub.

|Teradata|Data fabric table|
|--------|-----------------|
|TINYINT|Long|
|SMALLINT|Long|
|INTEGER|Long|
|BIGINT|Long|
|REAL|Decimal|
|FLOAT|Decimal|
|DOUBLE|Decimal|
|NUMERIC|Decimal|
|DECIMAL|Decimal|
|NUMBER|Decimal|
|CHAR|Char|
|CHARACTER|Char|
|VARCHAR|String|
|BINARY|File Attachment|
|VARBINARY|File Attachment|
|DATE|Date|
|TIME|Date/Time|
|TIMESTAMP|Date/Time|
|TIME WITH TIME ZONE|Date/Time|
|TIMESTAMP WITH TIME ZONE|Date/Time|

**Related topics**  


[Create a Teradata connection](../task/create-teradata-connection.md)

