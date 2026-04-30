---
title: TSOM Visibility
description: The TSOM Visibility solution is built on the foundational principles of ITOM Visibility, leveraging its proven frameworks for discovering and mapping IT resources.
locale: en-US
release: yokohama
product: Telecom Visibility
classification: telecom-visibility
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 6
breadcrumb: [Telecommunications Service Operations Management]
---

# TSOM Visibility

The TSOM Visibility solution is built on the foundational principles of ITOM Visibility, leveraging its proven frameworks for discovering and mapping IT resources.

In addition to the core ITOM Visibility functionalities, TSOM Visibility introduces a unique telecom-specific layer with tailored applications. These include Telecom Discovery, which leverages the Horizontal Discovery and Telecommunications Discovery Patterns application, Service Graph Connectors \(SGC\), and Telecom Discrepancy Identification &amp; Reconciliation, which incorporates telecom-specific logic introduced by the TSOM Visibility plugin. All components are designed to support the unique hierarchy and resource structures of the telecom data model. This combination enhances the discovery, reconciliation, and management of telecom infrastructure and services across complex multi-vendor, multi-technology networks, IT, and cloud environments.

**Note:** Additional TSOM applications and APIs related to TSOM Health and AIOps fall outside the scope of the TSOM Visibility solution and will be covered separately.

## TSOM: Architecture and Telecom Applications

![architecture and telecom applications.](../images/architecture-telecom-applications.png)

## TSOM Visibility: Telecom Discovery and Discrepancy Identification and Reconciliation

![telecom discovery and discrepancy identification.](../images/telecom-discovery-discrepancy-identification-reconciliation.png)

## Horizontal Discovery and Telecommunications Discovery Patterns

Horizontal Discovery is an automated process that continuously scans and identifies all the components within the network infrastructure. It plays a crucial role in maintaining an accurate and up-to-date CMDB and TNI with the information in the network.

In Telecom Discovery, we use Horizontal Discovery and Telecommunication \(TSOM\) Discovery Patterns \(sn\_tsom\_patterns\) to discover standalone xNFs using SNMP and CLI protocols.

For more information on the TSOM Patterns, see [Telecom Discovery using Telecommunications Discovery Patterns](telecom-discovery-using-telecommunication-discovery-pattern.md).

