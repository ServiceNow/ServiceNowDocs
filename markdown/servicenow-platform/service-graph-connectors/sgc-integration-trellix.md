---
title: Service Graph Connector for Trellix
description: Use the Service Graph Connector for Trellix to bring in device, server, and network data from a Trellix environment into your ServiceNow instance to streamline your incident response and asset management use cases.
locale: en-US
release: australia
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Service Graph Connector for Trellix

Use the Service Graph Connector for Trellix to bring in device, server, and network data from a Trellix environment into your ServiceNow instance to streamline your incident response and asset management use cases.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Supported versions

Supported ServiceNow versions:

-   Washington DC
-   Xanadu
-   Yokohama

## Use cases

The following examples describe how you can use the Service Graph Connector for Trellix for security operations management:

-   Identify cybersecurity risks in the environment.
-   Assess dependencies between configuration items \(CI\).
-   Enable effective security incident response and endpoint management systems.
-   Identify data quality issues, reconcile inconsistencies, and manage incidents and changes on discovered CIs.

## Configuring a connection for the connector

Use the SGC Central view in the Service Graph Workspace or CMDB Workspace to install the connector and configure the connection. The view enables you to install and discover connectors and to manage the full life cycle of creating, editing, monitoring, and debugging connections. For instructions, see [Configure Service Graph Connector for Trellix using SGC Central](../../sgc-central/task/sgcc-configure-trellix-integ.md).

**Important:** Unless there are configuration issues, use SGC Central to configure the connection. The guided setup method for configuration is being deprecated.

## CMDB integrations dashboard

The Integration Commons for CMDB store app provides a dashboard with a central view of the status, processing results, and processing errors of all installed integrations. You can see metrics for all integration runs. You can filter the view to a specific CMDB integration, a specific time duration, or a specific integration run. For more details about monitoring Trellix integrations in the CMDB Integrations Dashboard, see [Using the CMDB Integrations Dashboard](integration-commons-for-cmdb.md#section_fxg_lh4_blb).

## Data mapping

Data from the Trellix data sources is mapped and transformed into the ServiceNow CMDB Configuration Item \(CI\) class definitions using the Robust Transform Engine \(RTE\). Data is inserted into the ServiceNow CMDB using the Identification and Reconciliation Engine \(IRE\).

The following data source is included for the Trellix application:

-   **SG-Trellix-Devices**

    Imports data from devices and loads the imported data in the SGC Trellix Device Import \[sn\_trellix\_integ\_sgc\_trellix\_device\_import\] staging table.


The imported data is then inserted into the following target tables:

-   [File System](../reference/cmdb-trellix-classes.md#section_utl_zrr_mfc) \[cmdb\_ci\_file\_system\]
-   [IP Address](../reference/cmdb-trellix-classes.md#section_kpf_1sr_mfc) \[cmdb\_ci\_ip\_address\]
-   [Network Adapter](../reference/cmdb-trellix-classes.md#section_mgv_1sr_mfc) \[cmdb\_ci\_network\_adapter\]
-   [Server](../reference/cmdb-trellix-classes.md#section_wpn_bsr_mfc) \[cmdb\_ci\_server\]
-   [Software Installation](../reference/cmdb-trellix-classes.md#section_ahx_4ds_mfc) \[cmdb\_sam\_sw\_install\] \(if the Software Asset Management \(SAM\) application is installed\)
-   [Software](../reference/cmdb-trellix-classes.md#section_uqb_dsr_mfc) \[cmdb\_ci\_spkg\] \(if the SAM application isn't installed\)
-   [Software Instance](../reference/cmdb-trellix-classes.md#section_xfs_dsr_mfc) \[cmdb\_software\_instance\] \(if the SAM application isn't installed\)
-   [Storage Disk](../reference/cmdb-trellix-classes.md#section_thj_2sr_mfc) \[cmdb\_ci\_storage\_disk\]

You can use the IntegrationHub ETL app to view the data maps. See [IntegrationHub ETL](integrationhub-etl.md) for more information.

## System property

The following system property is available for Service Graph Connector for Trellix: `sn_trellix_integ.getdevices_count`. This property sets the pagination size for the records that are fetched from the Trellix API.

-   Type: integer
-   Default value: `100`

**Note:** To open the System Properties \[sys\_properties\] table, enter `sys_properties.list` in the navigation filter.

**Related topics**  


[Service Graph Connectors](cmdb-sgc-available.md)

[Configure Service Graph Connector for Trellix using SGC Central](../../sgc-central/task/sgcc-configure-trellix-integ.md)

[Configure Service Graph Connector for Trellix using guided setup](../task/sgc-config-trellix-integration.md)

[CMDB classes targeted in Service Graph Connector for Trellix](../reference/cmdb-trellix-classes.md)

