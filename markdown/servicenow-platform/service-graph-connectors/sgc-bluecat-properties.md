---
title: Service Graph Connector for BlueCat properties
description: Service Graph Connector for BlueCat properties control the behavior of the connector.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/servicenow-platform/service-graph-connectors/sgc-bluecat-properties.html
release: zurich
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [BlueCat, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Service Graph Connector for BlueCat properties

Service Graph Connector for BlueCat properties control the behavior of the connector.

## Connection properties

These connection properties are available for Service Graph Connector for BlueCat.

**Note:** To open the Service Graph Connection Properties \[sn\_cmdb\_int\_util\_service\_graph\_connection\_property\] table for the connector, navigate to **All** &gt; **Service Graph Connectors** &gt; **BlueCat** &gt; **Connections** and select the connection name. The connection properties are displayed in the Service Graph Connection Properties related list.

<table id="table_conn_props_bluecat"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

IPv6 network type

</td><td>

Set this property to true to enable the import of IPv6 IPAM data. When set to false, IPv6 data isn't imported. Default value: `true`

</td></tr><tr><td>

Chunk size for IP address retrieval

</td><td>

Specify the number of networks per chunk from which IP address data should be imported. Invalid values are auto-adjusted based on load and node count. Default value: `2`

</td></tr><tr><td>

IPv4 network type

</td><td>

Set this property to true to enable the import of IPv4 IPAM data. When set to false, IPv4 data isn't imported. Default value: `true`

</td></tr></tbody>
</table>## System properties

These system properties are available for Service Graph Connector for BlueCat.

**Note:** To open the System Properties \[sys\_properties\] table, enter `sys_properties.list` in the navigation filter.

<table id="table_sys_props_bluecat"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_bluecat\_integ.included\_network\_regex

</td><td>

-   Type: string
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

sn\_bluecat\_integ.task\_create\_on\_network\_insert

</td><td>

Create a task when a network is inserted-   Type: true \| false
-   Default value: `false`
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

sn\_bluecat\_integ.excluded\_network\_regex

</td><td>

-   Type: string
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

sn\_bluecat\_integ.task\_create\_on\_network\_delete

</td><td>

Create a task when a network is deleted-   Type: true \| false
-   Default value: `true`
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

sn\_bluecat\_integ.get\_ipam\_data\_action\_page\_size

</td><td>

Page Size of the BlueCat API Response-   Type: integer
-   Default value: `100`
-   Location: System Property \[sys\_properties\] table

</td></tr></tbody>
</table>