For more information on the Horizontal Discovery application, see [Horizontal discovery process flow with patterns](https://www.servicenow.com/docs/access?context=disco-process-flow-patterns&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US).

## Service Graph Connectors \(SGC\)

The Service Graph Connectors \(SGC\) are predefined integrations that ingest data into the Configuration Management Database \(CMDB\) from third-party sources. They can be used alongside any existing Service Graph Connectors, such as those for security, servers, software, monitoring, internet of Things \(IoT\), and cloud.

In Telecom Discovery, we use Service Graph Connectors to discover network resources via northbound APIs of EMS/NMS/Controllers, which manage various xNFs.

For more information on the Telecom SGSs, see [Telecom Discovery using Service Graph Connectors \(SGC\)](telecom-discovery-using-service-graph-connector.md).

## TSOM Visibility Applications

-   Service Graph Connectors \(TSOM SGCs\) –These new plugins enable the discovery of data from existing network management systems \(for example, EMS/NMS/Controllers\).
-   -   Plugin name: sn\_sgc\_altiplano\_connector
-   Plugin description: Service Graph Connector for Nokia Altiplano
    See [Telecom Discovery using Service Graph Connectors \(SGC\)](telecom-discovery-using-service-graph-connector.md).


-   Telecommunications Discovery Patterns \(TSOM Patterns\) – These new plugins include patterns for the discovery of standard SNMP-based standalone xNFs \(for example, telecom routers/switches without a management system or those intended to be discovered directly by bypassing their management systems\). They also include custom patterns for verifying specific Cisco and Juniper devices by leveraging their SNMP and CLI accessibility.
-   -   Plugin name: sn\_tsom\_patterns
-   Plugin description: Telecommunication Discovery Patterns
    See [Telecom Discovery using Telecommunications Discovery Patterns](telecom-discovery-using-telecommunication-discovery-pattern.md).


-   TSOM Visibility \(plugin\) – This plugin is an enabler of the TSOM Visibility applications. It contains logic that is common across our Telecom Discovery and Telecom Discrepancy Identification &amp; Reconciliation solution. It includes telecom-specific discrepancy identification and remediation logic, along with other common logic that we are building or will build for use across the application.
-   -   Plugin name: sn\_tsom\_core
-   Plugin description: TSOM Visibility \(plugin\)
    See [Telecom Discrepancy Identification and Reconciliation](telecom-reconciliation.md).


## CMDB 360

CMDB 360 retains a complete history of discovery sources and proposed values involved in updates to CI attributes. Use CMDB 360 data to track how the CMDB is populated by various discovery sources at the CI attribute level. You can also revert CI updates from a specific discovery source or recompute attribute values using updated reconciliation rules.

The CMDB 360 view provides aggregations and analyses of CMDB 360 data, which can be used to track activities and identify potential issues with discovery sources. Additionally, you can create custom queries, schedules, and reports to explore CMDB data.

For more information on CMDB 360, see [CMDB 360/Multisource CMDB](https://www.servicenow.com/docs/access?context=multisource-cmdb&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

## Discovery Admin Workspace

The Discovery Admin Workspace serves as a central location for monitoring, tracking, and completing discovery-related tasks. Experience a streamlined discovery process and greater efficiency with the integration of schedules, diagnostics, tuning, and more within this single workspace.

For more information on the Discovery Admin Workspace, see [Discovery Admin Workspace](https://www.servicenow.com/docs/access?context=discovery-admin-workspace&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US).

## Who uses TSOM Visibility

TSOM Visibility enables telecom operators and communication service providers \(CSP\) and providing platform as a service to discover their network resources.

The ServiceNow® Configuration Management Database \(CMDB\) and Telecom Network Inventory \(TNI\) aren’t operational tools. They’re strategic necessities in today’s IT and telecom landscape. Maintaining an accurate and complete CMDB/TNI provides the foundation for delivering critical services and drives multiple outcomes important to telecom operations, such as order/service fulfillment, inventory/asset management, and assurance. Having an up-to-date CMDB/Network Inventory is crucial for enabling high levels of Autonomous Network Operations \(ANO\) and essential for real-time decision-making, automation, and closed-loop operations.

## TSOM Visibility Installation Disclaimer

In order to support the TSOM Visibility solution, we have modified the [CMDB CI Class Models](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/it-operations-management/store-rn-itom-cmdb-class-models.html) store application, introducing updates to the IRE Identification Rules for the following telecom CIs:

-   Interface Cards
-   Slots
-   Subslots
-   Network Interfaces

TSOM Visibility requires CMDB CI Class Models Version 1.69.0 \(sn\_cmdb\_ci\_class\).

If you install any of the TSOM Visibility applications \(sn\_sgc\_altiplano\_connector, sn\_tsom\_patterns, or the sn\_tsom\_core plugin\), the CMDB CI Class Models store application is automatically updated \(or installed\) to Version 1.69.0.

**Note:** An administrator can still upgrade the CMDB CI Class Models store application to Version 1.69.0 at their discretion, regardless of whether their Yokohama instance has TSOM Visibility or even if their instance is on a pre-Yokohama release \(for example, Washington DC or Xanadu\).

**IMPORTANT!** If an administrator deploys CMDB CI Class Models Version 1.69.0—whether or not TSOM Visibility is installed—any customized IRE identification rules applied to one or more of the above-mentioned telecom CIs may be affected. These rules will require careful validation to ensure proper functionality.

## TSOM Visibility Licensing

The ServiceNow AI Platform uses a licensing model in which your organization is billed for the use of TSOM Visibility applications. Telecom Discovery, Telecom Discrepancy Identification &amp; Reconciliation and TSOM Visibility \(plugin\) are components of TSOM Visibility. To use TSOM Visibility, your organization must subscribe to TSOM.

**Note:** ServiceNow’s product documentation doesn’t include details on pricing, packaging, or other specifics, as these are determined by your organization's customer contract.

-   **[Telecom Discovery](telecom-discovery-tsom-visibility.md)**  
ServiceNow® Telecom Discovery \(also known as TSOM Discovery\) is a specialized solution within the broader ServiceNow ecosystem, designed to cater to the unique needs of telecommunications service providers \(CSPs\) in discovering and managing their telecom network assets.
-   **[Telecom Discrepancy Identification and Reconciliation](telecom-reconciliation.md)**  
Telecom Discrepancy Identification &amp; Reconciliation confirms that ServiceNow’s CMDB/TNI accurately reflects the updated state of the network and remains synchronized with planned or designed inventory resources.

**Parent Topic:**[Telecommunications Service Operations Management](telecom-service-operations-mgt-overview.md)

