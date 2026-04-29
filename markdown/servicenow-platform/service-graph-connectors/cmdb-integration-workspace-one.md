---
title: Service Graph Connector for VMware Workspace ONE UEM
description: Use the Service Graph Connector for VMware Workspace ONE UEM to pull data from VMware Workspace ONE Unified Endpoint Management \(UEM\) into your ServiceNow Instance.
locale: en-US
release: australia
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Service Graph Connector for VMware Workspace ONE UEM

Use the Service Graph Connector for VMware Workspace ONE UEM to pull data from VMware Workspace ONE Unified Endpoint Management \(UEM\) into your ServiceNow Instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

The integration imports different hardware assets into the ServiceNow® Configuration Management Database \(CMDB\) application.

## Supported versions

-   Supported versions:
    -   VMware Workspace ONE UEM version 25.6.961.16 \(2506\)
    -   Application Discovery Manager \(ADM\) API version 2
-   Supported ServiceNow versions:
    -   Yokohama
    -   Zurich
    -   Australia

## Use cases

The following are examples on how you can use the Service Graph Connector for different ServiceNow applications:

-   [IT Operations Management \(ITOM\) Visibility](https://www.servicenow.com/docs/access?context=itom-visibility-landing-page&version=australia&pubname=australia-it-operations-management&ft:locale=en-US)
    -   Detailed hardware and application inventory for Android, Apple, and Windows mobile devices. The inventory can be used with or without Software Asset Management \(SAM\).
    -   Compliance tracking for mobile devices. You can build your own device \(BYOD\) or use corporate-owned devices.
-   [IT Service Management \(ITSM\)](https://www.servicenow.com/docs/access?context=r_ITServiceManagement&version=australia&pubname=australia-it-service-management&ft:locale=en-US)
    -   Incident, problem, change on discovered configuration items \(CI\).
    -   Ownership tracking and assignment for mobile devices.

## Guided setup

The guided setup for the Service Graph Connector for VMware Workspace ONE UEM provides an organized sequence of tasks to configure the integration on your instance. To access the guided setup, see [Configure Service Graph Connector for VMware Workspace ONE UEM](../task/configure-workspace-one-integration.md).

## CMDB integrations dashboard

The Integration Commons for CMDB store app provides a dashboard with a central view of the status, processing results, and processing errors of all installed integrations. You can see metrics for all integration runs. You can filter the view to a specific CMDB integration, a specific time duration, or a specific integration run. For more details about monitoring Workspace ONE integrations in the CMDB Integrations Dashboard, see [Using the CMDB Integrations Dashboard](integration-commons-for-cmdb.md#section_fxg_lh4_blb).

## Data mapping

Data from the VMware Workspace ONE UEM Devices and Apps data sources is mapped and transformed into the ServiceNow CMDB Configuration Item \(CI\) class definitions using the Robust Transform Engine \(RTE\). Data is inserted into the ServiceNow CMDB using the Identification and Reconciliation Engine \(IRE\).

When you complete setting up the connection, you configure the integration to periodically pull data from VMware Workspace ONE UEM.

The data is loaded into the SG-Workspace ONE UEM Devices and Apps staging \[sn\_vmwoneuem\_integ\_devices\_and\_apps\] table.

The data is then inserted into the following target tables:

-   Computer \[cmdb\_ci\_computer\]
-   Handheld Computing Device \[cmdb\_ci\_handheld\_computing\]
-   Media Player \[cmdb\_ci\_media\_player\]
-   Network Adapter \[cmdb\_ci\_network\_adapter\]
-   Printer \[cmdb\_ci\_printer\]
-   SAM Software Installation \[cmdb\_sam\_sw\_install\], if com.snc.sams plugin is installed.
-   Serial Number \[cmdb\_serial\_number\]
-   Software Instance \[cmdb\_software\_instance\], if com.snc.sams plugin is not installed.
-   Software Package \[cmdb\_ci\_spkg\], if com.snc.sams plugin is not installed.

**Note:** To view any additional information such as the device owner, type of ownership, or compliance status, you need to switch to the SG-Workspace ONE UEM view. This view displays a **SG-Workspace ONE UEM Device Related** tab in the related list tabs with the additional information.

For more information on where data is saved when pulling data from VMware Workspace ONE Unified Endpoint Management \(UEM\), see [CMDB classes targeted in Service Graph Connector for VMware Workspace ONE UEM](../reference/cmdb-workspaceone-classes.md).

You can use the IntegrationHub ETL app to view the data maps. See [IntegrationHub ETL](integrationhub-etl.md) for more information.

**Related topics**  


[Service Graph Connectors](cmdb-sgc-available.md)

