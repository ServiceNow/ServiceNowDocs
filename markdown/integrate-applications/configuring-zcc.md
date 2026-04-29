---
title: Configuring Zero Copy Connectors
description: Set up and configure Zero Copy Connectors.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Zero Copy Connectors, Workflow Data Fabric]
---

# Configuring Zero Copy Connectors

Set up and configure Zero Copy Connectors.

## Configuration overview

The Zero Copy Connector Hub application is free for all production instances and non-production instances.

You can install the Zero Copy Connector Hub in either of the following ways:

-   Install the Zero Copy Connector Hub application \(sn\_data\_fabric\) from the ServiceNow Store.
-   Request the Zero Copy Connectors application \(sn\_data\_fabric\_zcc\), which includes the Zero Copy Connector Hub application.

With access to the Zero Copy Connector Hub, you can map a data fabric table included with an application to a local table on your instance using the ServiceNow local instance connector.

To create data fabric tables that can retrieve external data using zero copy connections, request the Zero Copy Connectors app \(sn\_data\_fabric\_zcc\). The Zero Copy Connector Hub is automatically installed when the Zero Copy Connectors plugin \(sn\_data\_fabric\_zcc\) is activated on your instance.

-   **[Activate Zero Copy Connector Hub](../task/activate-zcc-hub.md)**  
Access the Zero Copy Connector Hub on your instance by activating the Zero Copy Connector Hub plugin \(sn\_data\_fabric\).
-   **[Request Zero Copy Connectors](../task/request-zcc.md)**  
Create zero copy connections and data fabric tables after requesting the Zero Copy Connectors app through the Now Support Service Catalog. If it isn't already installed, the app installs the Zero Copy Connector Hub.
-   **[Create a connection administrator](../task/create-connection-admin-zcc.md)**  
Create a connection admin who can create zero copy connections in Zero Copy Connector Hub.
-   **[Enabling access to a data source](enabling-access-data-source-zcc.md)**  
Work with your data source administrator to enable access to your external data source.

**Parent Topic:**[Zero Copy Connectors](zero-copy-connectors.md)

