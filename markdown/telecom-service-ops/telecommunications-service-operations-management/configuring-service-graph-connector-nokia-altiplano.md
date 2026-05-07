---
title: Configure Nokia Altiplano service graph connector
description: Configure the Nokia Altiplano service graph connector to import physical and logical inventory data from the Nokia Altiplano Access Network SDN Controller into your ServiceNow Configuration Management Database \(CMDB\).
locale: en-US
release: australia
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure Telecom Visibility, Configure, Telecommunications Service Operations Management]
---

# Configure Nokia Altiplano service graph connector

Configure the Nokia Altiplano service graph connector to import physical and logical inventory data from the Nokia Altiplano Access Network SDN Controller into your ServiceNow Configuration Management Database \(CMDB\).

This integration uses REST APIs \(via a MID Server\) to ensure the CMDB reflects accurate, up-to-date telecom inventory aligned with the TM Forum-based data model.

**Note:** A valid Telecommunications Service Operations Management subscription is required to use this connector.

## Required plugins

|Plugin|ID|
|------|---|
|Telecom Service Operations Core|`sn_tsom_core`|
|Service Graph Connector for Nokia Aliplano|sn\_tsom\_altiplano\_connector|

**Note:** External requirements:

-   A running Nokia Altiplano Controller instance with access to its REST northbound API.
-   A MID Server with secure connectivity to the Altiplano instance.

## Configuration tasks overview

The following sections are available under the Nokia Altiplano navigation pane. Use the following table for post-guided setup or to perform manual configurations.

|Section|Description|
|-------|-----------|
|Setup|Configure MID Server, define Altiplano connections, and schedule imports.|
|Data Sources|Predefined data sources for bulk and filtered discovery \(SGC-Nokia Altiplano Bulk Discovery, SGC-Nokia Altiplano Filtering Discovery\). Enable parallel loading if needed. For more information on parallel loading, see [Configure concurrent import and parallel loading for Nokia Altiplano](../task/configure-concurrent-import-and-parallel-loading.md).|
|Import Schedules|Manage scheduling for each Altiplano connection alias. Run jobs manually or at defined intervals.|
|Connections &amp; Credential Aliases|Define aliases for each Altiplano instance. Store connection metadata and credentials.|
|Connections|Define Altiplano instance details, such as URL, selected MID Server, credential reference, and connection alias reference.|
|Credentials|Create Altiplano credentials using Basic Auth.|
|Filters|Configure filtering parameters used in filtered discovery \(for example, by device IP or name\).|
|Properties|Modify system behavior using connector-specific properties. For more information, see [System components installed with Nokia Altiplano](../reference/properties-installed-with-nokia-altiplano.md).|

## Supported Nokia Altiplano versions

-   Minimum supported version: 24.6
-   Supported OLT: Lightspan MF-2

**Note:** Fore more information, see [Mapping Nokia Altiplano CIs and Relationships in CMDB](data-mapping.md).

## Access the Guided Setup

Use the guided setup to simplify the configuration process. This setup provides an organized sequence of steps to help you complete integration quickly and correctly. To access the guided setup:

1.  Navigate to **All** &gt; **Service Graph Connectors** &gt; **Nokia Altiplano** &gt; **Setup**.
2.  Follow the task sequence to configure MID Server settings, Nokia Altiplano connections, filters, and import schedules. For more information, see [Set up Nokia Altiplano](../task/initial-setup-procedure.md).

**Related topics**  


[Set up Nokia Altiplano](../task/initial-setup-procedure.md)

[Set up multiple Nokia Altiplano instances](../task/multi-instance-setup.md)

[Configure concurrent import and parallel loading for Nokia Altiplano](../task/configure-concurrent-import-and-parallel-loading.md)

[Mapping Nokia Altiplano CIs and Relationships in CMDB](data-mapping.md)

[Run and verify import for Nokia Altiplano Service Graph Connector](../task/run-and-verify-import-for-nokia-altiplano-service-graph-connector.md)

[System components installed with Nokia Altiplano](../reference/properties-installed-with-nokia-altiplano.md)

[Telecom Discovery via Nokia Altiplano](service-graph-connector-for-nokia-altiplano.md#)

