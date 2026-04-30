---
title: Data mapping for Service Graph Connector for Infoblox
description: Data from the Infoblox data source is mapped and transformed into the ServiceNow CMDB configuration item \(CI\) class definitions using the Robust Transform Engine \(RTE\). Data is inserted into the ServiceNow CMDB using the Identification and Reconciliation Engine \(IRE\).
locale: en-US
release: zurich
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: reference
last_updated: "2026-03-03"
reading_time_minutes: 2
breadcrumb: [Infoblox, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Data mapping for Service Graph Connector for Infoblox

Data from the Infoblox data source is mapped and transformed into the ServiceNow CMDB configuration item \(CI\) class definitions using the Robust Transform Engine \(RTE\). Data is inserted into the ServiceNow CMDB using the Identification and Reconciliation Engine \(IRE\).

When you complete setting up the connection, you can configure the integration to pull data periodically from Infoblox. The data is loaded into staging tables and then inserted into the target tables.

The following table lists the data sources, the staging tables, and the target tables as CMDB CI and non-CMDB classes for Infoblox.

<table id="table_cg4_scb_m3c" class="custom-rows"><thead><tr><th class="filter">

Data source

</th><th>

Description

</th><th>

Staging table

</th><th>

Target tables

</th></tr></thead><tbody><tr><td>

SG-Infoblox IP Pool

</td><td>

Imports all the network containers from the Infoblox instance.**Note:** The SG-Infoblox IP Pool data source runs before the SG-Infoblox Network data source does.

</td><td>

SG-Infoblox IP Pool \[sn\_infoblox\_integ\_sg\_infoblox\_ip\_pool\]

</td><td>

[Managed IP Pool \[cmdb\_ci\_ip\_pool\]](sgc-cmdb-infoblox-classes.md#section_etk_zkg_fxb)

</td></tr><tr><td>

SG-Infoblox Network

</td><td>

Imports the IPv4 and IPv6 networks and subnets data from the Infoblox instance.**Note:** The SG-Infoblox Network data source runs after the SG-Infoblox IP Pool data source does.

</td><td>

SG-Infoblox Detailed Subnetwork \[sn\_infoblox\_integ\_sg\_infoblox\_detailed\_subnetwork\]

</td><td>

[Managed IP Network Subnet \[cmdb\_ci\_ip\_network\_subnet\]](sgc-cmdb-infoblox-classes.md#section_pmk_zkg_fxb)[Managed Network \[cmdb\_ci\_managed\_network\]](sgc-cmdb-infoblox-classes.md#section_xcl_zkg_fxb)

</td></tr><tr><td>

SG-Infoblox IP Address

</td><td>

Imports the IPv4 and IPv6 IP addresses from the Infoblox instance.**Note:** The SG-Infoblox IP Address data source runs after the SG-Infoblox Network data source does.

</td><td>

SG-Infoblox IP Address \[sn\_infoblox\_integ\_sg\_infoblox\_ip\_address\]

</td><td>

[Allocated IP Address \[cmdb\_ci\_allocated\_ip\_address\]](sgc-cmdb-infoblox-classes.md#section_c3g_zkg_fxb)[Managed IP Network Subnet \[cmdb\_ci\_ip\_network\_subnet\]](sgc-cmdb-infoblox-classes.md#section_pmk_zkg_fxb)

[Managed Network \[cmdb\_ci\_managed\_network\]](sgc-cmdb-infoblox-classes.md#section_xcl_zkg_fxb)

</td></tr><tr><td>

SG-Infoblox DNS Alias

</td><td>

Imports all the canonical name \(CNAME\) records from the Infoblox instance.

</td><td>

SG-Infoblox DNS Alias \[sn\_infoblox\_integ\_sg\_infoblox\_dns\_alias\]

</td><td>

[DNS Alias \[cmdb\_ci\_dns\_alias\]](sgc-cmdb-infoblox-classes.md#section_ypk_wmh_yxb)

</td></tr></tbody>
</table>For the SG-Infoblox IP Address data source, the [Detailed Subnetwork](sgc-cmdb-infoblox-classes.md#section_nlp_s44_nfc) \[sn\_infoblox\_integ\_sg\_infoblox\_detailed\_subnetwork\] table determines which IP addresses are imported based on the value of the **Get Ip Address** field.

A global default value can be set for the **Get Ip Address** option by setting the value of the **sn\_infoblox\_integ.default\_get\_ip\_address** system property in Service Graph Connector for Infoblox version 1.5.0 and later. Alternatively, you can update either the **sn\_infoblox\_integ.included\_network\_regex** system property to specify the list of IP addresses to be imported or the **sn\_infoblox\_integ.excluded\_network\_regex** system property to specify the list of IP addresses to be excluded from the import. For more information, see [Service Graph Connector for Infoblox properties](cmdb-sgc-infoblox-props.md).

For more information on where data is saved when pulling data from Infoblox, see [CMDB classes targeted in Service Graph Connector for Infoblox](sgc-cmdb-infoblox-classes.md).

You can use the IntegrationHub ETL app to view the data maps. See [IntegrationHub ETL](../concept/integrationhub-etl.md) for more information.

## Related content

[CMDB classes targeted in Service Graph Connector for Infoblox](sgc-cmdb-infoblox-classes.md)

[Service Graph Connector for Infoblox properties](cmdb-sgc-infoblox-props.md)

