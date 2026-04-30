---
title: Service Graph Connector for Splunk
description: The Service Graph Connector for Splunk pulls in asset inventory data \(hardware and software\) from the Splunk database into the Configuration Management Database \(CMDB\) application in your ServiceNow AI Platform instance.
locale: en-US
release: xanadu
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Service Graph Connector for Splunk

The Service Graph Connector for Splunk pulls in asset inventory data \(hardware and software\) from the Splunk database into the Configuration Management Database \(CMDB\) application in your ServiceNow AI Platform® instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Supported versions

Supported versions:

-   Xanadu
-   Washingtondc
-   Vancouver

## Use cases

By default, the Service Graph Connector for Splunk pulls the following basic forwarding details:

-   Forwarder's version
-   Forwarder's type
-   Forwarder's last check-in time
-   OS
-   Host
-   Host IP address

With the [Service Graph Connector for Splunk add-on](sgc-splunk-add-on.md), you have the option to import extended data for your Windows and Linux assets with the Service Graph Connector for Splunk that includes the following details:

-   MAC address
-   Operating system details
-   Asset name
-   Software details
-   File system
-   Last logon date
-   Open ports

This data is stored in the Configuration Management Database \(CMDB\) and Splunk Asset Details extension attributes custom tables.​ To import these extended asset details, the add-on is required. See [Install the add-on for the Service Graph Connector for Splunk](../task/spc-install-splunk-add-on.md).

## Guided setup

The guided setup for the Service Graph Connector for Splunk provides an organized sequence of tasks to configure the integration on your instance. To access the guided setup, see the section titled Configure the Service Graph Connector for Splunk.

## CMDB integrations dashboard

The Integration Commons for CMDB store app provides a dashboard with a central view of the status, processing results, and processing errors of all installed integrations. You can see metrics for all integration runs. You can filter the view to a specific CMDB integration, a specific time duration, or a specific integration run. For more details about monitoring integrations in the CMDB Integrations Dashboard, see [Using the CMDB Integrations Dashboard](../../../configuration-management/concept/integration-commons-for-cmdb.md#section_fxg_lh4_blb).

