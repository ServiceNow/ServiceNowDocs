---
title: Telecom discovery via Arista VeloCloud SD-WAN
description: The Service Graph Connector for Arista VeloCloud discovers SD-WAN inventory from VeloCloud Orchestrator and imports it into the CMDB.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-service-ops/telecommunications-service-operations-management/telecom-discovery-via-arista-velocloud.html
release: australia
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: concept
last_updated: "2026-06-24"
reading_time_minutes: 3
breadcrumb: [Indirect Discovery with SGCs, Telecom Discovery, Telecom Visibility, Explore, Telecommunications Service Operations Management]
---

# Telecom discovery via Arista VeloCloud SD-WAN

The Service Graph Connector for Arista VeloCloud discovers SD-WAN inventory from VeloCloud Orchestrator and imports it into the CMDB.

## Key benefits

-   Automatically scans VeloCloud Orchestrator to import all configuration item \(CI\) data based on import schedules.
-   Keeps the CMDB up to date with the latest CI information.
-   Uses Integration Hub ETL to provide a graphical representation of VeloCloud SD-WAN networks, device relationships, and dependencies.

**Note:** For a general overview of Service Graph Connector technology, see [Getting started with Service Graph Connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/cmdb-sgc-intro.md).

## Arista VeloCloud SD-WAN architecture

The Arista VeloCloud SD-WAN architecture consists of three key components:

-   VeloCloud SD-WAN Edge: An enterprise-class appliance deployed at branch sites that provides secure, optimized connectivity to applications. The Edge aggregates multiple links and steers traffic using Dynamic Multipath Optimization \(DMPO\) and deep application recognition \(DAR\).
-   VeloCloud SD-WAN Gateway: A distributed network component that optimizes data paths between branches, data centers, and cloud services. Gateways provide scalability, redundancy, and on-demand flexibility.
-   VeloCloud Orchestrator: A cloud-hosted or on-premises central management platform for configuring, provisioning, and monitoring the SD-WAN environment. The Service Graph Connector communicates with VeloCloud Orchestrator to discover and import inventory data into the CMDB.

## Discovery modes

The Service Graph Connector for Arista VeloCloud supports two VeloCloud account topologies:

-   Partner \(MSP\) mode: Applies to an Enterprise Proxy \(partner\) account that owns and manages many customer enterprises.
-   Operator mode: Applies to a direct operator account that manages its own enterprises without a partner proxy.

You don't need to specify the mode or provide an organization identifier. When discovery runs, the connector checks whether the supplied credentials belong to a Partner \(Enterprise Proxy\) account. If they do, discovery proceeds in Partner \(MSP\) mode; if not, the connector uses Operator mode. The same scheduled data import works for both account types.

Both modes follow the same discovery sequence:

1.  Account and partner lookup: The connector determines whether the account is a partner proxy.
2.  Gateway pools: The connector retrieves the gateway pool information available to the account.
3.  Enterprise list: The connector retrieves the list of enterprises \(organizations\). In Partner \(MSP\) mode, the list includes edge information. In Operator mode, the list is retrieved without edge information.
4.  Edge devices: For each enterprise, the connector retrieves its edge devices, including high-availability status, configuration, licenses, links, and site details. Any edge device without a name is skipped during import in both modes.

The main differences between the two modes are described in the following table.

|Aspect|Partner \(MSP\) mode|Operator mode|
|------|--------------------|-------------|
|Account type|Enterprise Proxy \(partner\)|Direct operator|
|Enterprise list source|`getEnterpriseProxyEnterprises`|`getNetworkEnterprises`|
|Edge data in the enterprise list|Included|Retrieved separately for each enterprise|
|Enterprises with no edge devices|Skipped|Retained|
|Partner association|Each enterprise is linked to its parent partner|No partner parent|
|Enterprise identification|Identified within the scope of the parent partner|Identified by a globally unique identifier|

Regardless of the mode, the connector builds the same inventory — organizations, network sites, edge devices, and network service instances. The connector establishes the relationships between organizations and their network sites.

For the full list of VeloCloud Orchestrator endpoints called during discovery, with sample responses, see [Arista VeloCloud Service Graph Connector API Endpoints](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/arista-velocloud-service-graph-connector-api-endpoints.md).

## CMDB Integrations Dashboard

The Integration Commons for CMDB application provides a dashboard with a central view of the status, processing results, and processing errors of all installed Service Graph Connectors. The dashboard displays metrics for all integration runs. You can filter the view to a specific integration, time duration, or integration run. For more details about monitoring integrations in the CMDB Integrations Dashboard, see [Integration Commons for CMDB](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/integration-commons-for-cmdb.md).

**Related topics**  


[Configure Arista VeloCloud Service Graph Connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/configure-arista-velocloud-service-graph-connector.md)

[Run Arista VeloCloud SD-WAN Import](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/run-arista-velocloud-sd-wan-import.md)

