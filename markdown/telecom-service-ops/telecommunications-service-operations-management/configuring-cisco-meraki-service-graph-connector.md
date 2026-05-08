---
title: Configure Cisco Meraki Service Graph Connector
description: Configure the Cisco Meraki Service Graph Connector \(SGC\) to import physical and logical inventory data from the Cisco Meraki \(SGC\) into your Configuration Management Database \(CMDB\).
locale: en-US
release: australia
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: concept
last_updated: "2026-05-08"
reading_time_minutes: 2
breadcrumb: [Configure Telecom Visibility, Configure, Telecommunications Service Operations Management]
---

# Configure Cisco Meraki Service Graph Connector

Configure the Cisco Meraki Service Graph Connector \(SGC\) to import physical and logical inventory data from the Cisco Meraki \(SGC\) into your Configuration Management Database \(CMDB\).

## Authentication

You must authenticate before initiating discovery. During the authentication process, the discovery service receives an access token, which it then uses for bulk or specific discovery operations. The integration uses Cisco Meraki REST APIs to discover managed elements such as network equipment, interfaces, and services.

This integration uses REST APIs \(via a MID Server\) to promote the CMDB reflects accurate, up-to-date telecom inventory aligned with the TM Forum-based data model. For a list of API references, see [Cisco Meraki Service Graph Connector API Endpoints](../reference/cisco-meraki-service-graph-connector-api-endpoints.md).

**Note:** A valid Telecommunications Service Operations Management subscription is required to use this connector.

## Required plugins

|Plugin|Plugin ID|
|------|---------|
|Telecom Service Operations Core|sn\_tsom\_core|
|Service Graph Connector for Meraki Telco SD-WAN|sn\_tsom\_meraki\_connector|

**Note:** External requirements:

-   A running Cisco Meraki instance with access to its REST API.
-   A MID Server with secure connectivity to the Cisco Meraki instance.

## Configuration tasks overview

The following sections are available under the Cisco Meraki navigation pane. Use the following table for post-guided setup or to perform manual configurations.

|Section|Description|
|-------|-----------|
|Setup|Configure MID Server, define Cisco Meraki connections, and schedule imports.|
|Data Sources|Predefined data sources for bulk and filtered discovery \(SGC-Cisco Meraki Bulk Discovery, SGC-Cisco Meraki Filtering Discovery\). Enable parallel loading if needed. For more information on parallel loading.|
|Import Schedules|Manage scheduling for each Cisco Meraki connection alias. Run jobs manually or at defined intervals.|
|Connections &amp; Credential Aliases|Define aliases for each Cisco Meraki instance. Store connection metadata and credentials.|
|Connections|Define Cisco Meraki instance details, such as URL, selected MID Server, credential reference, and connection alias reference.|
|Credentials|Create Cisco Meraki credentials using Basic Auth.|
|Filters|Configure filtering parameters used in filtered discovery \(for example, by device IP or name\).|
|Properties|Modify system behavior using connector-specific properties. For more information, see.|

## Access the Guided Setup

Use the guided setup to simplify the configuration process. This setup provides an organized sequence of steps to help you complete integration quickly and correctly. For more information, see [Set up the Service Graph Connector for Cisco Meraki schedule](../task/set-up-cisco-meraki.md).

