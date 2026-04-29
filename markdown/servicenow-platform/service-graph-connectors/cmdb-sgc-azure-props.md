---
title: Service Graph Connector for Microsoft Azure properties
description: Service Graph Connector for Microsoft Azure properties control the behavior of the connector.
locale: en-US
release: australia
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Reference, Microsoft Azure, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Service Graph Connector for Microsoft Azure properties

Service Graph Connector for Microsoft Azure properties control the behavior of the connector.

## Connection properties

These connection properties are available for the Service Graph Connector for Microsoft Azure hardware connections.

**Note:** To open the Service Graph Connection Properties \[sn\_cmdb\_int\_util\_service\_graph\_connection\_property\] table for the connector, navigate to **All** &gt; **Service Graph Connectors** &gt; **Azure** &gt; **Connections**, and select the hardware connection name. The connection properties are displayed in the Service Graph Connection Properties related list.

<table id="table_sbd_lbl_c3c"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

vmGraphQuery

</td><td>

Specify the resource graph query on which the Run command should be executed. By default, the Run command is executed on all running VMs.-   Type: string
-   Default value: empty

</td></tr><tr><td>

filter\_databricks

</td><td>

This property is used to filter Azure Databricks CIs using the Vendor tag provided by Azure. Azure Databricks virtual machines \(VMs\), Network Interface Controllers \(NICs\), and storage volumes \(collectively called Azure Databricks CIs\) have the value of the Vendor tag set to `Databricks`.

Starting with the Service Graph Connector for Microsoft Azure 1.14.0 version, all Azure Databricks CIs that have the value of the Vendor tag set to `Databricks` are filtered out from discovery during a full data load.

