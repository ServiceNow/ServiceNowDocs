---
title: Amazon S3 Tables
description: The Amazon S3 Tables connector provides read-only access to data and metadata in Amazon S3 Tables.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Primary connectors, Zero Copy Connectors, Workflow Data Fabric]
---

# Amazon S3 Tables

The Amazon S3 Tables connector provides read-only access to data and metadata in Amazon S3 Tables.

A connection admin can set up a connection to Amazon S3 Tables in the Zero Copy Connector Hub and grant data stewards access to this connection. Data stewards can then use the established connection to create a data fabric table and map data from S3 Tables. This allows users to access data in S3 Tables through the table list view or by using GlideRecord scripts. For details on creating data fabric tables and mapping data, see [Managing data fabric tables](managing-data-fabric-tables-zcc.md).

**Important:** The Amazon S3 Tables primary connector is in preview. A primary connector in preview is developed and supported by ServiceNow, but is still being enhanced to include all planned functionality. While in preview, a connector may have limitations in platform support or available features.

A primary connector in preview is fully functional for its documented scope and receives the same ServiceNow support as other primary connectors. For details on specific functionality limitations, see [KBB0010487](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KBB0010487).

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

The following table lists supported Amazon S3 Tables data types and the default matching data types in a data fabric table.

**Important:** Amazon S3 Tables data types not included in the table aren't supported for data mapping in Zero Copy Connector Hub.

|Amazon S3 Tables|Data fabric table|
|----------------|-----------------|
|boolean|True/False|
|int|Integer|
|long|Long|
|float|Floating Point Number|
|double|Decimal|
|decimal\(p,s\)|Decimal/Currency|
|string|String|
|date|Date|
|timestamp|Date/Time|
|timestamptz|Date/Time|
|uuid|GUID|

**Related topics**  


[create-databricks-connection]

