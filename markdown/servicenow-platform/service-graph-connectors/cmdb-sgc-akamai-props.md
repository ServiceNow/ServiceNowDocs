---
title: Service Graph Connector for Akamai API Security properties
description: Service Graph Connector for Akamai API Security properties control the behavior of the connector.
locale: en-US
release: xanadu
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: reference
last_updated: "2025-10-13"
reading_time_minutes: 1
breadcrumb: [Akamai API Security, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Service Graph Connector for Akamai API Security properties

Service Graph Connector for Akamai API Security properties control the behavior of the connector.

## Connection properties

These connection properties are available for the Service Graph Connector for Akamai API Security.

**Note:** To open the Service Graph Connection Properties \[sn\_cmdb\_int\_util\_service\_graph\_connection\_property\] table for the connector, navigate to **All** &gt; **Service Graph Connectors** &gt; **Akamai API Security** &gt; **Connections**, and select the connection name. The connection properties are displayed in the Service Graph Connection Properties related list.

<table id="table_d2w_pzn_ygc"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Import tags

</td><td>

Set the property to `true` to import API tags.-   Type: true \| false
-   Default value: `false`

</td></tr><tr><td>

Tags storage type

</td><td>

Specify whether the tag values should be stored in the Key Value \[cmdb\_key\_value\] table or in the **Attributes** field of the API Component \[cmdb\_ci\_api\_component\] table. -   Type: cmdb\_key\_value \| attributes
-   Default value: `cmdb_key_value`

</td></tr><tr><td>

Tags value separator

</td><td>

Specify the delimiter to parse tag strings into key-value pairs.​-   Type: custom
-   Default value: null

</td></tr></tbody>
</table>