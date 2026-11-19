---
title: Databricks
description: The Databricks connector provides read-only access to data and metadata from the Databricks data analytics platform.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/integrate-applications/databricks-zcc.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Primary connectors, Manage zero copy connections, Zero Copy Connectors, Workflow Data Fabric]
---

# Databricks

The Databricks connector provides read-only access to data and metadata from the Databricks data analytics platform.

A connection admin can set up a connection to Databricks in the Zero Copy Connector Hub and grant data stewards access to this connection. Data stewards can then use the established connection to create a data fabric table and map data from Databricks. This allows users to access Databricks data through the table list view or by using GlideRecord scripts. For details on creating data fabric tables and mapping data, see [Managing data fabric tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/managing-data-fabric-tables-zcc.md).

**Note:**

This connector is available starting with Yokohama patch 5.

## Personal authentication

When you configure the connection with an access token, you can choose whether the connection uses a shared, system-level OAuth entity profile or personal authentication. With personal authentication, each user connects with their own credentials instead of a shared service account. Queries return only the data that user can access at the source.

For details on how personal authentication works and which connectors support it, see [Personal authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/personal-auth-zcc.md).

## Connector enhancements

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

The following table lists supported Databricks data types and the default matching data types in a data fabric table.

**Note:** Databricks data types not included in the table aren't supported for data mapping in Zero Copy Connector Hub.

|Databricks|Data fabric table|
|----------|-----------------|
|bigint|Long Integer String|
|int|Long Integer String|
|smallint|Long Integer String|
|tinyint|Long Integer String|
|timestamp\_ntz|Basic Date/Time|
|char|Char|
|timestamp|Basic Date/Time|
|date|Date|
|decimal|Decimal|
|string|String|
|boolean|True/False|
|double|Floating Point Number|
|float|Floating Point Number|

**Related topics**  


[Create a Databricks connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/create-databricks-connection-zcc.md)

[Databricks authentication method fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/databricks-authentication-method-fields-zcc.md)

[Personal authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/personal-auth-zcc.md)

