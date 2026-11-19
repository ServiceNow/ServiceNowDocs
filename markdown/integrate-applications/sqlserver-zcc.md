---
title: Microsoft SQL Server
description: The Microsoft SQL Server connector enables access to relational database data from your Microsoft SQL Server instance without moving or copying data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/sqlserver-zcc.html
release: brazil
topic_type: concept
last_updated: "2026-09-30"
reading_time_minutes: 2
keywords: [Microsoft SQL Server connector, zero-copy connector, JDBC connector, relational database, data fabric]
breadcrumb: [Primary connectors, Manage zero copy connections, Zero Copy Connectors, Workflow Data Fabric]
---

# Microsoft SQL Server

The Microsoft SQL Server connector enables access to relational database data from your Microsoft SQL Server instance without moving or copying data.

Connection admins set up connections to Microsoft SQL Server in the Zero Copy Connector Hub and grant data stewards access. Data stewards use the connection to create data fabric tables and map data from Microsoft SQL Server. Users can then access Microsoft SQL Server data through the table list view or GlideRecord scripts. For details, see [Managing data fabric tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/managing-data-fabric-tables-zcc.md).

**Note:**

This connector is available starting with Australia patch 6.

## Personal authentication

When you configure the connection with an access token, you can choose whether the connection uses a shared, system-level OAuth entity profile or personal authentication. With personal authentication, each user connects with their own credentials instead of a shared service account. Queries return only the data that user can access at the source.

For details on how personal authentication works and which connectors support it, see [Personal authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/personal-auth-zcc.md).

## Connector enhancements

The connector has been enhanced to improve the performance of the following Glide queries and list view operations. These improvements allow the majority of queries to be executed at the data source.

-   Sort
-   Limit
-   Offset
-   Join \(inner, left, right, full, and cross\)

The connector supports the following pushdowns:

-   Cast expressions
-   String functions: `LOWER`, `UPPER`
-   Date-part extraction, for example extracting the year from a date column

Unsupported expressions fall back to Trino with correct results.

The connector supports the following aggregate pushdowns:

-   `avg()`
-   `count()`
-   `max()`
-   `min()`
-   `sum()`
-   `STDDEV_SAMP`
-   `STDDEV_POP`
-   `VARIANCE_SAMP`
-   `VARIANCE_POP`
-   `COVAR_SAMP`
-   `COVAR_POP`
-   `CORR`
-   `REGR_INTERCEPT`
-   `REGR_SLOPE`

The connector also supports complex-expression pushdown, including the following:

-   Arithmetic operations
-   `CAST`
-   `AND`/`OR`
-   `IN`
-   `LIKE`

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


[Create a Microsoft SQL Server connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/create-sqlserver-connection-zcc.md)

[Microsoft SQL Server authentication method fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/sqlserver-authentication-method-fields-zcc.md)

[Personal authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/personal-auth-zcc.md)

