---
title: Service Graph Connector Integration for Claroty CTD
description: Integrate Claroty Continuous Threat Detection \(CTD\) with the ServiceNow Operational Technology Manager application to import detected devices and Claroty CTD sites \(sensor or Network Intrusion Detection System appliances\).
locale: en-US
release: yokohama
product: Operational Technology Manager
classification: operational-technology-manager
topic_type: concept
last_updated: "2025-04-18"
reading_time_minutes: 4
breadcrumb: [Integrate, Operational Technology Manager, Operational Technology]
---

# Service Graph Connector Integration for Claroty CTD

Integrate Claroty Continuous Threat Detection \(CTD\) with the ServiceNow Operational Technology Manager application to import detected devices and Claroty CTD sites \(sensor or Network Intrusion Detection System appliances\).

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Supported versions

Claroty CTD Version:

-   4.4.3 or later
-   5.1

## Use cases

Use the Service Graph Connector Integration for Claroty Continuous Threat Detection with the Operational Technology Manager application to import the following information to the Configuration Management Database \(CMDB\)

-   Sites
-   Devices detected by each site
-   Connections \(or baselines\)
-   Installed programs

The following figure shows the detection method for importing Claroty CTD data into the CMDB.

![Process for importing Claroty CTD data into the ServiceNow Configuration Management Database (CMDB).](../image/claroty-emc-process.png)

## Guided setup

The guided setup for the Service Graph Connector Integration for Claroty CTD provides an organized sequence of tasks to configure the integration on your instance. To access the guided setup, see [Configure guided setup](../task/configuring-sgc-claroty-ctd-guided-setup.md).

## CMDB integrations dashboard

The Integration Commons for CMDB store app provides a dashboard with a central view of the status, processing results, and processing errors of all installed integrations. You can see metrics for all integration runs. You can filter the view to a specific CMDB integration, a specific time duration, or a specific integration run. For more details about monitoring integrations in the CMDB Integrations Dashboard, see [Integration Commons for CMDB](https://www.servicenow.com/docs/access?context=integration-commons-for-cmdb&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US#section_fxg_lh4_blb).

## Data mapping

Data from the Claroty CTD data sources is mapped and transformed into the ServiceNow CMDB Configuration Item \(CI\) class definitions using the Robust Transform Engine \(RTE\). Data is inserted into the ServiceNow CMDB using the Identification and Reconciliation Engine \(IRE\).

The following table lists the data sources included for the Service Graph Connector Integration for Claroty CTD and the corresponding staging tables where the imported data is loaded.

|Data source|Staging table|
|-----------|-------------|
|SG-OT Claroty CTD Devices|SG-OT Claroty CTD Devices Import \[sn\_clarotyctdsgc\_sg\_ot\_claroty\_ctd\_devices\_import\]|
|SG-OT Claroty CTD Baselines|SG-OT Claroty CTD Baselines Import \[sn\_clarotyctdsgc\_sg\_ot\_claroty\_ctd\_baselines\_import\]|
|SG-OT Claroty CTD Programs|SG-OT Claroty CTD Programs Import \[sn\_clarotyctdsgc\_sg\_ot\_claroty\_ctd\_programs\_import\]|
|SG-OT Claroty CTD Sites|SG-OT Claroty CTD Sites Import \[sn\_clarotyctdsgc\_sg\_ot\_claroty\_ctd\_sites\_import\]|

The imported data from the staging tables is then inserted into the following target tables:

-   Computer \[cmdb\_ci\_computer\]
-   Hardware \[cmdb\_ci\_hardware\]
-   IP Address \[cmdb\_ci\_ip\_address\]
-   Network Adapter \[cmdb\_ci\_network\_adapter\]
-   OT Device Details \[cmdb\_ot\_entity\]
-   OT Control Module \[cmdb\_ci\_ot\_control\_module\]
-   OT Control System \[cmdb\_ci\_ot\_control\]
-   Serial Number \[cmdb\_serial\_number\]

For more information, see [CMDB classes targeted](../reference/sgc-claroty-ctd-classes.md).

## Default query parameters for the Service Graph Connector Integration for Claroty CTD

By default, the Service Graph Connector Integration for Claroty CTD is shipped with query parameter filters. You can modify their values based on ServiceNow entitlements that you have with the IntegrationHub Enterprise package.

When you begin importing the data from the Claroty CTD, the Service Graph Connector Integration for Claroty CTD uses the default query parameter filters that are listed in the following table.

|Query parameter filter|Value|Description|
|----------------------|-----|-----------|
|approved\_exact|true|Unapproved devices on the Claroty CTD aren’t imported because the value of approved\_exact is set to true.|
|valid\_exact|true|Invalid devices on the Claroty CTD aren’t imported because the value of valid\_exact is set to true.|
|special\_hint\_exact|0|Address types that aren’t set to 0 \(unicast\) on the Claroty CTD aren’t imported.|
|ghost\_exact|false|If there’s an device on the Claroty CTD that is classified as a ghost, the Service Graph Connector Integration for Claroty CTD doesn’t import it because the default value is set to false.|

-   **[Configure the Service Graph Connector Integration for Claroty CTD](../task/configuring-sgc-claroty-ctd-guided-setup.md)**  
Use the guided setup for Service Graph Connector Integration for Claroty CTD to lead you through the integration steps.
-   **[Validate NIDS sensors](../task/validate-nids-appliances-sgc-claroty.md)**  
Validate the Network IDS \(NIDS\) sensors once they're imported to prepare for device import. The sensors can only pass the validation if they aren't in learning mode as such sensors aren't eligible for device import.
-   **[Accessing the connection details of the Service Graph Connector Integration for Claroty CTD](sgc-cmdb-claroty-ctd-conn.md#)**  
You can access the connection details of the Service Graph Connector Integration for Claroty CTD in a single view using the common connection framework \(CCF\) included within the Integration Commons for CMDB \(sn\_cmdb\_int\_util\) store app.
-   **[CMDB classes targeted in the Service Graph Connector Integration for Claroty CTD](../reference/sgc-claroty-ctd-classes.md)**  
When you complete the setup tasks, you can configure the integration periodically to pull data from Claroty CTD. The data is saved in tables that extend from the Configuration item \[cmdb\_ci\] table.

**Parent Topic:**[Operational Technology Manager Integrations](otm_integrations.md)