During delta loads, set the value of the **insert\_short\_lived\_vms** custom system property to `false` to filter Azure Databricks CIs that are marked as retired during discovery \(see [Custom system properties](cmdb-sgc-azure-props.md#section_rrf_frg_23c)\). Additionally, for each Hardware connection, set the **filter\_databricks** connection property to `true`.

-   Type: true \| false
-   Default value: false

</td></tr><tr><td colspan="2">

Properties used for the Run command

</td></tr><tr><td>

scriptsContainerName

</td><td>

Enter the name of the container where the `.sh` and `.ps1` files are uploaded in Azure.-   Type: string
-   Default value: empty

</td></tr><tr><td>

storageAccountName

</td><td>

Enter the name of the storage account where the containers are created.-   Type: string
-   Default value: empty

</td></tr><tr><td>

storageSubsription

</td><td>

Enter the subscription ID where the storage account is created.-   Type: string
-   Default value: empty

</td></tr><tr><td>

storageContainerName

</td><td>

Enter the name of the container where the results of the commands are to be stored.-   Type: string
-   Default value: empty

</td></tr><tr><td>

storageResourceGroup

</td><td>

Enter the resource group of the storage account.-   Type: string
-   Default value: empty

</td></tr><tr><td>

powershellScriptURI

</td><td>

Enter the URI of the `.ps1` file that is to be run on Windows machines.-   Type: URI
-   Default value: empty

</td></tr><tr><td>

shellScriptURI

</td><td>

Enter the URI of the `.sh` file that is to be run on Linux machines.-   Type: URI
-   Default value: empty

</td></tr><tr><td>

lookback\_time\_in\_days

</td><td>

This property is used for record removal. Time in days in which the sys\_object\_source records are queried for the deletion of CIs. The value is automatically updated to 15 after the initial run.Set the value of this property to empty to include all the older records populated by SG-Azure as removal candidates for the Integration Commons record removal API.

**Note:** Do not modify this property if the value is empty.

-   Type: integer
-   Default value: empty

</td></tr></tbody>
</table>For more information about the Run command for the Service Graph Connector for Microsoft Azure, see [Instructions for setting up Run Command in Service Graph Connector for Azure \[KB2001668\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2001668)

## Default system properties

These default system properties are available for Service Graph Connector for Microsoft Azure.

**Note:** To open the System Properties \[sys\_properties\] table, enter `sys_properties.list` in the navigation filter.

<table id="table_w4t_nrm_jzb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_retry\_max

</td><td>

Enter the maximum retry limit for a Microsoft Azure API call made from the data sources within the connector.-   Type: integer
-   Default value: `3`
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

api\_retry\_max\_without\_backoff

</td><td>

Enter the maximum retry limit for a Microsoft Azure API call made from the data sources within the connector, without using exponential backoff to increase the waiting time between consecutive retries.-   Type: integer
-   Default value: `3`
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

azure\_full\_pull\_partition\_size

</td><td>

Set the partition size for Azure full data pull. This property determines the number of subscriptions that each partition processes. The value must be set to a numeric value greater than `0`.-   Type: integer
-   Default value: null
-   Location: System Property \[sys\_properties\] table

**Note:** If no value is specified, the property value is determined based on the number of active threads in the instance.

See [Set partition size for parallel loading-enabled Azure accounts](../task/sgc-azure-partition-size-prop.md).

</td></tr><tr><td>

delta\_grace\_time

</td><td>

Enter the additional time period in hours added to the current delta pull period when fetching incremental changes.-   Type: integer
-   Default value: `0`
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

delta\_page\_size

</td><td>

Enter the page size, that is, the maximum number of records fetched per page in a data pull for the data sources within the connector.-   Type: integer
-   Default value: `500`
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

is\_delta\_sync\_enabled

</td><td>

Set the property to `false` to deactivate delta synchronization.-   Type: true \| false
-   Default value: `false`
-   Location: System Property \[sys\_properties\] table

See [Configuring data synchronization in Service Graph Connector for Microsoft Azure](../concept/sgc-cmdb-azure-data-sync.md#).

</td></tr><tr><td>

LDC\_status

</td><td>

Set the property to `true` to enable populating the passive status of an Azure datacenter \(also known as a logical datacenter\) in the Comments attribute of the Azure Datacenter \[cmdb\_ci\_azure\_datacenter\] CI class when the `regionType` attribute is `Logical` or the service account for the datacenter is deactivated .-   Type: true \| false
-   Default value: `false`
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

load\_balancer\_page\_limit

</td><td>

Enter the maximum number of records per page to be fetched in a delta pull for the SG-Azure Load Balancers data source.-   Type: integer
-   Default value: `500`
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

maximum\_delta\_total\_period

</td><td>

Enter the maximum time period in days preceding the current run time during delta pull.-   Type: integer
-   Default value: `7`
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

maximum\_delta\_window\_period

</td><td>

Enter the maximum time duration in hours for each API call to repeat within the total delta period during delta pull.-   Type: integer
-   Default value: `24`
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

network\_interface\_page\_limit

</td><td>

Enter the maximum number of records per page to be fetched in a delta pull for the SG-Azure Network Interface data source.-   Type: integer
-   Default value: `500`
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

pull\_disabled\_subscriptions

</td><td>

Set the property to `false` to deactivate the import of resources associated with deactivated Azure subscriptions.-   Type: true \| false
-   Default value: `true`
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

save\_rest\_response\_as\_attachment

</td><td>

Set the property to `true` to save the response from Azure Resource Graph API calls as an attachment and read the data. Set this value to `true` if more than 10MB data is returned from Resource Graph API calls.-   Type: true \| false
-   Default value: `false`
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

security\_group\_page\_limit

</td><td>

Enter the maximum number of records per page to be fetched in a delta pull for the SG-Azure Security Group data source.-   Type: integer
-   Default value: `500`
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

software\_page\_limit

</td><td>

Enter the maximum number of records fetched per page when importing software data through the SG-Azure Software data source.-   Type: integer
-   Default value: `5000`
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

tcp\_and\_process\_page\_limit

</td><td>

Enter the maximum number of records fetched per page when importing TCP and running process data through the SG-Azure TCP data source.-   Type: integer
-   Default value: `1000`
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

tcp\_time\_period

</td><td>

Enter the time period in hours during which TCP and running process data is imported through the SG-Azure TCP data source.-   Type: integer
-   Default value: `1`
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

vm\_power\_state\_page\_limit

</td><td>

Enter the maximum number of records fetched per page when importing the power state of VMs through the SG-Azure VM Config Data data source.-   Type: integer
-   Default value: `1000`
-   Location: System Property \[sys\_properties\] table

</td></tr></tbody>
</table>## Custom system properties

You can create these custom system properties for the Service Graph Connector for Microsoft Azure. These properties must be created in the Service Graph Connector for Microsoft Azure application scope. The custom properties that you create are listed in the System Properties \[sys\_properties\] table.

For more information about creating custom system properties, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=australia&pubname=australia-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

<table id="table_r43_g5k_c3c"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_sg\_azure\_integ.network\_page\_limit

</td><td>

Set the maximum number of records per page to be fetched for the SG-Azure Network data source.-   Type: integer
-   Default value: `100`

</td></tr><tr><td>

sn\_sg\_azure\_integ.insert\_short\_lived\_vms

</td><td>

Set the property to `false` to filter out Azure Databricks CIs during delta loads.-   Type: true \| false
-   Default value: `true`
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

sn\_sg\_azure\_integ.sg\_azure\_generic\_resource\_type\_dynamic\_create

</td><td>

Set the value to `true` to add new resource types to the Service Graph Resource Inclusion Whitelist \[sn\_cmdb\_int\_util\_service\_graph\_resource\_inclusion\_whitelist\] table.-   Type: true \| false
-   Default value: `false`
-   Location: System Property \[sys\_properties\] table

</td></tr></tbody>
</table>## Related content

[Data mapping for Service Graph Connector for Microsoft Azure](cmdb-data-mapping-azure.md)

[CMDB classes targeted in Service Graph Connector for Microsoft Azure](cmdb-azure-classes.md)

**Parent Topic:**[Service Graph Connector for Microsoft Azure reference](../concept/sgc-azure-reference.md)

