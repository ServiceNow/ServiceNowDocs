---
title: Service Graph Connector for Tanium Endpoints properties
description: Service Graph Connector for Tanium Endpoints properties control the behavior of the connector.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/servicenow-platform/service-graph-connectors/sgc-tanium-endpoints-properties.html
release: zurich
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: reference
last_updated: "2026-05-12"
reading_time_minutes: 1
breadcrumb: [Reference, Tanium Endpoints, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Service Graph Connector for Tanium Endpoints properties

Service Graph Connector for Tanium Endpoints properties control the behavior of the connector.

## Connection properties

These connection properties are available for the Service Graph Connector for Tanium Endpoints.

**Note:** To open the Service Graph Connection Properties \[sn\_cmdb\_int\_util\_service\_graph\_connection\_property\] table for the connector, navigate to **All** &gt; **Service Graph Connectors** &gt; **Tanium Endpoints** &gt; **Connections** and select the connection name. The connection properties are displayed in the Service Graph Connection Properties related list.

<table id="table_conn_props_tanium-endpoints"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

max\_retry\_count

</td><td>

Specifies the maximum number of retry attempts for the REST action.Default value: `3`

</td></tr><tr><td>

rest\_action\_limit

</td><td>

Specifies the page size per API call for the REST action. Default value: `50`

</td></tr></tbody>
</table>## System properties

These system properties are available for the Service Graph Connector for Tanium Endpoints.

**Note:** To open the System Properties \[sys\_properties\] table, enter `sys_properties.list` in the navigation filter.

<table id="table_sys_props_tanium-endpoints"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_tanium\_endpoint.buffer\_days\_from\_last\_scan\_for\_hardware

</td><td>

Specifies the number of days to consider a software as active after the last scan of the hardware on which it is installed.-   Type: integer
-   Default value: `0`
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

sn\_tanium\_endpoint.exclude\_serial\_number\_for\_certain\_os

</td><td>

Set this property to `true` to exclude the serial number from the CI record for the AIX and Solaris OS platforms.-   Type: string
-   Default value: `true`
-   Location: System Property \[sys\_properties\] table

</td></tr></tbody>
</table>**Parent Topic:**[Service Graph Connector for Tanium Endpoints reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-tanium-endpoints-reference.md)

