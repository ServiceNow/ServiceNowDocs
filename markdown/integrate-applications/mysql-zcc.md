---
title: MySQL
description: The MySQL connector enables access to relational database data from your MySQL instance without moving or copying data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/mysql-zcc.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [MySQL connector, zero-copy connector, JDBC connector, relational database, data fabric]
breadcrumb: [Primary connectors, Zero Copy Connectors, Workflow Data Fabric]
---

# MySQL

The MySQL connector enables access to relational database data from your MySQL instance without moving or copying data.

Connection admins set up connections to MySQL in the Zero Copy Connector Hub and grant data stewards access. Data stewards use the connection to create data fabric tables and map data from MySQL. Users can then access MySQL data through the table list view or GlideRecord scripts. For details, see [Managing data fabric tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/managing-data-fabric-tables-zcc.md).

**Important:** The MySQL primary connector is in preview. A primary connector in preview is developed and supported by ServiceNow, but is still being enhanced to include all planned functionality. While in preview, a connector may have limitations in platform support or available features.

A primary connector in preview is fully functional for its documented scope and receives the same ServiceNow support as other primary connectors. For details on specific functionality limitations, see [KBB0010487](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KBB0010487).

The connector supports pushdown for the following Glide queries and list view operations, allowing most queries to execute at the data source:

-   Sort
-   Limit
-   Offset
-   Filter
-   GroupBy
-   avg\(\)
-   count\(\)
-   max\(\)
-   min\(\)
-   sum\(\)
-   References

The connector supports primary key and composite \(unique\) key detection on MySQL tables.

## Supported data types

The following table lists supported MySQL data types and the default matching data types in a data fabric table.

|MySQL|Data fabric table|
|-----|-----------------|
|tinyint unsigned|Integer|
|smallint unsigned|Integer|
|int unsigned|Long|
|bigint unsigned|Decimal|
|json|Not supported|
|enum|String|
|datetime|Basic Date/Time|
|bit\(1\)|True/False|
|tinyint|Long|
|smallint|Integer|
|int/integer|Integer|
|bigint|Long|
|float \(Real\)|Floating Point Number|
|DOUBLE|Floating Point Number|
|decimal/numeric|Decimal|
|char\(n\)|Char \(fixed-length character field\)|
|varchar/nvarchar/longvarchar/longvarchar|String \(variable-length character field\)|
|date|Date|
|time|Basic Time|
|timestamp|Date/Time|
|binary/varbinary/longvarbinary|Varbinary|

MySQL data types not included in the table aren't supported for data mapping in Zero Copy Connector Hub.

**Related topics**  


[Create a MySQL connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/create-mysql-connection-zcc.md)

