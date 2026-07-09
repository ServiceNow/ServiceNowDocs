---
title: Cloudera Impala
description: The Cloudera Impala connector provides read-only access to data and metadata in Cloudera Impala.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/cloudera-impala-zcc.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Primary connectors, Zero Copy Connectors, Workflow Data Fabric]
---

# Cloudera Impala

The Cloudera Impala connector provides read-only access to data and metadata in Cloudera Impala.

A connection admin can set up a connection to Cloudera Impala in the Zero Copy Connector Hub and grant data stewards access to this connection. Data stewards can then use the established connection to create a data fabric table and map data from Cloudera Impala. This allows users to access Cloudera Impala data through the table list view or by using GlideRecord scripts. For details on creating data fabric tables and mapping data, see [Managing data fabric tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/managing-data-fabric-tables-zcc.md).

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

The following table lists supported Cloudera Impala data types and the default matching data types in a data fabric table.

**Important:** Cloudera Impala data types not included in the table aren't supported for data mapping in Zero Copy Connector Hub.

|Cloudera Impala|Data fabric table|
|---------------|-----------------|
|BOOLEAN|Boolean|
|TINYINT|Long|
|SMALLINT|Long|
|INTEGER|Long|
|BIGINT|Long|
|REAL|Decimal|
|FLOAT|Decimal|
|DOUBLE|Decimal|
|NUMERIC|Decimal|
|DECIMAL|Decimal|
|CHAR|String|
|VARCHAR|String|
|DATE|Date|
|TIMESTAMP|Date/Time|
|BINARY|File attachment|

**Related topics**  


[Create a Cloudera Impala connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/create-cloudera-impala-connection.md)

