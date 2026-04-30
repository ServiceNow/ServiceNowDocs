---
title: Service Graph Connector for Active Directory
description: The Service Graph Connector for Active Directory retrieves computer and software information from the Microsoft Active Directory \(AD\) product and imports it into the Configuration Management Database \(CMDB\) in your instance using Lightweight Directory Access Protocol \(LDAP\).
locale: en-US
release: zurich
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Service Graph Connector for Active Directory

The Service Graph Connector for Active Directory retrieves computer and software information from the Microsoft Active Directory \(AD\) product and imports it into the Configuration Management Database \(CMDB\) in your instance using Lightweight Directory Access Protocol \(LDAP\).

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Supported versions

-   Microsoft Active Directory version: Last tested on
-   Supported ServiceNow® versions:
    -   Utah
    -   Vancouver
    -   Washington

## Use cases

Import computer and software details about your assets from the Microsoft Active Directory product into your CMDB.

## Guided setup

The guided setup for the Service Graph Connector for Active Directory provides an organized sequence of tasks to configure the integration on your instance. To access the guided setup, [Configure Service Graph Connector for Active Directory](../task/sgc-ad-configure.md).

## CMDB integrations dashboard

The Integration Commons for CMDB store app provides a dashboard with a central view of the status, processing results, and processing errors of all installed integrations. You can see metrics for all integration runs. You can filter the view to a specific CMDB integration, a specific time duration, or a specific integration run. For more details about monitoring Microsoft Active Directory integrations in the CMDB Integrations Dashboard, see [Using the CMDB Integrations Dashboard](../../../configuration-management/concept/integration-commons-for-cmdb.md#section_fxg_lh4_blb).

## Data mapping

Data from the Service Graph Connector for Active Directory data sources is mapped and transformed into the ServiceNow CMDB Configuration Item \(CI\) class definitions using the Robust Transform Engine \(RTE\). Data is inserted into the ServiceNow CMDB using the Identification and Reconciliation Engine \(IRE\).

After you complete the guided setup, you configure the integration to periodically pull data from the Active Directory. The data is loaded into the following tables.

You can use the Integration Hub ETL application to view the data maps.

|Data source|Staging table|
|-----------|-------------|
|SGC Active Directory Import|SGC Active Directory Import \[sn\_sec\_sgc\_ad\_active\_directory\_import\]|
|Computer|Computer \[cmdb\_ci\_computer\]|
|Software|Software \[cmdb\_ci\_spkg\], \[cmdb\_software\_instance\], \[cmdb\_sam\_sw\_install\]|
|SGC Active Directory Computer|SGC Active Directory Computer \[sn\_sec\_sgc\_ad\_active\_directory\_computer\]|

