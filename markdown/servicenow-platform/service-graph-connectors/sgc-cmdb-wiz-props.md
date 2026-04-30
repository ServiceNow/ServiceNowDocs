---
title: Service Graph Connector for Wiz properties
description: Service Graph Connector for Wiz properties control the behavior of the connector.
locale: en-US
release: yokohama
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: reference
last_updated: "2025-11-03"
reading_time_minutes: 1
breadcrumb: [Wiz, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Service Graph Connector for Wiz properties

Service Graph Connector for Wiz properties control the behavior of the connector.

## Connection properties

These connection properties are available for Service Graph Connector for Wiz.

**Note:** To open the Service Graph Connection Properties \[sn\_cmdb\_int\_util\_service\_graph\_connection\_property\] table for the connector, navigate to **All** &gt; **Service Graph Connectors** &gt; **Wiz** &gt; **Connections** and select the connection name. The connection properties are displayed in the Service Graph Connection Properties related list.

|Property|Description|
|--------|-----------|
|Projects|Enter a list of comma-separated Project IDs for which the resource data should be collected. For multiple entries, separate the IDs with commas.|
|Exclude Projects|Enter a list of comma-separated Project IDs for which the resources are excluded only when the Projects property isn't set. In this case, all the resources except for the specified projects are imported. For multiple entries, separate the names with commas.|
|Server Bypass|Set the value to `true` to link VM data to existing Server records instead of creating new records. If the value is set to `false`, new Server and VM records are created.|
|Fetch Scaleset VMs|Set the value to `true` to import Scale Set VM records. If the value is set to `false`, Scale Set VMs aren't imported.​|

## System properties

These system properties are available for Service Graph Connector for Wiz.

**Note:** To open the System Properties \[sys\_properties\] table, enter `sys_properties.list` in the navigation filter.

<table id="table_w4t_nrm_jzb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_wiz\_integ.list\_resources\_action.page\_size

</td><td>

Enter the page size used in REST requests to fetch Wiz entities.-   Type: string
-   Default value: `100`
-   Location: System Property \[sys\_properties\] table

</td></tr></tbody>
</table>