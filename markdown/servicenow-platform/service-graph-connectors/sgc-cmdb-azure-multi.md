---
title: Setting up multiple connections in Service Graph Connector for Microsoft Azure
description: The Service Graph Connector for Microsoft Azure supports multiple Azure connections.
locale: en-US
release: australia
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Azure connector, multiple Azure workspaces, multiple Azure connections]
breadcrumb: [Additional features, Microsoft Azure, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Setting up multiple connections in Service Graph Connector for Microsoft Azure

The Service Graph Connector for Microsoft Azure supports multiple Azure connections.

**Important:** Add multiple connections by selecting **Add connection** on the Connections page of the Workflow Studio in the guided setup. For more information, see [Configure Service Graph Connector for Microsoft Azure](../task/configure-azure-integration.md).

## Setting up multiple connections

You can set up a hardware or software connection by using the guided setup. The Service Graph Connector for Microsoft Azure supports only one-to-one mapping between hardware and software connections. Therefore, when configuring multiple software connections, you must also configure an equivalent number of hardware connections. You can differentiate multiple connections using their respective connection aliases.

For example, if you add 10 software connections for 10 different workspaces, you must also add 10 hardware connections for each corresponding software connection.

## Setting up multiple workspaces

You can set up a workspace when adding a software connection using the guided setup. To set up multiple workspaces, you must configure that many different software connections in the Service Graph Connector for Microsoft Azure as there are workspaces and an equivalent number of hardware connections.

For example, if you have 10 workspaces, you must add 10 software connections for each workspace and 10 hardware connections for each corresponding software connection.

