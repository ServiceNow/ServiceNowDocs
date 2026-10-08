---
title: ServiceNow Remote Instance
description: The ServiceNow Remote Instance connector provides read-only access to another ServiceNow instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/integrate-applications/workflow-data-fabric-hub/servicenow-remote-instance-wdf.html
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

A connection admin can set up a connection to a remote ServiceNow instance in the Workflow Data Fabric Hub and grant data stewards access to this connection. Data stewards can then use the established connection to create a data fabric table and map data from the remote instance. This allows users to access remote instance data through the table list view or by using GlideRecord scripts. For details on creating data fabric tables and mapping data, see [Managing data fabric tables in Workflow Data Fabric Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/workflow-data-fabric-hub/managing-data-fabric-tables-wdf.md).

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

## Oracle instance limitation

The remote ServiceNow instance must be running on a supported database platform when using the ServiceNow Remote Instance connector with Workflow Data Fabric or Workflow Data Fabric Hub.

**Warning:** Connecting to a ServiceNow instance that uses Oracle as its underlying database is not supported. Queries that include tables from an Oracle-backed ServiceNow instance fail. This limitation applies specifically to instance-to-instance connectivity through the ServiceNow Remote Instance connector. Workflow Data Fabric and Workflow Data Fabric Hub support direct connections to external Oracle databases through the Oracle connector.

**Related topics**  


[Create a ServiceNow Remote Instance connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/workflow-data-fabric-hub/create-servicenow-remote-instance-connection.md)

