---
title: Oracle DB
description: The Oracle DB connector provides read-only access to data and metadata from an Oracle database.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/integrate-applications/oracle-zcc.html
release: australia
topic_type: concept
last_updated: "2026-11-11"
reading_time_minutes: 2
breadcrumb: [Primary connectors, Manage zero copy connections, Zero Copy Connectors, Workflow Data Fabric]
---

# Oracle DB

The Oracle DB connector provides read-only access to data and metadata from an Oracle database.

**Note:**

In the Zero Copy Connector Hub, this connector name is **Oracle**.

A connection admin can set up a connection to Oracle in the Zero Copy Connector Hub and grant data stewards access to this connection. Data stewards can then use the established connection to create a data fabric table and map data from Oracle. This allows users to access Oracle data through the table list view or by using GlideRecord scripts. For details on creating data fabric tables and mapping data, see [Managing data fabric tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/managing-data-fabric-tables-zcc.md).

**Note:**

This connector is available starting with Yokohama patch 5.

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

## Personal authentication

When you configure the connection with an access token, you can choose whether the connection uses a shared, system-level OAuth entity profile or personal authentication. With personal authentication, each user connects with their own credentials instead of a shared service account. Queries return only the data that user can access at the source.

For details on how personal authentication works and which connectors support it, see [Personal authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/personal-auth-zcc.md).

## Supported data types

The following table lists supported Oracle data types and the default matching data types in a data fabric table.

**Important:** Oracle data types not included in the table aren't supported for data mapping in Zero Copy Connector Hub.

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


[Create an Oracle DB connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/create-oracle-connection-zcc.md)

[Personal authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/personal-auth-zcc.md)

