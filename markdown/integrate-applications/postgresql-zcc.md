---
title: PostgreSQL
description: The PostgreSQL connector enables access to relational database data from your PostgreSQL instance without moving or copying data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/postgresql-zcc.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [PostgreSQL connector, zero-copy connector, JDBC connector, relational database, data fabric]
breadcrumb: [Primary connectors, Zero Copy Connectors, Workflow Data Fabric]
---

# PostgreSQL

The PostgreSQL connector enables access to relational database data from your PostgreSQL instance without moving or copying data.

Connection admins set up connections to PostgreSQL in the Zero Copy Connector Hub and grant data stewards access. Data stewards use the connection to create data fabric tables and map data from PostgreSQL. Users can then access PostgreSQL data through the table list view or GlideRecord scripts. For details, see [Managing data fabric tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/managing-data-fabric-tables-zcc.md).

For known limitations, see the Knowledge Base article [PostgreSQL connector known limitations \(KBB0010487\)](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KBB0010487).

The connector supports primary key and composite \(unique\) key detection on PostgreSQL tables.

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

The connector also supports the following statistical aggregate pushdowns: `STDDEV_SAMP`, `STDDEV_POP`, `VARIANCE_SAMP`, `VARIANCE_POP`, `COVAR_SAMP`, `COVAR_POP`, `CORR`, `REGR_INTERCEPT`, and `REGR_SLOPE`. The connector also supports complex-expression pushdown, including arithmetic operations, `CAST`, `AND`/`OR`, `IN`, and `LIKE`.

## Supported data types

**Note:** The following PostgreSQL data types aren't supported: `BYTEA`, `UUID`, `JSON`, `JSONB`, `VECTOR`, `HSTORE`, `ARRAY`, `GEOMETRY`, `GEOMETRY(GEOMETRY TYPE, SRID)`, and `POINT`.

|PostgreSQL|Data fabric table|
|----------|-----------------|
|bit|True/False|
|boolean|True/False|
|smallint|Integer|
|integer|Integer|
|bigint|Long|
|real|Floating Point Number|
|double|Floating Point Number|
|numeric\(p, s\)|Decimal|
|decimal\(p', s'\)|Decimal|
|numeric \(unconstrained\)|Decimal|
|char\(n\)|Char \(fixed-length character field\)|
|varchar\(n\)|String \(variable-length character field\)|
|enum|String|
|date|Date|
|time\(n\)|Basic Time|
|timestamp\(n\)|Basic Date/Time|
|timestampz\(n\)|Date/Time|
|money|String|

**Related topics**  


[Create a PostgreSQL connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/create-postgresql-connection-zcc.md)

