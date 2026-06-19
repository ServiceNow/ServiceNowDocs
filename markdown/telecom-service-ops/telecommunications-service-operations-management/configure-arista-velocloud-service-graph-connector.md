---
title: Configure Arista VeloCloud Service Graph Connector
description: Configure the Arista VeloCloud Service Graph Connector \(SGC\) to discover and import physical and logical inventory data from your Arista VeloCloud environment into the Configuration Management Database \(CMDB\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-service-ops/telecommunications-service-operations-management/configure-arista-velocloud-service-graph-connector.html
release: australia
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure Telecom Visibility, Configure, Telecommunications Service Operations Management]
---

# Configure Arista VeloCloud Service Graph Connector

Configure the Arista VeloCloud Service Graph Connector \(SGC\) to discover and import physical and logical inventory data from your Arista VeloCloud environment into the Configuration Management Database \(CMDB\).

Arista VeloCloud relies on VeloCloud Orchestrator \(VCO\) as its centralized management platform, available as either a self-hosted or SaaS deployment, to configure, monitor, and manage SD-WAN inventory across the network.

## Authentication

VeloCloud Orchestrator supports two types of user roles: MSP admins and organization admins. To authenticate API requests, users must generate an API token from their VCO account.

There are two types of API tokens:

-   User token: Inherits the same access permissions as the user who created it.
-   Organization token: Provides access scoped to a single organization.

You must authenticate before initiating discovery. During the authentication process, the discovery service receives an access token, which it then uses for bulk or specific discovery operations. The integration uses VeloCloud REST APIs to discover managed elements such as network equipment, interfaces, and services.

This integration uses REST APIs \(via a MID Server\) to ensure the CMDB reflects accurate, up-to-date telecom inventory aligned with the TM Forum-based data model. For a list of API references, see .

**Note:** A valid Telecommunications Service Operations Management subscription is required to use this connector.

## Required plugins

|Plugin|Plugin ID|
|------|---------|
|Telecom Service Operations Core|sn\_tsom\_core|
|Service Graph Connector for Velocloud Telco SD-WAN|sn\_tsom\_vcloud\_connector|

**Note:** External requirements:

-   A running Arista VeloCloud instance with access to its REST API.
-   A MID Server with secure connectivity to the Arista VeloCloud instance.

## Configuration tasks overview

The following sections are available under the Arista VeloCloud navigation pane. Use the following table for post-guided setup or to perform manual configurations.

|Section|Description|
|-------|-----------|
|Setup|Configure MID Server, define Arista VeloCloud connections, and schedule imports.|
|Data Sources|Predefined data sources for bulk and filtered discovery \(SGC-Arista VeloCloud Bulk Discovery, SGC-Arista VeloCloud Filtering Discovery\). Enable parallel loading if needed. For more information on parallel loading.|
|Import Schedules|Manage scheduling for each Arista VeloCloud connection alias. Run jobs manually or at defined intervals.|
|Connections &amp; Credential Aliases|Define aliases for each Arista VeloCloud instance. Store connection metadata and credentials.|
|Connections|Define Arista VeloCloud instance details, such as URL, selected MID Server, credential reference, and connection alias reference.|
|Credentials|Create Arista VeloCloud credentials using Basic Auth.|
|Filters|Configure filtering parameters used in filtered discovery \(for example, by device IP or name\).|
|Properties|Modify system behavior using connector-specific properties. For more information, see.|

## Access the Guided Setup

Use the guided setup to simplify the configuration process. This setup provides an organized sequence of steps to help you complete integration quickly and correctly. For more information, see [Set up the Service Graph Connector for Arista VeloCloud schedule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/set-up-the-service-graph-connector-for-arista-velocloud-schedule.md).

