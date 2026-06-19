---
title: Service Graph Connector for Rapid7
description: The Service Graph Connector for Rapid7 pulls in asset inventory data \(hardware and software\) from the Rapid7 database into the Configuration Management Database \(CMDB\) application in your ServiceNow AI Platform instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/servicenow-platform/service-graph-connectors/sgc-rapid7-integration.html
release: zurich
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Service Graph Connector for Rapid7

The Service Graph Connector for Rapid7 pulls in asset inventory data \(hardware and software\) from the Rapid7 database into the Configuration Management Database \(CMDB\) application in your ServiceNow AI Platform® instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Supported versions

-   Version 4.0 of the Rapid7 InsightVM application.
-   Utah, Vancouver, and Washington ServiceNow® family releases.

## Use cases

-   Complement the data from the Rapid7 InsightVM discovery product.
-   Import hardware data and details about your assets from the Rapid7 InsightVM integration and store them in appropriate configuration item \(CI\) classes in your CMDB.

## CMDB integrations dashboard

The Integration Commons for CMDB store app provides a dashboard with a central view of the status, processing results, and processing errors of all installed integrations. You can see metrics for all integration runs. You can filter the view to a specific CMDB integration, a specific time duration, or a specific integration run. For more details about monitoring Rapid7 integrations in the CMDB Integrations Dashboard, see [Using the CMDB Integrations Dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/cmdb-integration-commons/integration-commons-for-cmdb.md).

## Guided setup

Use the guided setup feature for the Service Graph Connector for Rapid7 to help you configure your integration in an organized sequence of tasks.

**Note:** The API token requires the InsightIDR viewer role.

## Configure the Service Graph Connector for Rapid7

After you have followed the instructions provided to you to download and activate the Service Graph Connector for Rapid7 application, refer to  and . There are a few steps you need to complete before you configure this integration.

