---
title: Service Graph Connector for Dynatrace SaaS properties
description: Service Graph Connector for Dynatrace SaaS properties control the behavior of the connector.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/servicenow-platform/service-graph-connectors/sgc-dynatrace-saas-properties.html
release: zurich
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: reference
last_updated: "2026-07-07"
reading_time_minutes: 2
breadcrumb: [Observability - Dynatrace SaaS, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Service Graph Connector for Dynatrace SaaS properties

Service Graph Connector for Dynatrace SaaS properties control the behavior of the connector.

## Connection properties

These connection properties are available for the Service Graph Connector for Dynatrace SaaS.

**Note:** To open the Service Graph Connection Properties \[sn\_cmdb\_int\_util\_service\_graph\_connection\_property\] table for the connector, navigate to **All** &gt; **Service Graph Connectors** &gt; **Dynatrace SaaS** &gt; **Connections** and select the connection name. The connection properties are displayed in the Service Graph Connection Properties related list.

<table id="table_conn_props_observability-dynatrace-saas"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

data\_fetch\_flow\_action\_timeout\_ms

</td><td>

Maximum time \(in milliseconds\) allowed for the connection’s Fetch Dynatrace SaaS Data flow designer action to run while calling Dynatrace API endpoints and loading results into ServiceNow source tables. If the action exceeds this limit, execution is terminated to prevent long‑running or stalled runs.Default value: `600000` \(10 minutes\)

</td></tr><tr><td>

initial\_dynatrace\_data\_fetch\_days

</td><td>

Specify the number of days for which data is fetched from Dynatrace when the connection runs for the first time or when **last\_run\_datetime** is empty. Default value: `7`

</td></tr><tr><td id="entry_dnf_1jj_njc">

service\_to\_service\_relationships\_enabled

</td><td>

Set this property to `true` to create upstream and downstream relationships between Dynatrace Service CIs \(service-to-service\).When this property is set to `false`, upstream and downstream service-to-service relationships aren't created for the connection.

Default value: `true`

</td></tr><tr><td id="entry_bhr_fjj_njc">

append\_tenant\_id\_to\_service\_name

</td><td>

Set this property to `true` to append the Dynatrace tenant ID to the Calculated Service names to maintain unique names across multiple Dynatrace connections.When this property is set to `false`, Calculated Service names are created without the Dynatrace tenant ID.

Default value: `false`

</td></tr><tr id="row_r42_t3j_njc"><td id="entry_isz_t3j_njc">

dynatrace\_api\_batch\_size

</td><td>

Specify the maximum number of records to be returned per Dynatrace API request. This property controls pagination for Dynatrace data fetch operations.Lower values might reduce the payload size but increase the number of API calls, while higher values might improve performance but increase the payload size.

Default value: `50`

</td></tr><tr id="row_rkx_j33_vjc"><td>

dynatrace\_classic\_connection\_alias\_sys\_id

</td><td>

Connection alias sys\_id from the Dynatrace Classic connector \(SGO-Dynatrace\). When this property is set, the connector performs a one-time cleanup of stale process CIs originally created by the classic connector.Leave the value field empty to skip classic migration cleanup.

Default value: empty

</td></tr><tr><td>

segment\_id

</td><td>

Specify the Dynatrace segment ID to be used for filtering entities. When a value is specified, only entities that belong to the specified segment are imported.**Note:** Only one segment ID can be specified.

If no value is specified, no segment filter is applied, and all entities are imported.

Default value: empty

</td></tr><tr id="row_kyc_xh3_vjc"><td>

ci\_retirement\_threshold\_days

</td><td>

Number of days to wait before retiring a CI that is no longer reported by Dynatrace. Configuration items that aren't seen for longer than this period are soft‑retired by setting their operational status to non‑operational.Default value: `35 days`

</td></tr></tbody>
</table>## System property

The following system property is available for the Service Graph Connector for Dynatrace SaaS.

**Note:** To open the System Properties \[sys\_properties\] table, enter `sys_properties.list` in the navigation filter.

<table id="table_sys_props_observability-dynatrace-saas"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_dynatrace\_saas.createUnmatchedApplicationCIs

</td><td>

Set this property to `true` to import all the unmatched running process records into the Applications table.-   Type: string
-   Default value: `true`
-   Location: System Property \[sys\_properties\] table

</td></tr></tbody>
</table>