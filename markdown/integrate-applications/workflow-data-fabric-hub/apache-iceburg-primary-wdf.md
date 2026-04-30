---
title: Apache Iceberg
description: The Apache Iceberg connector provides read-only access to data and metadata in the Iceberg format.
locale: en-US
release: yokohama
product: Workflow Data Fabric Hub
classification: workflow-data-fabric-hub
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Primary connectors, Managing zero copy connections in Workflow Data Fabric Hub, Workflow Data Fabric Hub, Data and Automation]
---

# Apache Iceberg

The Apache Iceberg connector provides read-only access to data and metadata in the Iceberg format.

A connection admin can set up a connection to Apache Iceberg in the Workflow Data Fabric Hub and grant data stewards access to this connection. Data stewards can then use the established connection to create a data fabric table and map data from Apache Iceberg. This allows users to access Apache Iceberg data through the table list view or by using GlideRecord scripts. For details on creating data fabric tables and mapping data, see [Managing data fabric tables in Workflow Data Fabric Hub](managing-data-fabric-tables-wdf.md).

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

The following table lists supported Apache Iceberg data types and the default matching data types in a data fabric table.

**Important:** Apache Iceberg data types not included in the table aren't supported for data mapping in Workflow Data Fabric Hub.

|Apache Iceberg|Data fabric table|
|--------------|-----------------|
| | |
| | |
| | |
| | |
| | |
| | |
| | |
| | |
| | |
| | |
| | |
| | |
| | |

**Related topics**  


[Create an Apache Iceberg connection](../task/create-apache-iceberg-connection-primary.md)

