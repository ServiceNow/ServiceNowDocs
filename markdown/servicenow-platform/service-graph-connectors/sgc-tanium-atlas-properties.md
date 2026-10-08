---
title: Service Graph Connector for Tanium Atlas properties
description: Service Graph Connector for Tanium Atlas properties control the behavior of the connector.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/servicenow-platform/service-graph-connectors/sgc-tanium-atlas-properties.html
release: zurich
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: reference
last_updated: "2026-10-06"
reading_time_minutes: 1
breadcrumb: [Tanium Atlas, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Service Graph Connector for Tanium Atlas properties

Service Graph Connector for Tanium Atlas properties control the behavior of the connector.

## Connection properties

These connection properties are available for Service Graph Connector for Tanium Atlas.

**Note:** To open the Service Graph Connection Properties \[sn\_cmdb\_int\_util\_service\_graph\_connection\_property\] table for the connector, navigate to **All** &gt; **Service Graph Connectors** &gt; **Tanium Atlas** &gt; **Connections** and select the connection name. The connection properties are displayed in the Service Graph Connection Properties related list.

<table id="table_conn_props_tanium-atlas"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

rest\_action\_limit

</td><td>

Page size per API call for REST action. Default value: `50`

</td></tr><tr><td>

max\_retry\_count

</td><td>

The maximum time a retry is triggered for the REST action. Default value: `3`

</td></tr></tbody>
</table>## System properties

These system properties are available for Service Graph Connector for Tanium Atlas.

**Note:** To open the System Properties \[sys\_properties\] table, enter `sys_properties.list` in the navigation filter.

<table id="table_sys_props_tanium-atlas"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_tanium\_atlas.buffer\_days\_from\_last\_scan\_for\_hardware

</td><td>

This specifies the number of days to consider a software as still active after the last scan of harware on which it is installed-   Type: integer
-   Default value: `0`
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

sn\_tanium\_atlas.exclude\_serial\_number\_for\_certain\_os

</td><td>

Exclude the serial number population on the CI for aix and solaris OS platforms-   Type: string
-   Default value: `true`
-   Location: System Property \[sys\_properties\] table

</td></tr></tbody>
</table>