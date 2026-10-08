---
title: Data mapping for Service Graph Connector for Omnissa Workspace ONE UEM
description: Data from the Omnissa data sources is mapped and transformed into the ServiceNow CMDB Configuration Item \(CI\) class definitions using the Robust Transform Engine \(RTE\). Data is inserted into the ServiceNow CMDB using the Identification and Reconciliation Engine \(IRE\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/service-graph-connectors/sgc-data-mapping-omnissa-works.html
release: brazil
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: reference
last_updated: "2026-09-22"
reading_time_minutes: 1
breadcrumb: [Omnissa Workspace ONE UEM, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Data mapping for Service Graph Connector for Omnissa Workspace ONE UEM

Data from the Omnissa data sources is mapped and transformed into the ServiceNow CMDB Configuration Item \(CI\) class definitions using the Robust Transform Engine \(RTE\). Data is inserted into the ServiceNow CMDB using the Identification and Reconciliation Engine \(IRE\).

## Data mapping for Service Graph Connector for Omnissa Workspace ONE UEM

When you complete setting up the connection, you can configure the integration to periodically pull data from Omnissa.

The following table lists the data sources, the staging tables, and the target tables as CMDB CI classes for the Service Graph Connector for Omnissa Workspace ONE UEM.

<table id="table_data_mapping" class="custom-rows"><thead><tr><th class="filter">

Data source

</th><th>

Staging table

</th><th>

Target tables

</th></tr></thead><tbody><tr><td>

SG-Omnissa WS1 Device

</td><td>

sn\_omnwoneuem\_inte\_sg\_omnissa\_ws1\_device

</td><td>

[Handheld Computing Device \[cmdb\_ci\_handheld\_computing\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/service-graph-connectors/sgc-omnissa-works-classes.md) [Network Adapter \[cmdb\_ci\_network\_adapter\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/service-graph-connectors/sgc-omnissa-works-classes.md)

 [Media Player \[cmdb\_ci\_media\_player\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/service-graph-connectors/sgc-omnissa-works-classes.md)

 [Printer \[cmdb\_ci\_printer\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/service-graph-connectors/sgc-omnissa-works-classes.md)

 [Hardware \[cmdb\_ci\_hardware\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/service-graph-connectors/sgc-omnissa-works-classes.md)

 [Computer \[cmdb\_ci\_computer\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/service-graph-connectors/sgc-omnissa-works-classes.md)

</td></tr><tr><td>

SG-Omnissa WS1 Remove Software

</td><td>

sn\_cmdb\_int\_util\_remove\_record

</td><td>

[Software \[cmdb\_ci\_spkg\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/service-graph-connectors/sgc-omnissa-works-classes.md)

</td></tr><tr><td>

SG-Omnissa WS1 Usage

</td><td>

sn\_omnwoneuem\_inte\_sg\_omnissa\_ws1\_usage

</td><td>

SG-Omnissa WS1 Usage

</td></tr><tr><td>

SG-Omnissa WS1 Apps

</td><td>

sn\_omnwoneuem\_inte\_sg\_omnissa\_ws1\_apps

</td><td>

[Software \[cmdb\_ci\_spkg\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/service-graph-connectors/sgc-omnissa-works-classes.md) [Hardware \[cmdb\_ci\_hardware\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/service-graph-connectors/sgc-omnissa-works-classes.md)

</td></tr></tbody>
</table>You can use the IntegrationHub ETL app to view the data maps. See [IntegrationHub ETL](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/integration-hub-etl/integrationhub-etl.md) for more information.

