---
title: Telecom Discovery via Nokia Altiplano
description: The Service Graph Connector for Nokia Altiplano offers a telecom-aware integration that brings real-time network inventory from the Nokia Altiplano Access Network SDN Controller into your ServiceNow CMDB.
locale: en-US
release: australia
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Indirect Discovery with SGCs, Telecom Discovery, Explore, Telecommunications Service Operations Management]
---

# Telecom Discovery via Nokia Altiplano

The Service Graph Connector for Nokia Altiplano offers a telecom-aware integration that brings real-time network inventory from the Nokia Altiplano Access Network SDN Controller into your ServiceNow CMDB.

Designed for service providers and telecom enterprises, this connector enables complete visibility, control, and synchronization of your physical and logical network infrastructure. This integration uses REST APIs and a MID Server to deliver a telecom-model-aligned view of your network, enabling more accurate service modeling, inventory management, and operational efficiency.

## Key benefits

-   Accurate inventory synchronization: Automatically populate the CMDB with up-to-date physical and logical inventory from Nokia Altiplano using secure, REST API-based ingestion. This includes OLTs, ONUs/ONTs, interface cards, ports, slots, and logical connections.
-   Telecom-Aware CI modeling: Model your network infrastructure in a telecom-aligned format using purpose-built CI classes and relationships. The connector ensures the accurate representation of devices and their dependencies—mirroring your actual network topology.
-   Simplified and Guided Setup: Reduce time-to-value with a built-in guided setup that walks you through connection configuration, data source management, and import scheduling with ease.
-   Flexible discovery options: Choose how and when to run discovery based on your needs—whether it’s full bulk loads, targeted filtered discovery, or phased OLT-only imports. Apply custom filters by device IP or name.
-   Multi-Instance support: Scale effortlessly by onboarding multiple Altiplano instances independently. Configure connection aliases and define import schedules per instance for complete operational flexibility.

**Note:** Supported Nokia Altiplano Controller minimum version is 24.6. For a general overview of Service Graph Connector technology, see [Getting started with Service Graph Connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/cmdb-sgc-intro.md).

## Nokia Altiplano SGC Architecture

The following infographic helps you understand the architecture of Nokia Altiplano service graph connector.

## Use cases

The following are examples on how you can use the Nokia Altiplano Service Graph Connector:

-   Automatically ingest and structure network data into ServiceNow’s CMDB for both physical and logical network elements: This creates a telecom-model-aligned CMDB view that mirrors your live network environment.
    -   Physical Components: OLTs, ONUs/ONTs, slots, subslots, cards, and ports
    -   Logical Components: Logical ports, VLANs, Link Aggregation Groups \(LAGs\), and logical paths between devices
-   Maintain the integrity of your network data with scheduled, automated reconciliation that:
    -   Detects and responds to real-time changes
    -   Prevents data drift or stale records
    -   Supports operational processes like service assurance, order fulfillment, and network planning
-   Discover beyond physical infrastructure by capturing and managing logical connectivity within ServiceNow:
    -   Identify and model logical ports, LAGs, and logical paths like PON and VLAN connections
    -   Link logical CIs with physical components using parent-child and member-of relationships
    -   Enhance diagnostics, impact analysis, and service modeling by visualizing end-to-end logical topologies
-   Leverage ServiceNow’s built-in Extract, Transform, Load \(ETL\) framework to simplify and accelerate integration:
    -   Predefined transformation maps and CI class definitions reduce development overhead
    -   Reuse existing CMDB structures to minimize customization
    -   Rapidly onboard new Altiplano instances and scale across your network infrastructure

## Key capabilities and components

|Capability|Description|Supporting component|
|----------|-----------|--------------------|
|Telecom-aware CMDB modeling|Maps Altiplano physical and logical inventory \(OLT, ONU/ONT, ports, slots, cards, interfaces\) into CMDB with telecom-specific CI classes and relationships.|RTE, IRE, CMDB tables \(`cmdb_ci_optical_line_terminal`, `cmdb_ci_optical_network_terminal`, etc.\)|
|Automated data ingestion|Retrieves device inventory from Nokia Altiplano via REST APIs with secure, scheduled imports.|MID Server, Data Sources \(SGC-Nokia Altiplano Bulk/Filtered Discovery\)|
|Custom discovery control|Choose OLT-only or include ONU data, apply filters by IP or name, schedule jobs per instance.|Import Schedules, System Properties \(`sn_sgc_altiplano.enable_onu_discovery`, etc.\)|
|Multi-instance support|Configure and manage discovery independently for multiple Altiplano controllers.|Connection Aliases, Credential Aliases|
|Parallel data processing|Improve performance by running concurrent data-source jobs for large datasets.|System Property: `sn_sgc_altiplano.parallel_number_of_data_source_jobs`, Enable Parallel Loading|
|Guided configuration|Simplifies setup with step-by-step interface for creating connections, credentials, and jobs.|Guided Setup UI \(Navigation: All &gt; Service Graph Connectors &gt; Nokia Altiplano &gt; Setup\)|
|Model-driven CI classification|Matches discovered devices to models and assigns correct CI class \(OLT, ONU, ONT\), or falls back to Network Gear.|Model Tables, System Property: `sn_sgc_altiplano.onu_ci_class`|
|Relationship|Establishes telecom-specific CI relationships \(e.g., member-of, contains, logical path\).|IRE, Logical Connections CI \(`cmdb_ci_ni_logical_path`\)|
|Dashboards and monitoring|View status, results, and errors of each run; filter by connector or timeframe.|Integration Commons for CMDB Dashboard|
|Scalable and reusable architecture|Decoupled data sources, transformation, and CI reconciliation for easy scaling and customization.|Import Sets \(`sn_sgc_altiplano_tsom_inventory`\), Transformation Maps, System Properties|

## CMDB Integrations Dashboard

The Integration Commons for CMDB store app provides a dashboard with a central view of the status, processing results, and processing errors of all installed Service Graph Connectors. You can see metrics for all integration runs. You can filter the view to a specific integration, a specific time duration, or a specific integration run. For more details about monitoring integrations in the CMDB Integrations Dashboard, see [Integration Commons for CMDB](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/cmdb-integration-commons/integration-commons-for-cmdb.md).

**Related topics**  


[Configure Nokia Altiplano service graph connector](configuring-service-graph-connector-nokia-altiplano.md)

[System components installed with Nokia Altiplano](../reference/properties-installed-with-nokia-altiplano.md)

