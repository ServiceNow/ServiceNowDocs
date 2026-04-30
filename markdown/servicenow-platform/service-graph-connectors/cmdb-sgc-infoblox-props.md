---
title: Service Graph Connector for Infoblox properties
description: Service Graph Connector for Infoblox properties control the behavior of the connector.
locale: en-US
release: yokohama
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: reference
last_updated: "2026-03-03"
reading_time_minutes: 2
breadcrumb: [Reference, Infoblox, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Service Graph Connector for Infoblox properties

Service Graph Connector for Infoblox properties control the behavior of the connector.

## Connection properties

These connection properties are available for the Service Graph Connector for Infoblox.

**Note:** To open the Service Graph Connection Properties \[sn\_cmdb\_int\_util\_service\_graph\_connection\_property\] table for the connector, navigate to **All** &gt; **Service Graph Connectors** &gt; **Infoblox** &gt; **Connections**, and select the connection name. The connection properties are displayed in the Service Graph Connection Properties related list.

<table id="table_ywm_hz1_m3c"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td>

Version of the Infoblox API.

</td></tr><tr><td>

network\_view

</td><td>

Enter the names \(as a comma-separated list\) of the Infoblox Network Views from which data is to be imported.**Note:** If a value isn't specified for this property, data is imported from all Infoblox network views.

 -   Type: string
-   Default value: empty

</td></tr></tbody>
</table>## System properties

These system properties are available for the Service Graph Connector for Infoblox.

**Note:** To open the System Properties \[sys\_properties\] table, enter `sys_properties.list` in the navigation filter.

<table id="table_rpm_gz1_m3c"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_infoblox\_integ.parallel\_loading\_partition\_size

</td><td>

Set the maximum number of networks that each partition processes.The maximum value that can be set for this property is `150`.

-   Type: integer
-   Default value: empty
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

sn\_infoblox\_integ.default\_get\_ip\_address

</td><td>

Set a global default value for the **Get IP Address** option.When the value is set to `true`, all newly imported networks automatically retrieve IP address details. You can specify which IP addresses are to be excluded from the import by using the **sn\_infoblox\_integ.excluded\_network\_regex** system property.

When the value is set to `false`, networks don't retrieve IP addresses by default. You can specify which IP addresses are to be imported by using the **sn\_infoblox\_integ.included\_network\_regex** system property.

-   Type: true \| false
-   Default value: `false`
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

sn\_infoblox\_integ.included\_network\_regex

</td><td>

Enter the list of IP addresses to be imported. Specify the list in pipe-delimited string format.-   Type: string
-   Default value: empty
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

sn\_infoblox\_integ.excluded\_network\_regex

</td><td>

Enter the list of IP addresses to be excluded from the import. Specify the list in pipe-delimited string format.-   Type: string
-   Default value: empty
-   Location: System Property \[sys\_properties\] table

</td></tr></tbody>
</table>## Related content

[Data mapping for Service Graph Connector for Infoblox](cmdb-data-mapping-infoblox.md)

[CMDB classes targeted in Service Graph Connector for Infoblox](sgc-cmdb-infoblox-classes.md)

**Parent Topic:**[Service Graph Connector for Infoblox reference](../concept/sgc-cmdb-infoblox-reference.md)

