---
title: Microsoft SQL Server
description: The Microsoft SQL Server connector enables access to relational database data from your Microsoft SQL Server instance without moving or copying data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/integrate-applications/sqlserver-zcc.html
release: australia
topic_type: concept
last_updated: "2026-09-30"
reading_time_minutes: 2
keywords: [Microsoft SQL Server connector, zero-copy connector, JDBC connector, relational database, data fabric]
breadcrumb: [Primary connectors, Zero Copy Connectors, Workflow Data Fabric]
---

# Microsoft SQL Server

The Microsoft SQL Server connector enables access to relational database data from your Microsoft SQL Server instance without moving or copying data.

Connection admins set up connections to Microsoft SQL Server in the Zero Copy Connector Hub and grant data stewards access. Data stewards use the connection to create data fabric tables and map data from Microsoft SQL Server. Users can then access Microsoft SQL Server data through the table list view or GlideRecord scripts. For details, see [Managing data fabric tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/managing-data-fabric-tables-zcc.md).

When you configure the connection with an access token, you can choose whether the connection authenticates using a shared, system-level OAuth entity profile or personal authentication.

**Note:** With personal authentication, each user's access to Microsoft SQL Server data is authenticated and audited against their own credentials, not a shared account. This supports stricter access control and clearer audit trails.

The connector supports pushdown for the following Glide queries and list view operations, allowing most queries to execute at the data source:

-   Sort
-   Limit
-   Offset
-   Join \(inner, left, right, full, and cross\)

The connector also supports pushdown for cast expressions, string functions such as `LOWER` and `UPPER`, and date-part extraction, for example extracting the year from a date column. Unsupported expressions fall back to Trino with correct results.

The connector also supports the following aggregate pushdowns: `avg()`, `count()`, `max()`, `min()`, `sum()`, `STDDEV_SAMP`, `STDDEV_POP`, `VARIANCE_SAMP`, `VARIANCE_POP`, `COVAR_SAMP`, `COVAR_POP`, `CORR`, `REGR_INTERCEPT`, and `REGR_SLOPE`. The connector also supports complex-expression pushdown, including arithmetic operations, `CAST`, `AND`/`OR`, `IN`, and `LIKE`.

## Supported data types

The following table lists supported Microsoft SQL Server data types and the default matching data types in a data fabric table.

**Note:** Microsoft SQL Server data types not included in the table aren't supported for data mapping in Zero Copy Connector Hub.

|Microsoft SQL Server|Data fabric table|
|--------------------|-----------------|
|BIT|True/False|
|TINYINT|Integer|
|SMALLINT|Integer|
|INT|Integer|
|BIGINT|Long|
|DECIMAL\(p, s\)|Decimal|
|NUMERIC\(p, s\)|Decimal|
|FLOAT\(n\)|Floating Point Number|
|REAL|Floating Point Number|
|DATE|Date|
|TIME\(n\)|Basic Time|
|DATETIME2\(n\)|Basic Date/Time|
|SMALLDATETIME|Basic Date/Time|
|DATETIMEOFFSET\(n\)|Date/Time|
|CHAR\(n\)|Char|
|VARCHAR\(n\)|String|
|TEXT|String|
|NCHAR\(n\)|Char|
|NVARCHAR\(n\)|String|
|NTEXT|String|
|VARBINARY\(n\)|String|

**Related topics**  


[Create a Microsoft SQL Server connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/create-sqlserver-connection-zcc.md)

