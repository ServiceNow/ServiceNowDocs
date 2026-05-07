---
title: Configure a Fortinet SD-WAN Service Graph Connector
description: Configuring the Fortinet SD-WAN Service Graph Connector \(SGC\) enables you to import physical inventory data from FortiManager into the Configuration Management Database \(CMDB\) of your ServiceNow instance.
locale: en-US
release: australia
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: concept
last_updated: "2026-05-06"
reading_time_minutes: 2
breadcrumb: [Configure Telecom Visibility, Configure, Telecommunications Service Operations Management]
---

# Configure a Fortinet SD-WAN Service Graph Connector

Configuring the Fortinet SD-WAN Service Graph Connector \(SGC\) enables you to import physical inventory data from FortiManager into the Configuration Management Database \(CMDB\) of your ServiceNow instance.

FortiManager is the Fortinet centralized management platform that enables you to configure, monitor, and manage multiple Fortinet security devices, including firewalls and SD-WAN appliances, from a single interface.

The FortiManager JSON API is used to perform configuration and monitoring tasks on a FortiManager device. The SGC for Fortinet SD-WAN uses JSON to gather information and populate the CMDB.

By using structured JSON requests over HTTPS, you can efficiently interact with FortiManager to streamline operations and scale network management tasks across multiple Fortinet devices. These APIs enable automated tasks within the Fortinet ecosystem, such as bulk configuration changes, device management, status monitoring, and inventory collection. To access the Fortinet APIs, create a user and key credentials from FortiManager. For API reference examples, see [Fortinet Service Graph Connector API Endpoints](../reference/fortinet-service-graph-connector-api-endpoints.md).

**Note:** A valid Telecommunications Service Operations Management subscription is required to use this connector.

## Required plugins

|Plugin|Plugin ID|
|------|---------|
|Telecom Service Operations Core|sn\_tsom\_core|
|Service Graph Connector for Fortinet|sn\_tsom\_fortinet\_connector|

**Note:** External requirements:

-   A running FortiManager instance with access to its JSON-RPC based northbound API.
-   A configured API key in the FortiPortal to enable access to JSON-RPC requests.
-   A MID Server with secure connectivity to the FortiManager instance.

## Configuration tasks overview

The following sections are available under the Fortinet navigation pane. Use the following table for post-guided setup or to perform manual configurations.

|Section|Description|
|-------|-----------|
|Setup|Configure the MID Server, define Fortinet connections, and schedule imports.|
|Data Sources|Predefined data sources for bulk \(SGC-Fortinet Bulk Discovery\) and filtered discovery \(SGC-Fortinet Filtering Discovery\).|
|Import Schedules|Manage scheduling for each Fortinet connection alias. Run jobs manually or at defined intervals.|
|Connections &amp; Credential Aliases|Define aliases for each Fortinet instance. Store connection metadata and credentials.|
|Connections|Define Fortinet instance details, such as the URL, the selected MID Server, credential reference, and connection alias reference.|
|Credentials|Create Fortinet credentials using API Key Credentials.|
|Filters|Configure filtering parameters used in discovery filtered by device IP or name.|
|Properties|Modify system behavior using connector-specific properties.|

## Access the Guided Setup

Use the guided setup to simplify the configuration process. This setup provides an organized sequence of steps to help you complete integration quickly and correctly. For more information, see [Set up the Service Graph Connector for Fortinet schedule](../task/set-up-fortinet-sd-wan.md).

