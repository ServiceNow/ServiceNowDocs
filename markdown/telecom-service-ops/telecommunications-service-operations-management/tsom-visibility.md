---
title: Telecom Visibility
description: Telecom Visibility extends the discovery and reconciliation capabilities of ITOM Visibility to meet the specific needs of telecom service providers. It enables accurate, telecom-aware network inventory by discovering real-time network data, reconciling mismatches, and maintaining a consistent telecom model in your CMDB and TNI \(Telecommunications Network Inventory\).
locale: en-US
release: australia
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Explore, Telecommunications Service Operations Management]
---

# Telecom Visibility

Telecom Visibility extends the discovery and reconciliation capabilities of ITOM Visibility to meet the specific needs of telecom service providers. It enables accurate, telecom-aware network inventory by discovering real-time network data, reconciling mismatches, and maintaining a consistent telecom model in your CMDB and TNI \(Telecommunications Network Inventory\).

Discover physical and logical network components across telecom domains, reconcile discrepancies between discovery and inventory data, and maintain a telecom-specific CMDB structure to support advanced automation and assurance use cases.

## Telecom Visibility overview

Telecom Visibility is a unified solution for discovering and managing telecom network resources. It leverages proven discovery technologies such as Horizontal Discovery, Telecommunications Discovery Patterns, and Service Graph Connectors \(SGC\) to bring network data from various systems \(for example, CLI/SNMP-based standalone devices or API-driven EMS/NMS/controllers\) into your CMDB.

Telecom Visibility helps communication service providers \(CSPs\) and telecom operators:

-   Discover and maintain telecom-specific network inventory
-   Reconcile mismatches between planned/design inventory and actual network state
-   Support Autonomous Network Operations \(ANO\), service fulfillment, and assurance workflows

## Key Capabilities

|Capability|Description|
|----------|-----------|
|Telecom Discovery with Patterns|Discover standalone network functions \(xNFs\) such as routers and switches using SNMP and CLI protocols via predefined Telecom Discovery Patterns.|
|Service Graph Connector Integration|Bring inventory and configuration data from external EMS/NMS/controllers into CMDB using northbound APIs.|
|Discrepancy Identification &amp; Reconciliation|Detect and resolve mismatches between inventoried and discovered data \(for example, missing CIs, model mismatches, stale entries\).|
|Telecom-Centric Data Modeling|Maintain structured and hierarchical telecom data including interface cards, slots, subslots, VLANs, and ports.|
|CMDB Integration|Use CMDB 360 and Discovery Admin Workspace to monitor discovery sources, attribute changes, and reconciliation outcomes.|

## Applications and Plugins

1.  Telecommunications Horizontal Discovery Patterns: Discovers telecom devices \(xNFs\) such as routers and switches using SNMP/CLI. Enables accurate inventory updates by scanning live network infrastructure. Supports vendor-specific patterns including:
    -   Cisco \(ASR1K, 7613, Nexus 9000, Nexus 3548\)
    -   Juniper \(MX80, MX104, MX240, MX460\)
2.  Service Graph Connectors \(SGC s\) for TSOM: Prebuilt integrations with EMS/NMS/controllers to import inventory data via APIs. Supports:
    -   Scheduled or on-demand discovery
    -   Multi-instance configurations
    -   Integration with systems like Nokia Altiplano \(GPON networks\)
3.  Telecom Visibility Plugin: Provides shared logic and foundational components for both discovery and discrepancy reconciliation. Ensures:
    -   Consistent behavior across TSOM workflows
    -   Reusable components for reconciliation and remediation
4.  CMDB CI Class Models for Telecom \(Required version: 1.82 or later\): Extends the CMDB to include telecom-specific classes and relationships, including:
    -   Interface cards
    -   Slots and subslots
    -   Network interfaces

## Telecom Visibility architecture

Telecom Visibility combines direct and indirect discovery methods:

-   Direct Discovery using SNMP/CLI \(for example, standalone routers/switches\)
-   Indirect Discovery using APIs from EMS/NMS/controllers \(for example, Nokia Altiplano\)

These feed into the CMDB and TNI, which then support decision-making, automation, and network operations. The following infographic demonstrates the architecture of Telecom Visibility.

## Use Cases

|Use Case|Outcome|
|--------|-------|
|Autonomous Network Operations|Reliable network inventory supports AI/ML-driven automation.|
|Service Fulfillment|Accurate CMDB/TNI ensures order accuracy and rapid provisioning.|
|Service Assurance|Reconciled inventory reduces troubleshooting time and increases uptime.|
|Audit &amp; Compliance|Discovery Admin Workspace and CMDB 360 support audit readiness and traceability.|

## Key personas

Telecom Visibility is used by:

-   Network and infrastructure teams: Discover and manage real-time network resource data across vendors and technologies.
-   Inventory and fulfillment teams: Maintain an accurate and complete CMDB/TNI to support service fulfillment, order management, and provisioning.
-   Platform administrators: Configure plugins, manage discovery sources, validate reconciliation rules, and monitor discovery performance.

## Monitoring tools

Discovery Admin Workspace - Central console to:

-   Monitor discovery tasks
-   Validate reconciliation processes
-   Tune schedules and view diagnostics

CMDB 360 - Visualize:

-   Attribute-level update history
-   Source attribution
-   Reconciliation rules in action

## Key benefits

|Feature|Benefit|
|-------|-------|
|CLI/SNMP Discovery|Expands network coverage without relying on external APIs.|
|Nokia Altiplano Integration|Supports GPON network discovery across multiple controller instances.|
|Discrepancy Reconciliation|Keeps inventory clean, actionable, and aligned with real network state.|

**Related topics**  


[Configure Telecom Visibility](../task/configuring-tsom-visibility.md)

[Discovery Admin Workspace](https://www.servicenow.com/docs/access?context=discovery-admin-workspace&version=australia&pubname=australia-it-operations-management&ft:locale=en-US)

