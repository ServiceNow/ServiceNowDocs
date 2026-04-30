---
title: Service Graph Connector for OpenTelemetry properties
description: Service Graph Connector for OpenTelemetry properties control the behavior of the connector.
locale: en-US
release: xanadu
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: reference
last_updated: "2026-02-27"
reading_time_minutes: 1
breadcrumb: [OpenTelemetry, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Service Graph Connector for OpenTelemetry properties

Service Graph Connector for OpenTelemetry properties control the behavior of the connector.

**Important:** Starting with the Australia release, Service Graph Connector for OpenTelemetry is being prepared for future deprecation. It will be hidden and no longer installed on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

## Connection properties

These connection properties are available for Service Graph Connector for OpenTelemetry.

**Note:** To open the Service Graph Connection Properties \[sn\_cmdb\_int\_util\_service\_graph\_connection\_property\] table for the connector, navigate to **All** &gt; **Service Graph Connectors** &gt; **OpenTelemetry** &gt; **Connections** and select the connection name. The connection properties are displayed in the Service Graph Connection Properties related list.

<table id="table_tmg_rjm_lzb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Organization

</td><td>

Enter the name of an OpenTelemetry organization.-   Type: string
-   Default value: None
-   Location: Service Graph Connection Properties \[sn\_cmdb\_int\_util\_service\_graph\_connection\_property\] table

</td></tr><tr><td>

Lookback Time

</td><td>

Enter time in hours to retrieve OpenTelemetry resources.-   Type: integer
-   Default value: `12`
-   Location: Service Graph Connection Properties \[sn\_cmdb\_int\_util\_service\_graph\_connection\_property\] table

</td></tr></tbody>
</table>## System properties

These system properties are available for Service Graph Connector for OpenTelemetry.

**Note:** To open the System Properties \[sys\_properties\] table, enter `sys_properties.list` in the navigation filter.

<table id="table_w4t_nrm_jzb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_sg\_lightstep.classes\_to\_inactivate\_stale\_records

</td><td>

Enter a list of configuration item \(CI\) classes to be inactivated as stale records. For multiple entries, separate the CI classes with commas.-   Type: string
-   Default value: None
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

sn\_sg\_lightstep.events\_for\_unmatched\_ci.enabled

</td><td>

Set the property to `true` to ingest events that don't have a matching CI in CMDB.-   Type: true \| false
-   Default value: `false`
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

sn\_sg\_lightstep.resource\_api\_num\_rows

</td><td>

Enter the maximum number of rows fetched in the Resource API response from OpenTelemetry resources.-   Type: integer
-   Default value: `2500`
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

sn\_sg\_lightstep.service\_map\_classes\_to\_exclude

</td><td>

Enter a list of CI classes to be excluded from the service map. For multiple entries, separate the CI classes with commas.-   Type: string
-   Default value: None
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

sn\_sg\_lightstep.service\_map\_max\_levels

</td><td>

Enter the maximum hierarchy level of CIs to be included in the service map. -   Type: integer
-   Default value: `5`
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

sn\_sg\_lightstep.service\_map\_relationship\_types\_to\_exclude

</td><td>

Enter a list of Cl relationship types to be excluded from the service map. For multiple entries, separate the CI relationship types with commas.-   Type: string
-   Default value: None
-   Location: System Property \[sys\_properties\] table

</td></tr></tbody>
</table>