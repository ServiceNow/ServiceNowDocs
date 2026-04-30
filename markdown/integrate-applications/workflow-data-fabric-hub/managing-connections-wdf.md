---
title: Managing zero copy connections in Workflow Data Fabric Hub
description: Securely connect to an external data source and access external data directly from your instance, without the need to copy or store any data locally.
locale: en-US
release: zurich
product: Workflow Data Fabric Hub
classification: workflow-data-fabric-hub
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Workflow Data Fabric Hub, Workflow Data Fabric]
---

# Managing zero copy connections in Workflow Data Fabric Hub

Securely connect to an external data source and access external data directly from your instance, without the need to copy or store any data locally.

## Overview of managing zero copy connections

A zero copy connection provides secure, real-time access to data from outside sources without having to copy data to your local database. The connection admin is responsible for creating and managing zero copy connections as shown in this infographic.

![The connection admin selects the connector for a data source, creates a zero copy connection, grants data steward access to the connection, and maintains the connection.](../image/MMASSET0020811-creating-connections-in-workflow-data-fabric-hub-landing.png "Creating and managing zero copy connections")

## Types of connectors

A connection admin with the df\_connection\_admin role can create connections to available data sources using primary and community connectors.

-   **Primary connectors**

    Primary connectors are developed, made available, and supported by ServiceNow. Primary connectors have been enhanced to improve the performance of Glide queries and list view operations. These improvements allow the majority of queries to be executed at the data source.

-   **Community connectors**

    Community connectors are developed by the open-source community and made available by ServiceNow. These connectors are certified for essential functionality but are not part of the ServiceNow support scope.


-   **[Primary connectors](primary-connectors-wdf.md)**  
Connect to external data sources using primary connectors in Workflow Data Fabric Hub.
-   **[Community connectors](community-connectors-wdf.md)**  
Connect to external data sources using community connectors in Workflow Data Fabric Hub.
-   **[Manage access to an established connection using roles](../task/manage-access-connection-wdf.md)**  
Manage which data stewards can access an established connection and create data fabric tables.
-   **[View data assets from an established connection](../task/view-assets-connection-wdf.md)**  
View the external schema and tables that are accessible to the service account used in a zero copy connection.
-   **[Monitoring established connections](monitoring-connection-status-wdf.md)**  
Maintain the health of established connections by monitoring connection status in Workflow Data Fabric Hub.
-   **[Update an established connection](../task/configure-connection-details-wdf.md#)**  
Keep connection details current by updating service account information, authentication, or security settings.
-   **[Test an established connection](../task/test-connection-wdf.md)**  
Test the connection to an external data source from an established connection.

**Parent Topic:**[Workflow Data Fabric Hub](workflow-data-fabric.md)

