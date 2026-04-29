---
title: Service Graph Connector for Microsoft Intune properties
description: Service Graph Connector properties control the behavior of connections.
locale: en-US
release: australia
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Microsoft Intune, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Service Graph Connector for Microsoft Intune properties

Service Graph Connector properties control the behavior of connections.

## Connection properties

These connection properties are available for Service Graph Connector for Microsoft Intune.

**Note:** To open the Service Graph Connection Properties \[sn\_cmdb\_int\_util\_service\_graph\_connection\_property\] table for the connector, navigate to **All** &gt; **Service Graph Connectors** &gt; **Intune** &gt; **Connections** and select the connection name. The connection properties are displayed in the Service Graph Connection Properties related list.

<table id="table_xtl_vjd_d2c"><thead><tr><th>

Property

</th><th>

Description

</th><th>

Data source type

</th></tr></thead><tbody><tr><td>

include\_primary\_user\_details

</td><td>

Set the property to `true` to retrieve primary user details during import and add the assigned\_to attribute to the Configuration item \[cmdb\_ci\] table. Set the property to `false` to retrieve the enrolled user details.

Retrieving primary user details increases the time for importing data because of additional API calls.

**Note:** When a user is assigned to a device initially, the enrolled and primary users are the same. If the device is reassigned to another user, the primary user name is reassigned to the new user, but the enrolled user is still the original enrolled user name.

-   Type: true \| false
-   Default value: `true`

</td><td>

Regular data sources \(SG-Intune Computer, SG-Intune Devices, and SG-Intune Software\)

</td></tr><tr><td>

include\_ip\_address\_details

</td><td>

Set the property to `true` to retrieve IP address details during import and add the records to the IP Address \[cmdb\_ci\_ip\_address\] table.Set the property to `false` to skip retrieving IP addresses.

Retrieving IP addresses increases the time for importing data because of additional API calls.

-   Type: true \| false
-   Default value: `true`

</td><td>

Regular data sources \(SG-Intune Computer, SG-Intune Devices, and SG-Intune Software\)

</td></tr><tr><td>

api\_version

</td><td>

Enter the version of the Microsoft Intune Graph API.**Note:** This property is specific to the regular data sources \(SG-Intune Computer, SG-Intune Devices, and SG-Intune Software\).

-   Type: string
-   Default value: `v1.0`

</td><td>

Regular data sources \(SG-Intune Computer, SG-Intune Devices, and SG-Intune Software\)

</td></tr><tr><td>

software\_path

</td><td>

Set the path of the software code for finding apps and associated devices for regular data sources \(SG-Intune Computer, SG-Intune Devices, and SG-Intune Software\).Set the property to null value to enable the logic to determine the path of the software code.

-   Type: device \| app
-   Default value: `device`

</td><td>

Regular data sources \(SG-Intune Computer, SG-Intune Devices, and SG-Intune Software\)

</td></tr><tr><td>

device\_report\_chunks\_count

</td><td>

Set the number of device report chunks. The value must be a power of 16 \(1, 16, or 256\).-   Type: integer
-   Default value: `1`

</td><td>

Advanced data sources \(SG-Intune Device Reports and SG-Intune Software Reports\)

</td></tr><tr><td>

software\_report\_chunks\_count

</td><td>

Set the number of software report chunks. The value must be a power of 16 \(1, 16, or 256\).-   Type: integer
-   Default value: `16`

</td><td>

Advanced data sources \(SG-Intune Device Reports and SG-Intune Software Reports\)

</td></tr><tr><td>

export\_apis\_max\_calls\_before\_wait

</td><td>

Set the maximum number of API calls that can be made consecutively before a waiting period is enforced. -   Type: integer
-   Default value: `8`

</td><td>

Advanced data sources \(SG-Intune Device Reports and SG-Intune Software Reports\)

</td></tr><tr><td>

export\_apis\_wait\_time\_in\_ms

</td><td>

Set the duration \(in milliseconds\) for the waiting period after the specified number of consecutive API calls is reached.-   Type: integer
-   Default value: `120000`

</td><td>

Advanced data sources \(SG-Intune Device Reports and SG-Intune Software Reports\)

</td></tr></tbody>
</table>