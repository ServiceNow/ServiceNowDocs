---
title: Amazon Redshift
description: The Amazon Redshift connector provides read-only access to data and metadata from the Redshift data warehouse service.
locale: en-US
release: zurich
product: Workflow Data Fabric Hub
classification: workflow-data-fabric-hub
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Primary connectors, Manage zero copy connections, Workflow Data Fabric Hub, Workflow Data Fabric]
---

# Amazon Redshift

The Amazon Redshift connector provides read-only access to data and metadata from the Redshift data warehouse service.

A connection admin can set up a connection to Amazon Redshift in the Workflow Data Fabric Hub and grant data stewards access to this connection. Data stewards can then use the established connection to create a data fabric table and map data from Amazon Redshift. This allows users to access Amazon Redshift data through the table list view or by using GlideRecord scripts. For details on creating data fabric tables and mapping data, see [Managing data fabric tables in Workflow Data Fabric Hub](managing-data-fabric-tables-wdf.md).

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

The following table lists supported Amazon Redshift data types and the default matching data types in a data fabric table.

**Important:** Amazon Redshift data types not included in the table aren't supported for data mapping in Workflow Data Fabric Hub.

|Amazon Redshift|Data fabric table|
|---------------|-----------------|
|smallint|Integer|
|integer|Integer|
|bigint|Long Integer String|
|decimal|Decimal|
|numeric|Decimal|
|double|Floating Point Number|
|float4|Floating Point Number|
|float8|Floating Point Number|
|char|String|
|varchar|String|
|text|String|
|date|Date|
|timestamp|Basic Date/Time|
|timestamptz|Date/Time|
|boolean|True/False|

**Related topics**  


[Create an Amazon Redshift connection](../task/create-amazon-redshift-connection.md)

