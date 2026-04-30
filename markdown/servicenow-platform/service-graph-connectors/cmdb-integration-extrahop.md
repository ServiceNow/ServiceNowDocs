---
title: Service Graph Connector for ExtraHop
description: Use the Service Graph Connector for ExtraHop to pull data from the ExtraHop application into your ServiceNow instance.
locale: en-US
release: yokohama
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Service Graph Connector for ExtraHop

Use the Service Graph Connector for ExtraHop to pull data from the ExtraHop application into your ServiceNow instance.

**Important:** ServiceNow hosted Service Graph Connector for ExtraHop is now deprecated and no longer supported or available for new activation. ExtraHop hosted Service Graph Connector for ExtraHop provides the latest experience for this functionality. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

The Service Graph Connector for ExtraHop provides real-time network visibility across your enterprise by implementing stream processing, so that you can transform your network data into structured wire data.

The Service Graph Connector for ExtraHop pulls network visibility data into the ServiceNow® Configuration Management Database \(CMDB\) application. The connector enriches discovered device data and establishes relationships between devices based on network traffic flow.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## System requirements and supported versions

Dependencies and requirements:

-   MID Server that is installed on Linux or Windows, unless the ExtraHop appliance is publicly accessible.
-   ExtraHop Discover appliance with firmware version 7.2 or later with a user account that has unlimited privileges.

-   Supported versions: ExtraHop v7.9.
-   Supported ServiceNow versions:
    -   Tokyo
    -   Utah
    -   Vancouver
    -   Washington DC

## Use cases

The following are examples on how you can use the Service Graph Connector:

-   Identification of network interactions between CIs.
-   Discovery of network traffic flow data between computers or other types of hardware.
-   Creation of relationships between devices. The relationships are based on network traffic flow.

## Guided setup

The guided setup for the Service Graph Connector for ExtraHop provides an organized sequence of tasks to configure the integration on your instance. To access the guided setup, see [Configure Service Graph Connector for ExtraHop](../task/configure-extrahop-integration.md).

## CMDB Integrations Dashboard

The Integration Commons for CMDB store app provides a dashboard with a central view of the status, processing results, and processing errors of all installed Service Graph Connectors. You can see metrics for all integration runs. You can also filter the view to a specific CMDB integration, a specific time duration, or a specific integration run. For more details about monitoring ExtraHop integrations in the CMDB Integrations Dashboard, see [Using the CMDB Integrations Dashboard](integration-commons-for-cmdb.md#section_fxg_lh4_blb).

## Data mapping

Data from data sources in the ExtraHop application is mapped and transformed into the ServiceNow CMDB Configuration Item \(CI\) class definitions using the Robust Transform Engine \(RTE\). Data is inserted into the ServiceNow CMDB using the Identification and Reconciliation Engine \(IRE\).

When you complete setting up the connection, you can configure the integration to periodically pull data from the ExtraHop application. The data is loaded into the following staging tables:

-   ExtraHop Computer \[sn\_extrahop\_integr\_computer\]
-   ExtraHop Network Activity \[sn\_extrahop\_integr\_activity\]

The data is then inserted into the following target tables:

-   CI Relationship \[cmdb\_rel\_ci\]
-   Hardware \[cmdb\_ci\_hardware\]
-   IP Address \[cmdb\_ci\_ip\_address\]
-   Network Adapter \[cmdb\_ci\_network\_adapter\]

**Related topics**  


[Service Graph Connectors](cmdb-sgc-available.md)

