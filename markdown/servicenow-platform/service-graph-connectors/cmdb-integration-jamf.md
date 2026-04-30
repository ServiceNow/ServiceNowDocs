---
title: Service Graph Connector for Jamf
description: Use the Service Graph Connector for Jamf to pull data from Jamf into your ServiceNow instance.
locale: en-US
release: zurich
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Service Graph Connector for Jamf

Use the Service Graph Connector for Jamf to pull data from Jamf into your ServiceNow instance.

The Service Graph Connector for Jamf pulls data from computers, disks, networks, and software applications into the ServiceNow® Configuration Management Database \(CMDB\) application.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Supported versions

Supported ServiceNow versions:

-   Xanadu
-   Yokohama
-   Zurich

## Use cases

The following are examples on how you can use the Service Graph Connector for different ServiceNow® applications:

-   [IT Operations Management \(ITOM\) Visibility](https://www.servicenow.com/docs/access?context=itom-visibility-landing-page&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)
    -   Detailed hardware and software inventory tracking for macOS hardware and apps. The tracking can be done with or without Software Asset Management \(SAM\).
    -   Detailed hardware and software inventory tracking for hardware and apps for both iPhones and iPads. The tracking can be done with or without Software Asset Management \(SAM\).
    -   Compliance tracking for mobile devices and end-user computers.
    -   Duplicate data detection on imports to improve performance of nightly imports.
-   [Software Asset Management \(SAM\)](https://www.servicenow.com/docs/access?context=c_SoftwareAssetMgmt&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US) and [IT Asset Management \(ITAM\)](https://www.servicenow.com/docs/access?context=it-asset-management&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)
    -   Software package and installation tracking.
    -   License reclamation by detecting removed software.
    -   Software Usage tracking.
-   [IT Service Management \(ITSM\)](https://www.servicenow.com/docs/access?context=r_ITServiceManagement&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)
    -   Incidents, problems, and changes on discovered configuration items \(CI\).
    -   Automatic ownership assignment based on top users.

## Configuring a connection for the connector

You can configure a connection for the connector by using the SGC Central view in the Service Graph Workspace or CMDB Workspace. The view enables you to discover and install connectors, and then effectively manage the full life cycle of creating, editing, monitoring, and debugging connections. To configure the connector using SGC Central, see [Configure Service Graph Connector for Jamf using SGC Central](../../sgc-central/task/sgcc-configure-jamf-integration.md).

**Important:** Unless there are configuration issues, use the SGC Central view in the Service Graph Workspace or CMDB Workspace to configure the connection for the connector, as the guided setup method is planned for deprecated.

## CMDB integrations dashboard

The Integration Commons for CMDB store app provides a dashboard with a central view of the status, processing results, and processing errors of all installed integrations. You can see metrics for all integration runs. You can filter the view to a specific CMDB integration, a specific time duration, or a specific integration run. For more details about monitoring Jamf integrations in the CMDB Integrations Dashboard, see [Using the CMDB Integrations Dashboard](integration-commons-for-cmdb.md#section_fxg_lh4_blb).

## Data mapping

Data from the Jamf data source is mapped and transformed into the ServiceNow CMDB Configuration Item \(CI\) class definitions using the Robust Transform Engine \(RTE\). Data is inserted into the ServiceNow CMDB using the Identification and Reconciliation Engine \(IRE\).

When you complete setting up the connection, you can configure the integration to periodically pull data from Jamf.

The delta data synchronization feature is available in Jamf version 2.14 and higher. You can configure the **is\_delta\_enabled\_for\_computers** and **is\_delta\_enabled\_for\_mobiles** connection properties for synchronizing only delta data from a Jamf instance. See [Configuring data synchronization in Service Graph Connector for Jamf](sgc-cmdb-jamf-data-sync.md#).

The following data sources are included for the Jamf application:

-   **SG-Jamf Computers**

    Imports data from computers and loads the imported data in the SG-Jamf Computers \[sn\_jamf\_integrate\_sg\_jamf\_computers\] staging table.

-   **SG-Jamf Lookup Mac Software Bundle Ids**

    Imports data from software applications installed on macOS devices and loads the imported data in the SG-Jamf Lookup Mac Software Bundle Ids \[sn\_cmdb\_int\_util\_mac\_software\_bundleid\_lookup\] staging table.

    **Note:** To view the publisher information for applications installed on macOS devices, run the SG-Jamf Lookup Mac Software Bundle Ids data source before running the SG-Jamf Computers or SG-Jamf Mobile Devices data sources.

-   **SG-Jamf Mobile Devices**

    Imports data from mobile devices and loads the imported data in the SG-Jamf Mobile Devices \[sn\_jamf\_integrate\_sg\_jamf\_mobile\_devices\] staging table.

-   **SG-Jamf Remove Computers Software**

    Removes the imported computer software data that were later deleted from the source and updates the information in the SG-Jamf Remove Computers Software \[sn\_jamf\_integrate\_jamf\_remove\_software\] staging table.

-   **SG-Jamf Remove Mobile Software**

    Removes the imported mobile software data that were later deleted from the source and updates the information in the SG-Jamf Remove Mobile Software \[sn\_jamf\_integrate\_remove\_mobile\_software\] staging table.

-   **SG-Jamf Software Usage**

    Imports the software usage details from the Jamf environment to track which software data is being used infrequently, hasn't been used recently enough, or isn't being used at all and loads the imported data in the SG-Jamf Software Usage \[sn\_jamf\_integrate\_jamf\_software\_usage\] staging table. Based on the software usage information, you can add a reclamation rule to aggregate usage records and to identify unused software devices. See [Software reclamation rules](https://www.servicenow.com/docs/access?context=sw-reclamation-rules&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US).

    **Note:** The SG-Jamf Software Usage data source is available only when the Software Asset Management Professional plugin \(com.snc.samp\) is activated on your ServiceNow instance. See [Request Software Asset Management](https://www.servicenow.com/docs/access?context=t_RequSoftwareAssetMgmt&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US).


The imported data is then inserted into the following target tables:

-   CI Relationship \[cmdb\_rel\_ci\]
-   Computer \[cmdb\_ci\_computer\]
-   Disk \[cmdb\_ci\_disk\]
-   Handheld Computing device \[cmdb\_ci\_handheld\_computing\]
-   IP Address \[cmdb\_ci\_ip\_address\]
-   Network Adapter \[cmdb\_ci\_network\_adapter\]
-   Printer \[cmdb\_ci\_printer\]
-   Serial Number \[cmdb\_serial\_number\]
-   Software Installation \[cmdb\_sam\_sw\_install\] \(If the SAM application is installed.\)
-   Software Instance \[cmdb\_software\_instance\] \(If the SAM application is not installed.\)
-   Software \[cmdb\_ci\_spkg\] \(If the SAM application is not installed.\)
-   Software Usage \[samp\_sw\_usage\]

**Note:** For the Computer \[cmdb\_ci\_computer\] and Handheld Computing device \[cmdb\_ci\_handheld\_computing\] data sources, if you created multiple Jamf instances and want to know where the CIs originated from, you can identify the origins from the **Key** and **Value** columns. Additionally, you can view the Jamf Extension Attributes \[sn\_jamf\_integrate\_extension\_attribute\] and Most recent discovery \[last\_discovered\] fields in both data sources. If you want to configure multiple instances, follow the steps in [Configure Service Graph Connector for Jamf using the guided setup](../task/configure-jamf-integration.md) in step 4.

For more information on where data is saved when pulling data from a Jamf application, see [CMDB classes targeted in Service Graph Connector for Jamf](../reference/cmdb-jamf-classes.md).

You can use the IntegrationHub ETL app to view the data maps. See [IntegrationHub ETL](integrationhub-etl.md) for more information.

**Related topics**  


[Service Graph Connectors](cmdb-sgc-available.md)

