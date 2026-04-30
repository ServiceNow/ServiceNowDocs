---
title: Service Graph Connector for Observability - Dynatrace properties
description: Service Graph Connector for Observability - Dynatrace properties control the behavior of the connector.
locale: en-US
release: xanadu
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: reference
last_updated: "2026-03-05"
reading_time_minutes: 3
breadcrumb: [Observability-Dynatrace, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Service Graph Connector for Observability - Dynatrace properties

Service Graph Connector for Observability - Dynatrace properties control the behavior of the connector.

## Connection properties

These connection properties are available for Service Graph Connector for Observability - Dynatrace.

**Note:** To open the Service Graph Connection Properties \[sn\_cmdb\_int\_util\_service\_graph\_connection\_property\] table for the connector, navigate to **All** &gt; **Service Graph Connectors** &gt; **Dynatrace Observability** &gt; **Connections** and select the connection name. The connection properties are displayed in the Service Graph Connection Properties related list.

<table id="table_tmg_rjm_lzb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

managementZoneIds

</td><td>

Enter a list of management zone IDs to fetch from Dynatrace. For multiple entries, separate the IDs with commas.

</td></tr><tr><td>

managementZoneNames

</td><td>

Enter a list of management zones to fetch from Dynatrace. For multiple entries, separate the names with commas.

</td></tr><tr><td>

tags

</td><td>

Enter a list of tags to fetch from Dynatrace. For multiple entries, separate the tags with commas.

</td></tr><tr><td>

grailEnabled

</td><td>

Set the property to `true` for a Grail-enabled tenant.

</td></tr><tr><td>

OAuth Connection

</td><td>

View the Sys ID of the OAuth connection and credential alias linked to the Service Graph connection record.

</td></tr><tr><td>

serviceTypes

</td><td>

Enter a list of Dynatrace service types from where to ingest the data into CMDB. For multiple entries, separate the service types with commas.Valid values are:

-   BACKGROUND\_ACTIVITY
-   CICS\_SERVICE
-   CUSTOM\_SERVICE
-   DATABASE\_SERVICE
-   ENTERPRISE\_SERVICE\_BUS\_SERVICE
-   EXTERNAL
-   IBM\_INTEGRATION\_BUS\_SERVICE
-   IMS\_SERVICE
-   MESSAGING\_SERVICE
-   QUEUE\_LISTENER\_SERVICE
-   RMI\_SERVICE
-   RPC\_SERVICE
-   WEB\_REQUEST\_SERVICE
-   WEB\_SERVICE

</td></tr><tr><td>

saveRESTResponseAsAttachment​

</td><td>

Set the property to `true` to use the SGO-Dynatrace Fetch Entities For Larger Payload action flow and save the response from Dynatrace as an attachment with a `.json` extension. ​​Set the property to `false` to use the dedicated action flow and consume the response from Dynatrace as a data stream for processing.​

-   Type: true \| false
-   Default value: `false`

</td></tr><tr><td>

flowDesignerTimeout

</td><td>

Set the timeout value \(in milliseconds\) for a Dynatrace flow, subflow, or action execution.-   Type: integer
-   Default value: `600000`

</td></tr></tbody>
</table>## System properties

These system properties are available for Service Graph Connector for Observability - Dynatrace.

**Note:** To open the System Properties \[sys\_properties\] table, enter `sys_properties.list` in the navigation filter.

<table id="table_w4t_nrm_jzb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_dynatrace\_integ.append\_environment\_id\_to\_service\_name

</td><td>

Set the property to `true` to append the Dynatrace Environment ID to the Service name. Set the property to `false` to retain the Service name as is. -   Type: true \| false
-   Default value: `false`
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

sn\_dynatrace\_integ.createUnmatchedApplicationCIs

</td><td>

Set the property to `true` to add unclassified processes to the Application \[cmdb\_ci\_appl\] table. Set the property to `false` to ignore unclassified processes.-   Type: true \| false
-   Default value: `true`
-   Location: System Property \[sys\_properties\] table

**Note:** Classified processes are added to the corresponding child application classes in the Application \[cmdb\_ci\_appl\] table regardless of the value of this property.

</td></tr><tr><td>

sn\_dynatrace\_integ.default\_from\_value\_days

</td><td>

Enter the number of days a configuration item \(CI\) can be inactive before it is ignored.-   Type: integer
-   Default value: `300`
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

sn\_dynatrace\_integ.page\_size

</td><td>

Enter the page size used in REST requests to fetch Dynatrace entities.-   Type: integer
-   Default value: `50`
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

sn\_dynatrace\_integ.populate\_applications

</td><td>

Set the property to `true` to populate the Application \[cmdb\_ci\_appl\] CIs from Dynatrace processes. Set the property to `false` to ignore the Application \[cmdb\_ci\_appl\] CIs. -   Type: true \| false
-   Default value: `false`
-   Location: System Property \[sys\_properties\] table

**Note:** This property is read via scheduled imports. The manual execution of the SGO-Dynatrace Processes and SGO-Dynatrace Process Groups data sources will not consider this property.

</td></tr><tr><td>

sn\_dynatrace\_integ.critical\_cluster\_threshold

</td><td>

Enter the percentage of an application cluster's nodes that need to be in a state to raise that state to its parent in the service map.**Note:** This system property is available only if the Observability Commons for CMDB \(sn\_observability\) plugin is installed. For more information, see [Observability Commons for CMDB](https://store.servicenow.com/sn_appstore_store.do#!/store/application/97e04562072020107add6a77c4a9351a) on the ServiceNow Store.

-   Type: integer
-   Default value: `75`
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

sn\_dynatrace\_integ.events\_for\_unmatched\_ci.enabled

</td><td>

Set the property to `true` to ingest events that don't have a matching CI in CMDB.**Note:** This system property is available only if the Observability Commons for CMDB \(sn\_observability\) plugin is installed. For more information, see [Observability Commons for CMDB](https://store.servicenow.com/sn_appstore_store.do#!/store/application/97e04562072020107add6a77c4a9351a) on the ServiceNow Store.

-   Type: true \| false
-   Default value: `false`
-   Location: System Property \[sys\_properties\] table

</td></tr></tbody>
</table>