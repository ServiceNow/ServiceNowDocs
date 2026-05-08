---
title: Direct Discovery using Discovery Patterns
description: The Telecommunications Discovery Patterns plugin \(also known as TSOM Patterns\) extends ServiceNow AI Platform Telecom Discovery to support direct discovery of standalone network elements—such as routers and switches—without relying on traditional network management systems. These patterns enable Communication Service Providers \(CSPs\) to identify and map multivendor xNFs using protocols like SNMP and CLI, with support for NETCONF.
locale: en-US
release: australia
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Telecom Discovery, Explore, Telecommunications Service Operations Management]
---

# Direct Discovery using Discovery Patterns

The Telecommunications Discovery Patterns plugin \(also known as TSOM Patterns\) extends ServiceNow AI Platform Telecom Discovery to support direct discovery of standalone network elements—such as routers and switches—without relying on traditional network management systems. These patterns enable Communication Service Providers \(CSPs\) to identify and map multivendor xNFs using protocols like SNMP and CLI, with support for NETCONF.

Telecommunications Discovery Patterns provide a powerful, pattern-based approach to discover and manage telecom network resources directly from network elements. These patterns are especially valuable for discovering standalone xNFs \(such as routers and switches\) that are not managed through traditional EMS/NMS systems.

This capability enhances visibility across telecom infrastructures and ensures that both vendor-neutral and vendor-specific device data is captured and reflected in the CMDB and Telecom Network Inventory \(TNI\), following the TNI data model.

**Note:** Telecommunications Discovery Patterns are part of the TSOM Visibility subscription and are available as a customer-visible plugin from the ServiceNow Store.

## Key capabilities

-   Direct Network Element Discovery
    -   Use SNMP, CLI, and NETCONF to communicate directly with physical network elements.
    -   Discover physical network inventory such as interface cards, slots, ports, and devices without relying on EMS/NMS mediation.
-   Automated CI Mapping and CMDB Integration
    -   Discovered data is automatically mapped to telecom-aligned Configuration Item \(CI\) classes.
    -   Integrates directly with the Identification and Reconciliation Engine \(IRE\) to ensure accurate, non-duplicate CI records in the CMDB and Telecom Network Inventory \(TNI\).
-   CMDB Accuracy and Compliance
    -   Patterns trigger CMDB Compliance Certification Audits to detect mismatches or outdated records.
    -   Supports discrepancy identification and remediation, helping maintain data integrity.
-   Low-Code Pattern Customization: Extend or customize discovery patterns using low-code pattern designers to meet your specific network architecture and business needs.

## How it works

Telecommunications Discovery Patterns are executed through Horizontal Discovery using the Nebula Discovery Language \(NDL\). A pattern is a sequence of steps that:

1.  Establishes a connection to a target device.
2.  Executes commands using SNMP, CLI, or both.
3.  Extracts CI attributes and relationships.
4.  Sends results to IRE for reconciliation and insertion into the CMDB and TNI.

The discovery logic follows the TNI data model, which restructures complex CI relationships \(e.g., card-on-card scenarios\) to align with telecom modeling best practices. For example, If a child card is discovered inside a parent card, Telecom Discovery synthesizes a subslot to insert the child, avoiding an invalid card-on-card configuration.

## Architecture using Horizontal Discovery and Telecommunications Discovery Patterns

The following infographic is an example of the implementation for standalone SNMP or/and CLI xNFs.

## Horizontal Discovery Application

The Horizontal Discovery application in ServiceNow is a versatile and highly scalable discovery engine designed to operate effectively across network, IT, and cloud environments, collecting data across multiple layers to provide a holistic view of the infrastructure.

For more information, see Horizontal discovery process flow with patterns.

## Supported discovery patterns

A pattern is a sequence of commands designed to detect attributes of a configuration item \(CI\) and its outbound connections. Telecom Discovery provides a set of preconfigured Patterns that cover a wide range of network elements. ServiceNow offers several out-of-the-box \(OOB\) TSOM patterns, including:

-   Telecom Router Pattern – Generic SNMP-based router discovery.
-   Telecom Cisco 7613 Router Pattern – For Cisco 7613 routers using SNMP.
-   Telecom Juniper MX SSH Router Pattern – SNMP + CLI discovery of Juniper MX routers.
-   Telecom Cisco Switch Pattern – SNMP-based Cisco switch discovery.
-   Telecom Switch Pattern – SNMP-based generic switch discovery.

## TNI entity creation

If your instance has the **Telecom Network Inventory \(TNI\)** plugin installed:

-   Every discovered CI automatically results in a TNI entity record.
-   The IRE payload includes mapping to both `cmdb_ci` and `tni_entity` tables.

This ensures seamless alignment between operational and inventory systems, which is essential for order fulfillment, assurance, and network planning.

## MID Server

MID Server is a Java application that runs as a Windows service or UNIX daemon on a server within your local network. The ServiceNow® MID Server facilitates communication and data transfer between a ServiceNow instance and external applications, data sources, and services.

For more information, see MID Server.

## Identification &amp; Reconciliation Engine \(IRE\)

IRE offers a centralized framework for identifying and reconciling data from multiple sources. It verifies the integrity of the CMDB and some non-CMDB tables when various data sources are used to create or update CI records.

**Related topics**  


[Install Horizontal Discovery and set up Discovery Patterns](../task/install-horizontal-telecommunication-discoverypatterns.md)

