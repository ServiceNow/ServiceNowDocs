---
title: Service Graph Connector for Nautobot
description: Use the Service Graph Connector for Nautobot to integrate the data discovered by Nautobot into your ServiceNow instance to support various use cases.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/servicenow-platform/service-graph-connectors/sgc-integration-nautobot.html
release: zurich
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: concept
last_updated: "2026-04-07"
reading_time_minutes: 2
breadcrumb: [Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Service Graph Connector for Nautobot

Use the Service Graph Connector for Nautobot to integrate the data discovered by Nautobot into your ServiceNow instance to support various use cases.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

## Supported versions

-   Zurich Patch 4
-   Australia
-   Brazil

## Use cases

The Service Graph Connector for Nautobot brings data into the API Insights capability of the ServiceNow platform, enabling the management of different APIs in one instance. The connector adds information discovered by Nautobot to the CMDB CI classes.

## Configuring a connection for the connector

Use the SGC Central view in the Service Graph Workspace or CMDB Workspace to install the connector and configure the connection. The view enables you to install and discover connectors and to manage the full life cycle of creating, editing, monitoring, and debugging connections. For instructions, see [Configure Service Graph Connector for Nautobot using SGC Central](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgcc-configure-nautobot.md).

## CMDB integrations dashboard

The Integration Commons for CMDB store app provides a dashboard with a central view of the status, processing results, and processing errors of all installed integrations. You can see metrics for all integration runs. You can filter the view to a specific CMDB integration, a specific time duration, or a specific integration run. For more details about monitoring Nautobot integrations in the CMDB Integrations Dashboard, see [Using the CMDB Integrations Dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/cmdb-integration-commons/integration-commons-for-cmdb.md).

## Data mapping

Data from the Nautobot data sources is mapped and transformed into the ServiceNow CMDB Configuration Item \(CI\) class definitions using the Robust Transform Engine \(RTE\). Data is inserted into the ServiceNow CMDB using the Identification and Reconciliation Engine \(IRE\).

The following table lists the data sources, the staging tables, and the target tables as CMDB CI and non-CMDB classes for Nautobot.

<table id="table_data_mapping" class="custom-rows"><thead><tr><th class="filter">

Data source

</th><th>

Staging table

</th><th>

Target tables

</th></tr></thead><tbody><tr><td>

SG-Nautobot Server

</td><td>

sn\_nautobot\_integ\_sg\_nautobot\_server

</td><td>

[Server \[cmdb\_ci\_server\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-nautobot-classes.md) [Linux Server \[cmdb\_ci\_linux\_server\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-nautobot-classes.md)

 [Windows Server \[cmdb\_ci\_win\_server\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-nautobot-classes.md)

</td></tr><tr><td>

SG-Nautobot IP Address

</td><td>

sn\_nautobot\_integ\_sg\_nautobot\_ip\_address

</td><td>

[Allocated IP Address \[cmdb\_ci\_allocated\_ip\_address\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-nautobot-classes.md)

</td></tr><tr><td>

SG-Nautobot Namespace

</td><td>

sn\_nautobot\_integ\_sg\_nautobot\_namespace

</td><td>

[Managed Network \[cmdb\_ci\_managed\_network\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-nautobot-classes.md)

</td></tr><tr><td>

SG-Nautobot Prefixes

</td><td>

sn\_nautobot\_integ\_sg\_nautobot\_prefixes

</td><td>

[Managed IP Network Subnet \[cmdb\_ci\_ip\_network\_subnet\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-nautobot-classes.md)

</td></tr></tbody>
</table>You can use the IntegrationHub ETL app to view the data maps. See [IntegrationHub ETL](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/integration-hub-etl/integrationhub-etl.md) for more information.

**Related topics**  


[Service Graph Connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-sgc-available.md)

[Configure Service Graph Connector for Nautobot using SGC Central](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgcc-configure-nautobot.md)

[CMDB classes targeted in Service Graph Connector for Nautobot](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-nautobot-classes.md)

