---
title: Service Graph Connector for GCP properties
description: Service Graph Connector for GCP properties control the behavior of the connector.
locale: en-US
release: xanadu
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: reference
last_updated: "2026-03-06"
reading_time_minutes: 11
breadcrumb: [Reference, GCP, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Service Graph Connector for GCP properties

Service Graph Connector for GCP properties control the behavior of the connector.

## Connection properties

These connection properties are available for the Service Graph Connector for GCP.

**Note:** To open the Service Graph Connection Properties \[sn\_cmdb\_int\_util\_service\_graph\_connection\_property\] table for the connector, navigate to **All** &gt; **Service Graph Connectors** &gt; **GCP** &gt; **Connections**, and select the connection name. The connection properties are displayed in the Service Graph Connection Properties related list.

<table id="table_ad3_z3n_whc"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Organization Id

</td><td>

Enter the organization ID of the SG-GCP account.-   Type: integer
-   Default value: empty

</td></tr><tr><td>

Service Account

</td><td>

Service principal used by the Service Graph Connector for GCP to access the GCP organization, projects, and resources.

</td></tr><tr><td>

Discovery Scope

</td><td>

Enter the discovery scope of the SG-GCP account.-   Type: choice list
-   Default value: empty
-   Choices: organizations \| projects

</td></tr><tr><td>

JWT Provider

</td><td>

The JWT Provider sys\_id created for the SG-GCP connection. The value is automatically populated after the connection details are added.-   Type: string
-   Default value: empty

</td></tr><tr><td>

AppScript Folder IDs

</td><td>

Enter the GCP AppScript folder IDs as a comma-separated list to exclude the AppScript folders and projects information from being added to the CMDB during import.Automations are run on AppScript folders, which contain multiple projects that include meta information. AppScript folders don't contain any resources such as networks, subnets, and VMs.

-   Type: string
-   Default value: empty

</td></tr><tr><td colspan="2">

Properties used for soft deletion

</td></tr><tr><td>

Use Record Removal

</td><td>

This property is used for soft deletion and life cycle handling using the Integration Commons record removal API. The value is automatically updated to `true` after the initial run.**Note:** Do not modify this property.

-   Type: true \| false
-   Default value: true

For more information about soft deletion for the Service Graph Connector for GCP, see [Soft deletion](../concept/sgc-cmdb-gcp-removal.md#section_dgn_plz_ncc).

</td></tr><tr><td>

lookback\_time\_in\_days

</td><td>

This property is used for soft deletion. Time in days in which the sys\_object\_source records are queried for the soft deletion of CIs. The value is automatically updated to 15 after the initial run. Set the value of this property to empty to include all the older records populated by SG-GCP as removal candidates for soft deletion.

**Note:** Do not modify this property if the value is empty.

-   Type: integer
-   Default value: empty

For more information about soft deletion for the Service Graph Connector for GCP, see [Soft deletion](../concept/sgc-cmdb-gcp-removal.md#section_dgn_plz_ncc).

</td></tr><tr><td colspan="2">

Properties used for deep discovery

</td></tr><tr><td>

Shell Script Object Path

</td><td>

Enter the path to the `.sh` file uploaded to the cloud storage bucket.This property is required only when deep discovery is enabled. For more information, see [Deep discovery for Service Graph Connector for GCP](../concept/sgc-gcp-deep-discovery.md).

-   Type: string
-   Default value: empty

</td></tr><tr><td>

PowerShell Script Object Path

</td><td>

Enter the path to the `.ps1` file uploaded to the cloud storage bucket.This property is required only when deep discovery is enabled. For more information, see [Deep discovery for Service Graph Connector for GCP](../concept/sgc-gcp-deep-discovery.md).

-   Type: string
-   Default value: empty

</td></tr><tr><td>

PowerShell Script Generation Number

</td><td>

Enter the generation number for the `.ps1` file uploaded to the cloud storage bucket.This property is required only when deep discovery is enabled. For more information, see [Deep discovery for Service Graph Connector for GCP](../concept/sgc-gcp-deep-discovery.md).

-   Type: integer
-   Default value: empty

</td></tr><tr><td>

Shell Script Generation Number

</td><td>

Enter the generation number for the `.sh` file uploaded to the cloud storage bucket.This property is required only when deep discovery is enabled. For more information, see [Deep discovery for Service Graph Connector for GCP](../concept/sgc-gcp-deep-discovery.md).

-   Type: integer
-   Default value: empty

</td></tr><tr><td>

Scripts Bucket Name

</td><td>

Enter the name of the cloud storage bucket where the `.sh` and `.ps1` files are uploaded in Google Cloud Platform.This property is required only when deep discovery is enabled. For more information, see [Deep discovery for Service Graph Connector for GCP](../concept/sgc-gcp-deep-discovery.md).

-   Type: string
-   Default value: empty

</td></tr><tr><td>

Outputs Bucket Name

</td><td>

Enter the name of the cloudsn\_itom\_pattern.use a single hardware type for cloud data centers storage bucket provided in the `.sh` and `.ps1` files where the output of the commands are to be stored.This property is required only when deep discovery is enabled. For more information, see [Deep discovery for Service Graph Connector for GCP](../concept/sgc-gcp-deep-discovery.md).

-   Type: string
-   Default value: empty

</td></tr><tr><td>

Outputs Storage Path

</td><td>

Enter the folder path provided in the `.sh` and `.ps1` files where the output is uploaded in the cloud storage bucket.This property is required only when deep discovery is enabled. For more information, see [Deep discovery for Service Graph Connector for GCP](../concept/sgc-gcp-deep-discovery.md).

-   Type: string
-   Default value: empty

</td></tr></tbody>
</table>## Default system properties

These default system properties are available for the Service Graph Connector for GCP.

**Note:** To open the System Properties \[sys\_properties\] table, enter `sys_properties.list` in the navigation filter.

<table id="table_hsw_3jm_yhc"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_gcp\_integ.save\_rest\_response\_as\_attachment

</td><td>

Set this property to `true` to save the REST responses as attachments. Set this property to `false` if the payload size is less than 10 MB.-   Type: true \| false
-   Default value: `true`
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

sn\_gcp\_integ.sggcp\_config\_list\_discovered\_retry\_count

</td><td>

Set the retry count after a failure of the list APIs.-   Type: integer
-   Default value: `100`
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

sn\_gcp\_integ.sg\_gcp\_list\_folder\_page\_size

</td><td>

Set the page size for the list folder API response.-   Type: integer
-   Default value: `100`
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

sn\_gcp\_integ.sg\_gcp\_list\_project\_page\_size

</td><td>

Set the page size for the list project API response.-   Type: integer
-   Default value: `100`
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

sn\_gcp\_integ.sg\_gcp\_list\_resources\_page\_size

</td><td>

Set the page size for the list resources API response.-   Type: integer
-   Default value: `1000`
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

sn\_gcp\_integ.sg\_gcp\_generic\_resource\_type\_dynamic\_create

</td><td>

Set the value to `true` to add new resource types to the Service Graph Resource Inclusion Whitelist \[sn\_cmdb\_int\_util\_service\_graph\_resource\_inclusion\_whitelist\] table.-   Type: true \| false
-   Default value: `false`
-   Location: System Property \[sys\_properties\] table

</td></tr></tbody>
</table>## Custom system properties

You can create these custom system properties for the Service Graph Connector for GCP. These properties must be created in the Service Graph Connector for GCP application scope. The custom properties that you create are listed in the System Properties \[sys\_properties\] table.

For more information about creating custom system properties, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=xanadu&pubname=xanadu-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

<table id="table_ohm_3jm_yhc"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_gcp\_integ.add\_inherited\_tags

</td><td>

Option to populate the inherited tags of the parent resource.-   Type: true \| false
-   Default value: `true`

</td></tr><tr><td>

sn\_gcp\_integ.software\_chunk\_size

</td><td>

Enter the number of software records per computer batch. The value of this property can be reduced if the import row size leads to transformation errors.

 -   Type: integer
-   Default value: `100`

</td></tr><tr><td>

sn\_gcp\_integ.sg\_gcp\_software\_inventory\_batch\_size

</td><td>

Set the batch size of the API response for the SG-GCP Software Inventory data source. Specify a value between `1` and `100`.-   Type: integer
-   Default value: `100`

</td></tr><tr><td>

sn\_gcp\_integ.sg\_gcp\_cloud\_db\_batch\_size

</td><td>

Set the batch size of the API response for the SG-GCP Cloud Database data source. Specify a value between `1` and `100`.-   Type: integer
-   Default value: `100`

</td></tr><tr><td>

sn\_gcp\_integ.sg\_gcp\_cloud\_function\_batch\_size

</td><td>

Set the batch size of the API response for the SG-GCP Cloud Function data source. Specify a value between `1` and `100`.-   Type: integer
-   Default value: `100`

</td></tr><tr><td>

sn\_gcp\_integ.sg\_gcp\_kubernetes\_cluster\_batch\_size

</td><td>

Set the batch size of the API response for the SG-GCP Kubernetes Cluster data source. Specify a value between `1` and `100`.-   Type: integer
-   Default value: `100`

</td></tr><tr><td>

sn\_gcp\_integ.sg\_gcp\_kubernetes\_deployment\_batch\_size

</td><td>

Set the batch size of the API response for the SG-GCP Kubernetes Deployment data source. Specify a value between `1` and `100`.-   Type: integer
-   Default value: `100`

</td></tr><tr><td>

sn\_gcp\_integ.sg\_gcp\_kubernetes\_namespace\_batch\_size

</td><td>

Set the batch size of the API response for the SG-GCP Kubernetes Namespace data source. Specify a value between `1` and `100`.-   Type: integer
-   Default value: `100`

</td></tr><tr><td>

sn\_gcp\_integ.sg\_gcp\_kubernetes\_node\_batch\_size

</td><td>

Set the batch size of the API response for the SG-GCP Kubernetes Node data source. Specify a value between `1` and `100`.-   Type: integer
-   Default value: `100`

</td></tr><tr><td>

sn\_gcp\_integ.sg\_gcp\_kubernetes\_node\_pool\_batch\_size

</td><td>

Set the batch size of the API response for the SG-GCP Kubernetes Node Pool data source. Specify a value between `1` and `100`.-   Type: integer
-   Default value: `100`

</td></tr><tr><td>

sn\_gcp\_integ.sg\_gcp\_kubernetes\_cluster\_role\_batch\_size

</td><td>

Set the batch size of the API response for the SG-GCP Kubernetes Cluster Roles data source. Specify a value between `1` and `100`.-   Type: integer
-   Default value: `100`

</td></tr><tr><td>

sn\_gcp\_integ.sg\_gcp\_kubernetes\_cluster\_role\_binding\_batch\_size

</td><td>

Set the batch size of the API response for the SG-GCP Kubernetes Cluster Role Binding data source. Specify a value between `1` and `100`.-   Type: integer
-   Default value: `100`

</td></tr><tr><td>

sn\_gcp\_integ.sg\_gcp\_kubernetes\_pod\_batch\_size

</td><td>

Set the batch size of the API response for the SG-GCP Kubernetes Pod data source. Specify a value between `1` and `100`.-   Type: integer
-   Default value: `100`

</td></tr><tr><td>

sn\_gcp\_integ.sg\_gcp\_kubernetes\_replicaset\_batch\_size

</td><td>

Set the batch size of the API response for the SG-GCP Kubernetes Replicaset data source. Specify a value between `1` and `100`.-   Type: integer
-   Default value: `100`

</td></tr><tr><td>

sn\_gcp\_integ.sg\_gcp\_kubernetes\_service\_batch\_size

</td><td>

Set the batch size of the API response for the SG-GCP Kubernetes Service data source. Specify a value between `1` and `100`.-   Type: integer
-   Default value: `100`

</td></tr><tr><td>

sn\_gcp\_integ.sg\_gcp\_lb\_health\_service\_batch\_size

</td><td>

Set the batch size of the API response for the SG-GCP Load Balancer Health Service data source. Specify a value between `1` and `100`.-   Type: integer
-   Default value: `100`

</td></tr><tr><td>

sn\_gcp\_integ.sg\_gcp\_lb\_pool\_batch\_size

</td><td>

Set the batch size of the API response for the SG-GCP Load Balancer Pool data source. Specify a value between `1` and `100`.-   Type: integer
-   Default value: `100`

</td></tr><tr><td>

sn\_gcp\_integ.sg\_gcp\_lb\_pool\_member\_batch\_size

</td><td>

Set the batch size of the API response for the SG-GCP Load Balancer Pool Member data source. Specify a value between `1` and `100`.-   Type: integer
-   Default value: `100`

</td></tr><tr><td>

sn\_gcp\_integ.sg\_gcp\_lb\_service\_batch\_size

</td><td>

Set the batch size of the API response for the SG-GCP Load Balancer Service data source. Specify a value between `1` and `100`.-   Type: integer
-   Default value: `100`

</td></tr><tr><td>

sn\_gcp\_integ.sg\_gcp\_load\_balancer\_batch\_size

</td><td>

Set the batch size of the API response for the SG-GCP Load Balancer data source. Specify a value between `1` and `100`.-   Type: integer
-   Default value: `100`

</td></tr><tr><td>

sn\_gcp\_integ.sg\_gcp\_network\_batch\_size

</td><td>

Set the batch size of the API response for the SG-GCP Network data source. Specify a value between `1` and `100`.-   Type: integer
-   Default value: `100`

</td></tr><tr><td>

sn\_gcp\_integ.sg\_gcp\_object\_storage\_batch\_size

</td><td>

Set the batch size of the API response for the SG-GCP Cloud Object Storage data source. Specify a value between `1` and `100`.-   Type: integer
-   Default value: `100`

</td></tr><tr><td>

sn\_gcp\_integ.sg\_gcp\_security\_group\_batch\_size

</td><td>

Set the batch size of the API response for the SG-GCP Security Group data source. Specify a value between `1` and `100`.-   Type: integer
-   Default value: `100`

</td></tr><tr><td>

sn\_gcp\_integ.sg\_gcp\_storage\_volume\_batch\_size

</td><td>

Set the batch size of the API response for the SG-GCP Storage Volume data source. Specify a value between `1` and `100`.-   Type: integer
-   Default value: `100`

</td></tr><tr><td>

sn\_gcp\_integ.sg\_gcp\_storage\_vol\_snapshot\_batch\_size

</td><td>

Set the batch size of the API response for the SG-GCP Storage Volume Snapshot data source. Specify a value between `1` and `100`.-   Type: integer
-   Default value: `100`

</td></tr><tr><td>

sn\_gcp\_integ.sg\_gcp\_subnet\_batch\_size

</td><td>

Set the batch size of the API response for the SG-GCP Subnet data source. Specify a value between `1` and `100`.-   Type: integer
-   Default value: `100`

</td></tr><tr><td>

sn\_gcp\_integ.sg\_gcp\_vm\_instance\_batch\_size

</td><td>

Set the batch size of the API response for the SG-GCP VM Instance data source. Specify a value between `1` and `100`.-   Type: integer
-   Default value: `100`

</td></tr><tr><td>

sn\_gcp\_integ.sg\_gcp\_machine\_image\_batch\_size

</td><td>

Set the batch size of the API response for the SG-GCP Machine Image data source. Specify a value between `1` and `100`.-   Type: integer
-   Default value: `100`

</td></tr><tr><td>

sn\_gcp\_integ.sg\_gcp\_list\_generic\_resource\_page\_size

</td><td>

Set the page size for the list generic resource API response. Specify a value between `1` and `1000`.-   Type: integer
-   Default value: `1000`

</td></tr><tr><td>

sn\_gcp\_integ.sg\_gcp\_list\_annotation\_resource\_page\_size

</td><td>

Set the page size for the list annotation resource API response. Specify a value between `1` and `1000`.-   Type: integer
-   Default value: `1000`

</td></tr><tr><td>

sn\_sg\_gcp\_integ.min\_retry\_wait\_time

</td><td>

Set the minimum wait time \(in milliseconds\) before retrying after an API failure due to throttling or rate limiting issues.-   Type: integer
-   Default value: `10,000`

</td></tr><tr><td>

sn\_sg\_gcp\_integ.max\_retry\_wait\_time

</td><td>

Set the maximum waiting period \(in milliseconds\) after an API failure due to throttling or rate limiting issues.-   Type: integer
-   Default value: `160,000`

</td></tr></tbody>
</table>**Parent Topic:**[Service Graph Connector for GCP reference](../concept/sgc-cmdb-gcp-reference.md)

**Related topics**  


[Data mapping for Service Graph Connector for GCP](cmdb-data-mapping-gcp.md)

[CMDB classes targeted in Service Graph Connector for GCP](sgc-cmdb-gcp-classes.md)

[Deep discovery for Service Graph Connector for GCP](../concept/sgc-gcp-deep-discovery.md)

[Record removal process in Service Graph Connector for GCP](../concept/sgc-cmdb-gcp-removal.md)

