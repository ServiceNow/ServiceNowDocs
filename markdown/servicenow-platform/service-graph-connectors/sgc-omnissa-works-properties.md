---
title: Service Graph Connector for Omnissa Workspace ONE UEM properties
description: Service Graph Connector for Omnissa Workspace ONE UEM properties control the behavior of the connector.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/service-graph-connectors/sgc-omnissa-works-properties.html
release: brazil
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: reference
last_updated: "2026-09-22"
reading_time_minutes: 1
breadcrumb: [Omnissa Workspace ONE UEM, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Service Graph Connector for Omnissa Workspace ONE UEM properties

Service Graph Connector for Omnissa Workspace ONE UEM properties control the behavior of the connector.

## Connection properties

These connection properties are available for Service Graph Connector for Omnissa Workspace ONE UEM.

**Note:** To open the Service Graph Connection Properties \[sn\_cmdb\_int\_util\_service\_graph\_connection\_property\] table for the connector, navigate to **All** &gt; **Service Graph Connectors** &gt; **Omnissa Workspace ONE UEM** &gt; **Connections** and select the connection name. The connection properties are displayed in the Service Graph Connection Properties related list.

<table id="table_conn_props_omnissa-works"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

hostname

</td><td>

Host URL to create, run, track, and download reports.

</td></tr><tr><td>

managed\_apps\_only

</td><td>

When true, only apps reported with app\_is\_managed=true are imported. Mirrors the managed\_apps\_only behavior of the Workspace ONE UEM connector's Apps data source. Default value: `false`

</td></tr></tbody>
</table>