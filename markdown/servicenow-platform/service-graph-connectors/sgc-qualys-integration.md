---
title: Service Graph Connector for Qualys
description: The Service Graph Connector for Qualys pulls in asset inventory data \(hardware and software\) from the Qualys database into the Configuration Management Database \(CMDB\) application in your ServiceNow AI Platform instance.
locale: en-US
release: australia
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Service Graph Connector for Qualys

The Service Graph Connector for Qualys pulls in asset inventory data \(hardware and software\) from the Qualys database into the Configuration Management Database \(CMDB\) application in your ServiceNow AI Platform® instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Supported versions

Use this data to manage your Qualys resources directly from your ServiceNow AI Platform® instance.

Supported Qualys APIs:

-   Qualys Global Asset API v2. You might prefer to use this API if you are importing data for the Security Posture Control Security Posture Control application.
-   Qualys Asset Management API v2. This API is deactivated by default. You should only activate this API if you don't have access to the Qualys Cybersecurity Asset Management \(CSAM\) product. ServiceNow uses a different API \(Asset management and tagging\) for this API but the data returned is not comprehensive.

Supported ServiceNow® versions:

-   Utah
-   Vancouver
-   Washington

## Use cases

The following are examples on how you can use the Service Graph Connector for Qualys for different ServiceNow applications:

-   Complements the Qualys Asset Discovery.
-   Import data with the Global Asset API or the Asset Management API.
-   Multi-instance support.

## Guided Setup

The guided setup for the Service Graph Connector for Qualys provides you with an organized sequence of tasks to configure the integration on your instance. For instructions, see [Configure the Service Graph Connector for Qualys](../task/sgc-qualys-configure.md).

## CMDB integrations dashboard

The Integration Commons for CMDB store app provides a dashboard with a central view of the status, processing results, and processing errors of all installed integrations. You can see metrics for all integration runs. You can filter the view to a specific CMDB integration, a specific time duration, or a specific integration run. For more details about monitoring Qualys integrations in the CMDB Integrations Dashboard, see [Using the CMDB Integrations Dashboard](../../../configuration-management/concept/integration-commons-for-cmdb.md#section_fxg_lh4_blb).

## Hardware CI Rules

The hardware Configuration item \(CI\) mapping rule table is equipped with hardware category1, hardware category2 and corresponding target CI class. Following a Qualys API call, the system checks the hardware category1 and hardware category2 to determine their satisfaction, if hardware category1 and hardware category2 is match with the table record then the associated target CI class is added to the import set table data. During the mapping process, this designated target CI class is then used.

## Computer CI Rules

The Computer CI Mapping Rule table is equipped with predefined rules, including criteria such as OS name, OS category, OS category 2, OS Publisher, OS Product name, and the corresponding target CI class. Following a Qualys API call, the system checks these rules to determine their satisfaction. If a rule is met, the associated target CI class is added to the import set table data. During the mapping process, this designated target CI class is then used.

If you want to update CI attributes, you must create new reconciliation rules to determine which discovery sources can update CI attributes. See 'Reconciliation rules' in the online product documentation and the Identification and Reconciliation Fundamentals article in the ServiceNow Support Knowledge base for more information.

## Asset Management CI Rules

The Asset Management CI Mapping Rule table is equipped with predefined rules, including criteria such as Operating System, Is Volume Info Present, Is processor Present, Cloud Provider and the corresponding target CI class. Following a Qualys API call, the system checks these rules to determine their satisfaction. If a rule is met, the associated target CI class is added to the import set table data. During the mapping process, this designated target CI class is then used.

