---
title: ServiceNow Remote Instance
description: The ServiceNow Remote Instance connector provides read-only access to another ServiceNow instance.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Primary connectors, Zero Copy Connectors, Workflow Data Fabric]
---

# ServiceNow Remote Instance

The ServiceNow Remote Instance connector provides read-only access to another ServiceNow instance.

The ServiceNow Remote Instance connector enables you to query tables residing in remote ServiceNow instances and access that data as if it were stored locally. This connector is designed to allow a central instance to retrieve records from one or more remote instances in real time.

A connection admin can set up a connection to a remote ServiceNow instance in the Zero Copy Connector Hub and grant data stewards access to this connection. Data stewards can then use the established connection to create a data fabric table and map data from the remote instance. This allows users to access remote ServiceNow data through the table list view or by using GlideRecord scripts. For details on creating data fabric tables and mapping data, see [Managing data fabric tables](managing-data-fabric-tables-zcc.md).

## How the connector works

After a zero copy connection is established and a data steward creates a data fabric table with mapped data, the connector queries the remote instance each time users access the data fabric table. Records are retrieved in real time and displayed in lists and forms, but they're never stored or persisted on your local instance. After users close the list or form, the retrieved data is purged from memory.

This approach differs from other data synchronization methods like Instance Data Replication \(IDR\) or custom API integrations because no data transfer or storage occurs on the local instance.

## Service account security model

Access to tables on the remote ServiceNow instance is controlled through a service account. The remote instance administrator creates this service account and grants it permissions to access only the specific tables required for the connection.

When configuring the connection, the connection admin provides the service account credentials. The permissions assigned to the service account on the remote instance determine which tables and fields are available through the zero copy connection. This security model ensures that data stewards can only map data that the remote instance administrator has explicitly made accessible.

Work with the remote instance administrator to perform the following tasks:

-   Create a dedicated service account for zero copy access.
-   Grant the service account read permissions to the required tables on the remote instance.
-   Document which tables and fields the service account can access.

## Use case

A managed service provider operates twelve ServiceNow instances for different business units, each containing incident, change, and asset data specific to that unit. Due to data residency regulations in multiple regions, records cannot be copied or moved between instances.

The provider designates one instance as the central processing instance where cross-organizational workflows and dashboards are managed. Using the ServiceNow Remote Instance connector, the central instance establishes zero copy connections to each of the twelve remote instances. Data stewards create data fabric tables that map incident and asset fields from the remote instances.

When an executive dashboard displays consolidated metrics, the central instance queries each remote instance and retrieves only the records needed for the current view. When a workflow requires a decision based on asset data from a specific region, the central instance looks up the relevant records without storing them. Throughout these operations, all data remains in its original instance, satisfying data residency requirements while providing the unified visibility the organization needs.

**Related topics**  


[Create a ServiceNow Remote Instance connection](../task/create-servicenow-remote-instance-connection.md)

