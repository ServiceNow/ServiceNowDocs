---
title: Data mapping for Service Graph Connector for NetBrain
description: Data from the NetBrain data sources is mapped and transformed into the ServiceNow CMDB Configuration Item \(CI\) class definitions using the Robust Transform Engine \(RTE\). Data is inserted into the ServiceNow CMDB using the Identification and Reconciliation Engine \(IRE\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/service-graph-connectors/sgc-data-mapping-netbrain.html
release: brazil
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: reference
last_updated: "2026-10-06"
reading_time_minutes: 1
breadcrumb: [NetBrain, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Data mapping for Service Graph Connector for NetBrain

Data from the NetBrain data sources is mapped and transformed into the ServiceNow CMDB Configuration Item \(CI\) class definitions using the Robust Transform Engine \(RTE\). Data is inserted into the ServiceNow CMDB using the Identification and Reconciliation Engine \(IRE\).

## Data mapping for Service Graph Connector for NetBrain

When you complete setting up the connection, you can configure the integration to periodically pull data from NetBrain.

The following table lists the data sources, the staging tables, and the target tables as CMDB CI classes for the Service Graph Connector for NetBrain.

<table id="table_data_mapping" class="custom-rows"><thead><tr><th class="filter">

Data source

</th><th>

Staging table

</th><th>

Target tables

</th></tr></thead><tbody><tr><td>

SG-NetBrain One IP

</td><td>

sn\_netbrain\_integ\_one\_ip

</td><td>

[Network Adapter \[cmdb\_ci\_network\_adapter\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/service-graph-connectors/sgc-netbrain-classes.md) [Switch \[cmdb\_ci\_netgear\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/service-graph-connectors/sgc-netbrain-classes.md)

 [Device \[cmdb\_ci\_hardware\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/service-graph-connectors/sgc-netbrain-classes.md)

</td></tr><tr><td>

SG-NetBrain ESX Server-Switch

</td><td>

sn\_netbrain\_integ\_adt\_staging

</td><td>

[Device \[cmdb\_ci\_hardware\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/service-graph-connectors/sgc-netbrain-classes.md) [IP Switch \[cmdb\_ci\_ip\_switch\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/service-graph-connectors/sgc-netbrain-classes.md)

</td></tr></tbody>
</table>You can use the IntegrationHub ETL app to view the data maps. See [IntegrationHub ETL](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/integration-hub-etl/integrationhub-etl.md) for more information.

