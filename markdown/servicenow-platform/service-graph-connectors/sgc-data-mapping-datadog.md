---
title: Data mapping for Observability-Datadog
description: Data from the Observability-Datadog data sources is mapped and transformed into the ServiceNow CMDB Configuration Item \(CI\) class definitions using the Robust Transform Engine \(RTE\). Data is inserted into the ServiceNow CMDB using the Identification and Reconciliation Engine \(IRE\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/servicenow-platform/service-graph-connectors/sgc-data-mapping-datadog.html
release: zurich
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: reference
last_updated: "2026-05-01"
reading_time_minutes: 1
breadcrumb: [Observability-Datadog, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Data mapping for Observability-Datadog

Data from the Observability-Datadog data sources is mapped and transformed into the ServiceNow CMDB Configuration Item \(CI\) class definitions using the Robust Transform Engine \(RTE\). Data is inserted into the ServiceNow CMDB using the Identification and Reconciliation Engine \(IRE\).

## Data mapping for Observability-Datadog

When you complete setting up the connection, you can configure the integration to periodically pull data from Observability-Datadog.

The following table lists the data sources, the staging tables, and the target tables as CMDB CI classes for Observability-Datadog.

<table id="table_data_mapping" class="custom-rows"><thead><tr><th class="filter">

Data source

</th><th>

Staging table

</th><th>

Target tables

</th></tr></thead><tbody><tr><td>

SGO Datadog - Services Catalog

</td><td>

sn\_datadog\_integra\_datadog\_service\_catalog

</td><td>

Calculated Application Service \[cmdb\_ci\_service\_calculated\]

</td></tr><tr><td>

SGO-Datadog application services

</td><td>

sn\_datadog\_integra\_datadog\_application\_services

</td><td>

Calculated Application Service \[cmdb\_ci\_service\_calculated\] [Server \[cmdb\_ci\_server\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-datadog-classes.md)

</td></tr><tr><td>

SGO Datadog - Hosts

</td><td>

sn\_datadog\_integra\_datadog\_hosts

</td><td>

[Logical Datacenter \[cmdb\_ci\_logical\_datacenter\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-datadog-classes.md) [Network Adapter \[cmdb\_ci\_network\_adapter\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-datadog-classes.md)

 [Server \[cmdb\_ci\_server\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-datadog-classes.md)

 [Cloud DataBase \[cmdb\_ci\_cloud\_database\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-datadog-classes.md)

 [Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-datadog-classes.md)

 [Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-datadog-classes.md)

 [IP Address \[cmdb\_ci\_ip\_address\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-datadog-classes.md)

 Software \[cmdb\_ci\_spkg\]

</td></tr><tr><td>

SGO Datadog - Service Relation

</td><td>

sn\_datadog\_integra\_datadog\_service\_relation

</td><td>

Calculated Application Service \[cmdb\_ci\_service\_calculated\]

</td></tr><tr><td>

SGO-Datadog Hosts

</td><td>

sn\_datadog\_integra\_datadog\_hosts

</td><td>

[Logical Datacenter \[cmdb\_ci\_logical\_datacenter\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-datadog-classes.md) [Network Adapter \[cmdb\_ci\_network\_adapter\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-datadog-classes.md)

 [Server \[cmdb\_ci\_server\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-datadog-classes.md)

 [Cloud DataBase \[cmdb\_ci\_cloud\_database\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-datadog-classes.md)

 [Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-datadog-classes.md)

 [Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-datadog-classes.md)

 [IP Address \[cmdb\_ci\_ip\_address\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-datadog-classes.md)

 Software \[cmdb\_ci\_spkg\]

</td></tr></tbody>
</table>You can use the IntegrationHub ETL app to view the data maps. See [IntegrationHub ETL](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/integration-hub-etl/integrationhub-etl.md) for more information.

