---
title: Service Graph Connector for Jamf properties
description: Service Graph Connector for Jamf properties control the behavior of the connector.
locale: en-US
release: zurich
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Jamf, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Service Graph Connector for Jamf properties

Service Graph Connector for Jamf properties control the behavior of the connector.

## Connection properties

These connection properties are available for the Service Graph Connector for Jamf.

**Note:** To open the Service Graph Connection Properties \[sn\_cmdb\_int\_util\_service\_graph\_connection\_property\] table for the connector, navigate to **All** &gt; **Service Graph Connectors** &gt; **Jamf** &gt; **Connections**, and select the connection name. The connection properties are displayed in the Service Graph Connection Properties related list.

<table id="table_xtl_vjd_d2c"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

auth\_type

</td><td>

Set the property to `basic` to use Basic authentication for the connection. This authentication type uses a user name and password.Set the property to `oauth` to use Client credentials \(OAuth 2.0\) authentication for the connection. This authentication type uses a client ID and client secret.

The default Bearer token authentication type uses a user name and password to retrieve a token for subsequent connection requests.

-   Type: basic \| bearer \| oauth
-   Default value: `bearer`

**Note:**

-   For an OOB default connection, any of the three authentication types can be used.
-   For additional connections \(multi-instance\), only the Basic and Bearer authentication types can be used. To use the Client credentials \(OAuth 2.0\) authentication type, follow the guided setup to configure client authentication credentials for the connection. See [Configure Service Graph Connector for Jamf using the guided setup](../task/configure-jamf-integration.md).

</td></tr><tr><td>

import\_managed\_apps\_only

</td><td>

Set the property to `true` to import only managed application records.When the property is set to `false`, all application records are imported.

-   Type: true \| false
-   Default value: `false`

</td></tr><tr><td>

is\_delta\_enabled\_for\_computers

</td><td>

Set the property to `true` to enable the SG-Jamf Computers data source to pull only the changes \(delta\) between consecutive imports. When the property is set to `false`, a full import is performed with every pull.

**Note:** This property is available only if the **use\_jamf\_pro\_api** property is set to `true`.

-   Type: true \| false
-   Default value: `false`

See [Configuring data synchronization in Service Graph Connector for Jamf](../concept/sgc-cmdb-jamf-data-sync.md#).

</td></tr><tr><td>

is\_delta\_enabled\_for\_mobiles

</td><td>

Set the property to `true` to enable the SG-Jamf Mobile Devices data source to pull only the changes \(delta\) between consecutive imports. When the property is set to `false`, a full import is performed with every pull.

**Note:** This property is available only if the **use\_jamf\_mobile\_pro\_api** property is set to `true`.

-   Type: true \| false
-   Default value: `false`

See [Configuring data synchronization in Service Graph Connector for Jamf](../concept/sgc-cmdb-jamf-data-sync.md#).

</td></tr><tr><td>

use\_jamf\_mobile\_pro\_api

</td><td>

Set the property to `true` to use the Jamf Pro API for querying Jamf mobile device records. Set the property to `false` to use the Jamf Classic API.**Note:** The Jamf Pro API is supported by Jamf version 11.4 and higher. The Jamf Pro API supports pagination of response data and provides performance improvement compared to the Jamf Classic API.

-   Type: true \| false
-   Default value: null

</td></tr><tr><td>

use\_jamf\_pro\_api

</td><td>

Set the property to `false` to use the Jamf Classic API instead of the Jamf Pro API for querying Jamf mobile device records. When the property is set to `true`, the Jamf Pro API is used for querying Jamf mobile device records.

**Note:** The Jamf Pro API is supported by Jamf version 11.4 and higher. The Jamf Pro API supports pagination of response data and provides performance improvement compared to the Jamf Classic API.

-   Type: true \| false
-   Default value: `true`

</td></tr></tbody>
</table>