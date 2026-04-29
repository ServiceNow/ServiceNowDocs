---
title: Managing zero copy connections
description: Securely connect to an external data source and access external data directly from your instance, without the need to copy or store any data locally.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Zero Copy Connectors, Workflow Data Fabric]
---

# Managing zero copy connections

Securely connect to an external data source and access external data directly from your instance, without the need to copy or store any data locally.

## Overview of managing zero copy connections

A zero copy connection provides secure, real-time access to data from outside sources without having to copy data to your local database. The connection admin is responsible for creating and managing zero copy connections as shown in this infographic.

![The connection admin selects the connector for a data source, creates a zero copy connection, grants data steward access to the connection, and maintains the connection.](../../../administer/workflow-data-fabric/image/MMASSET0020811-creating-connections-in-workflow-data-fabric-hub-landing.png "Creating and managing zero copy connections")

## Types of connectors

A connection admin with the df\_connection\_admin role can create connections to available data sources using primary and community connectors.

-   **Primary connectors**

    Primary connectors are developed, made available, and supported by ServiceNow. Primary connectors have been enhanced to improve the performance of Glide queries and list view operations. These improvements allow the majority of queries to be executed at the data source.

-   **Community connectors**

    Community connectors are developed by the open-source community and made available by ServiceNow. These connectors are certified for essential functionality but are not part of the ServiceNow support scope.


-   **[Manage access to an established connection using roles](../task/manage-access-connection-zcc.md)**  
Manage which data stewards can access an established connection and create data fabric tables.
-   **[View data assets from an established connection](../task/view-assets-connection-zcc.md)**  
View the external schema and tables that are accessible to the service account used in a zero copy connection.
-   **[Monitoring established connections](monitoring-connection-status-zcc.md)**  
Maintain the health of established connections by monitoring connection status in Zero Copy Connector Hub.
-   **[Update an established connection](../task/configure-connection-details-zcc.md#)**  
Keep connection details current by updating service account information, authentication, or security settings.
-   **[Test an established connection](../task/test-connection-zcc.md)**  
Test the connection to an external data source from an established connection.

**Parent Topic:**[Zero Copy Connectors](zero-copy-connectors.md)

