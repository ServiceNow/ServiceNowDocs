---
title: Telecom Discovery via Fortinet SD-WAN
description: The Service Graph Connector for Fortinet provides a telecom-aware integration that imports real-time network inventory data from the Fortinet network management system into the Configuration Management Database \(CMDB\). This integration enhances visibility and management of network resources.
locale: en-US
release: australia
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: concept
last_updated: "2026-05-09"
reading_time_minutes: 2
breadcrumb: [Indirect Discovery with SGCs, Telecom Discovery, Explore, Telecommunications Service Operations Management]
---

# Telecom Discovery via Fortinet SD-WAN

The Service Graph Connector for Fortinet provides a telecom-aware integration that imports real-time network inventory data from the Fortinet network management system into the Configuration Management Database \(CMDB\). This integration enhances visibility and management of network resources.

## Key benefits

-   Accurate inventory synchronization: Automatically populate the CMDB with up-to-date physical and logical inventory from Fortinet using secure, REST API-based ingestion. SD-WAN devices, interface cards, ports, slots, and logical connections are included.
-   Telecom-aware CI modeling: Model your network infrastructure in a telecom-aligned format using purpose-built CI classes and relationships. The connector promotes an accurate representation of devices and their dependencies that mirrors your network topology.
-   Simplified and Guided setup: Reduce time-to-value with a built-in guided setup that walks you through connection configuration, data source management, and import scheduling with ease.
-   Flexible discovery options: Choose how and when to run discovery. Apply custom filters by device IP or name.

**Note:** For a general overview of Service Graph Connector technology, see [Getting started with Service Graph Connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/cmdb-sgc-intro.md).

## Fortinet SD-WAN architecture

The Fortinet SD-WAN architecture is composed of three key components:

1.  FortiPortal: A cloud-based service through which you register for Fortinet accounts and manage their licenses.
2.  FortiManager: A centralized management solution used to oversee and manage SD-WAN networks.
3.  FortiAnalyzer: A security analytics and reporting tool that collects and analyzes logs from Fortinet devices to identify potential security threats and conformance issues. Alerts are sent through a preconfigured webhook, and metrics are retrieved through API calls.

Fortinet APIs use JSON-RPC to enable programmatic interaction with FortiManager and FortiAnalyzer for bulk configuration, device management, and inventory collection.

The following infographic illustrates the architecture of the Fortinet Service Graph Connector.

![Fortinet SD-WAN architecture](../images/fortinet-service-connector-vertical.svg)

## CMDB Integrations Dashboard

The Integration Commons for CMDB application provides a dashboard with a central view of the status, processing results, and processing errors of all installed Service Graph Connectors. The dashboard displays metrics for all integration runs. You can filter the view to a specific integration, time duration, or integration run. For more details about monitoring integrations in the CMDB Integrations Dashboard, see [Integration Commons for CMDB](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/cmdb-integration-commons/integration-commons-for-cmdb.md).

**Related topics**  


[Configure a Fortinet SD-WAN Service Graph Connector](configure-fortinet-service-graph-connector.md)

[Run and verify an import schedule for Fortinet SGC](../task/run-and-verify-import-for-fortinet-sd-wan.md)

