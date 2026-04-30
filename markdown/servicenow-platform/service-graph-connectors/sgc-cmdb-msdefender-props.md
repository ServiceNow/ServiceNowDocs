---
title: Service Graph Connector for Microsoft Defender Endpoint properties
description: Service Graph Connector for Microsoft Defender Endpoint properties control the behavior of the connector.
locale: en-US
release: yokohama
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Microsoft Defender for Endpoint, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Service Graph Connector for Microsoft Defender Endpoint properties

Service Graph Connector for Microsoft Defender Endpoint properties control the behavior of the connector.

## System properties

These system properties are available for Service Graph Connector for Microsoft Defender Endpoint.

**Note:** To open the System Properties \[sys\_properties\] table, enter `sys_properties.list` in the navigation filter.

<table id="table_w4t_nrm_jzb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_defender\_integ.pagination\_record\_count

</td><td>

Enter the maximum number of rows fetched in the List machines API response from the machine resource type.-   Type: integer
-   Default value: `500`
-   Location: System Property \[sys\_properties\] table

</td></tr></tbody>
</table>