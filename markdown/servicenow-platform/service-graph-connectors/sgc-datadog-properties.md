---
title: Observability-Datadog properties
description: Observability-Datadog properties control the behavior of the connector.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/servicenow-platform/service-graph-connectors/sgc-datadog-properties.html
release: zurich
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: reference
last_updated: "2026-05-01"
reading_time_minutes: 1
breadcrumb: [Observability-Datadog, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Observability-Datadog properties

Observability-Datadog properties control the behavior of the connector.

## Connection properties

These connection properties are available for Observability-Datadog.

**Note:** To open the Service Graph Connection Properties \[sn\_cmdb\_int\_util\_service\_graph\_connection\_property\] table for the connector, navigate to **All** &gt; **Service Graph Connectors** &gt; **Observability-Datadog** &gt; **Connections** and select the connection name. The connection properties are displayed in the Service Graph Connection Properties related list.

<table id="table_conn_props_datadog"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

hosts\_filter

</td><td>

Comma-separated list of host tags in the key:value format to define a filter for pulling host data from Datadog. Example: datadog:monitored,env:production

</td></tr></tbody>
</table>## System properties

These system properties are available for Observability-Datadog.

**Note:** To open the System Properties \[sys\_properties\] table, enter `sys_properties.list` in the navigation filter.

<table id="table_sys_props_datadog"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_datadog\_integra.datadog\_enabled

</td><td>

-   Type: boolean
-   Default value: `false`
-   Location: System Property \[sys\_properties\] table

</td></tr></tbody>
</table>