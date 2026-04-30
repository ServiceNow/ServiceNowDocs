---
title: ServiceNow Remote Instance
description: The ServiceNow Remote Instance connector provides read-only access to another ServiceNow instance.
locale: en-US
release: zurich
product: Workflow Data Fabric Hub
classification: workflow-data-fabric-hub
topic_type: concept
last_updated: "2025-10-01"
reading_time_minutes: 1
breadcrumb: [Primary connectors, Manage zero copy connections, Workflow Data Fabric Hub, Workflow Data Fabric]
---

# ServiceNow Remote Instance

The ServiceNow Remote Instance connector provides read-only access to another ServiceNow instance.

A connection admin can set up a connection to a remote ServiceNow instance in the Workflow Data Fabric Hub and grant data stewards access to this connection. Data stewards can then use the established connection to create a data fabric table and map data from the remote instance. This allows users to access remote instance data through the table list view or by using GlideRecord scripts. For details on creating data fabric tables and mapping data, see [Managing data fabric tables in Workflow Data Fabric Hub](managing-data-fabric-tables-wdf.md).

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

The following table lists supported ServiceNow data types and the default matching data types in a data fabric table.

**Important:** ServiceNow data types not included in the table aren't supported for data mapping in Workflow Data Fabric Hub.

|ServiceNow|Data fabric table|
|----------|-----------------|
| | |
| | |
| | |

**Related topics**  


[Create a ServiceNow Remote Instance connection](../task/create-servicenow-remote-instance-connection.md)

