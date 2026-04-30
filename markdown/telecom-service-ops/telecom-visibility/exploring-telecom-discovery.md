---
title: Exploring Telecom Discovery
description: ServiceNow Telecom Discovery solution builds on proven technologies within the ServiceNow platform, leveraging powerful capabilities such as ITOM Visibility and Horizontal Discovery, and the Service Graph Connectors. Each of these components plays a key role in supporting telecom-specific use cases while also maintaining flexibility for general IT/Cloud discovery.
locale: en-US
release: yokohama
product: Telecom Visibility
classification: telecom-visibility
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Telecom Discovery, TSOM Visibility, Telecommunications Service Operations Management]
---

# Exploring Telecom Discovery

ServiceNow® Telecom Discovery solution builds on proven technologies within the ServiceNow® platform, leveraging powerful capabilities such as ITOM Visibility and Horizontal Discovery, and the Service Graph Connectors. Each of these components plays a key role in supporting telecom-specific use cases while also maintaining flexibility for general IT/Cloud discovery.

![telecom network.](../images/exploring-telecom-discovery.png)

The TSOM Visibility Plugins can be seamlessly used alongside the ITOM Visibility to enhance infrastructure discovery and visibility. By integrating these plugins, organizations can leverage TSOMs advanced Telecommunications Discovery Patterns and Service Graph Connectors \(SGC\) with ITOM's capabilities, enabling comprehensive identification and mapping of network components, services, and configurations. This combined approach confirms an accurate and enriched data population within the CMDB, providing a unified and detailed view of IT and telecom network resources.

**TSOM Visibility Plugins:**

## Service Graph Connectors \(SGC\)

This new plugin enables the discovery of data from existing network management systems \(for example, EMS/NMS/Controllers\), with a focus in this release on integrating Nokia Altiplano Access SDN Control via REST API. It’s a customer-visible plugin and must be installed individually.

Plugin name: sn\_sgc\_altiplano\_connector.

Plugin description: Service Graph Connector for Nokia Altiplano.

For more information, see [Telecom Discovery using Service Graph Connectors \(SGC\)](telecom-discovery-using-service-graph-connector.md).

## Telecommunications Discovery Patterns \(TSOM Patterns\)

This new plugin includes patterns for the discovery of standard SNMP-based, standalone xNFs \(for example, telecom routers and switches without a management system or those we want to discover directly by bypassing their management systems\), as well as custom patterns for verifying specific Cisco and Juniper devices by leveraging their SNMP and CLI accessibility.

Plugin name: sn\_tsom\_patterns.

Plugin description: Telecommunication Discovery Patterns.

For more information, see [Telecom Discovery using Telecommunications Discovery Patterns](telecom-discovery-using-telecommunication-discovery-pattern.md).

## TSOM Visibility plugin

This plugin contains logic that is common across our TSOM Visibility application. It includes telecom-specific discrepancy and remediation logic, along with other common logic that we are building or will build for use across the application.

Plugin name: sn\_tsom\_core.

Plugin description: Telecom Service Operations Core.

For more information, see [Telecom Discrepancy Identification and Reconciliation](telecom-reconciliation.md).

ServiceNow provides customers and partners with the capability to create and modify Service Graph Connectors and Telecommunications Discovery Patterns. To simplify this process, ServiceNow has developed a set of **no-code/low-code UI-based design tools**. These tools enable users to customize and extend Service Graph Connectors and Patterns without needing deep coding expertise, confirming flexibility, and faster deployment of tailored solutions for specific network environments.

-   **[Telecom Discovery using Telecommunications Discovery Patterns](telecom-discovery-using-telecommunication-discovery-pattern.md)**  
The new Telecommunication Discovery Patterns \(also known as TSOM Patterns\) include patterns for discovering standalone xNFs, enabling the discovery of standalone network elements without a management system, using SNMP, CLI, and NETCONF \(roadmap\) protocols.
-   **[Telecom Discovery using Service Graph Connectors \(SGC\)](telecom-discovery-using-service-graph-connector.md)**  
Service Graph Connectors are predefined integrations that ingest data into the Configuration Management Database \(CMDB\) from third-party sources \(for example, northbound APIs of EMS/NMS/Controllers, which manage various xNFs\) across different network domains, while enabling a structured, telecom-model-aligned view of network resources and services.

**Parent Topic:**[Telecom Discovery](telecom-discovery-tsom-visibility.md)

