---
title: Configuring Workflow Data Fabric Hub
description: Set up and configure Workflow Data Fabric Hub.
locale: en-US
release: zurich
product: Workflow Data Fabric Hub
classification: workflow-data-fabric-hub
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Workflow Data Fabric Hub, Workflow Data Fabric]
---

# Configuring Workflow Data Fabric Hub

Set up and configure Workflow Data Fabric Hub.

## Configuration overview

The Workflow Data Fabric Hub application is free for all production instances and non-production instances.

You can install the Workflow Data Fabric Hub application in either of the following ways:

-   Install the Workflow Data Fabric Hub application \(sn\_data\_fabric\) from the ServiceNow Store.
-   Request the Zero Copy Connectors application \(sn\_data\_fabric\_zcc\), which includes the Workflow Data Fabric Hub application.

With access to the Workflow Data Fabric Hub, you can map a data fabric table included with an application to a local table on your instance using the ServiceNow local instance connector.

To create data fabric tables that can retrieve external data using zero copy connections, request the Zero Copy Connectors app \(sn\_data\_fabric\_zcc\). The Workflow Data Fabric Hub is automatically installed when the Zero Copy Connectors plugin \(sn\_data\_fabric\_zcc\) is activated on your instance.

-   **[Activate Workflow Data Fabric Hub](../task/activate-workflow-data-fabric-hub.md)**  
Access Workflow Data Fabric Hub on your instance by activating the Workflow Data Fabric Hub plugin \(sn\_data\_fabric\).
-   **[Request Zero Copy Connectors](../task/request-wdf.md)**  
Create zero copy connections and data fabric tables in Workflow Data Fabric Hub after requesting the Zero Copy Connectors app through the Now Support Service Catalog. If it isn't already installed, the app installs Workflow Data Fabric Hub.
-   **[Create a connection administrator](../task/create-connection-admin-wdf.md)**  
Create a connection admin who can create zero copy connections in Workflow Data Fabric Hub.
-   **[Enabling access to a data source](enabling-access-data-source-wdf.md)**  
Work with your data source administrator to enable access to your external data source.

**Parent Topic:**[Workflow Data Fabric Hub](workflow-data-fabric.md)

