---
title: Google BigQuery
description: The Google BigQuery connector provides read-only access to data and metadata from the Google BigQuery data warehouse service.
locale: en-US
release: zurich
product: Workflow Data Fabric Hub
classification: workflow-data-fabric-hub
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Primary connectors, Manage zero copy connections, Workflow Data Fabric Hub, Workflow Data Fabric]
---

# Google BigQuery

The Google BigQuery connector provides read-only access to data and metadata from the Google BigQuery data warehouse service.

A connection admin can set up a connection to Google BigQuery in the Workflow Data Fabric Hub and grant data stewards access to this connection. Data stewards can then use the established connection to create a data fabric table and map data from Google BigQuery. This allows users to access Google BigQuery data through the table list view or by using GlideRecord scripts. For details on creating data fabric tables and mapping data, see [Managing data fabric tables in Workflow Data Fabric Hub](managing-data-fabric-tables-wdf.md).

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

The following table lists supported Google BigQuery data types and the default matching data types in a data fabric table.

**Important:** Google BigQuery data types not included in the table aren't supported for data mapping in Workflow Data Fabric Hub.

|Google BigQuery|Data fabric table|
|---------------|-----------------|
|date|Date|
|numeric|Decimal|
|string|String|
|int64|Long Integer String|
|boolean|True/False|

**Related topics**  


[Create a Google BigQuery connection](../task/create-bigquery-connection.md)

