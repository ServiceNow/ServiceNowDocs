---
title: Discovery for Microsoft Azure Cloud
description: If your cloud resources are in an Azure cloud, you must create a user identity called a service principal that grants permissions to the MID Server to access selected resources.
locale: en-US
release: yokohama
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Discovery for cloud environment, Discovery, ITOM Visibility, IT Operations Management]
---

# Discovery for Microsoft Azure Cloud

If your cloud resources are in an Azure cloud, you must create a user identity called a service principal that grants permissions to the MID Server to access selected resources.

## Azure management groups and subscriptions

An Azure management group contains other management groups and subscriptions. The management groups in an Azure Cloud environment form a hierarchy, but don’t contain volumes or virtual machines. Subscriptions contain cloud resources, such as virtual machines. The subscriptions that belong to management groups are called sub-accounts.

The advantages of using management groups are:

Easy population of sub-accounts

After you configure the management group and supply the necessary credentials, you can test the account. If the test succeeds, Discovery returns a list of subscriptions in that management group. From this list, you can choose one or more subscription sub-accounts to include in the Discovery schedule using the management group. For more information on the hierarchy of management groups and subscriptions, see [Organize your resources with Azure management groups](https://docs.microsoft.com/en-us/azure/governance/management-groups/overview)

Discovery of sub-account resources using dynamically acquired credentials

When you run Discovery on your subscriptions, you do not need separate credentials for each sub-account. Discovery finds the credentials for the management group and maps them to all of the subscription sub-accounts. The Cloud Discovery process handles credentials automatically by acquiring a temporary credential for each sub-account via an Azure API. You can elect to use the default configuration or customize the MID Server to assume other roles for additional controls and security. In addition, Discovery can automatically refresh the list of sub-accounts and datacenters covered in a discovery schedule. For more information, see the KB article [Retrieve newer accounts/sub-accounts automatically via Cloud Discovery.](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0961449)

A service principal for Azure cloud services is similar to a Microsoft Windows service account that enables Windows processes to communicate with each other within an Active Directory domain.

To create the Azure service principal in your ServiceNow instance, copy the service principal credential values from the Azure portal into a text editor, and then transfer those values into the instance.

![Text file that temporarily holds Azure service principal credential values](../image/azure-text-file.png "The text file that you generate during this procedure")

This table shows you the Azure Service Principal value and the location in Azure where you can find the values you need for the credentials.

|Cloud Provisioning and Governance setting|Azure Service Principal value|Location of the Azure value|
|-----------------------------------------|-----------------------------|---------------------------|
|Tenant ID|Azure **Directory ID** value from the text file.|**Azure Active Directory** &gt; **Properties** &gt; **Directory ID**|
|Client ID|Azure **Application ID** value from the text file.|**Azure Active Directory** &gt; **App registrations** &gt; **Registered App.Application ID**|
|Secret Key|Azure **Application key** value from the text file.|**Azure Active Directory** &gt; **App registrations** &gt; **Registered App** &gt; **Settings** &gt; **Keys \(hidden\)**|
|Account ID|Azure **Subscription ID** associated with the Tenant ID.|**Azure Active Directory** &gt; **Subscriptions** &gt; **Subscription ID**|

## Verify the REST API Permissions

Download the [Cloud Discovery patterns spreadsheet](https://downloads.docs.servicenow.com/resource/enus/api/servicenow-discovery-patterns-api-details.xlsx) so you can grant user permissions required for running the Discovery patterns. In addition to permissions, the spreadsheet also includes useful information such as pattern names, types, CI Classes, and links to vendor documentation. New patterns are available quarterly, so check periodically to be sure you have the latest version of the spreadsheet.

## Data collected by Service Mapping during top-down discovery

To include discovered components into service instances, enable CI relationships used in tag-based discovery by Service Mapping. These CI relationships are available from the 1.0.68 release on the ServiceNow Store. For operational steps, see [Tag-based discovery configuration](../../service-mapping/concept/tag_discovery_configuration.md).

Service Mapping uses tag-based discovery to create service instance maps including the Cloud components. The Service Mapping application comes with the following preconfigured CI relationships used for tag-based discovery. These CI relationships are available from the 1.0.68 release on the ServiceNow Store.

|CI|Relationship|CI|
|---|------------|---|
|Configuration Item \[cmdb\_ci\]|Hosted on::Hosts|Logical Datacenter \[cmdb\_ci\_logical\_datacenter\]|
|Logical Datacenter \[cmdb\_ci\_logical\_datacenter\]|Hosted on::Hosts|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|

## Azure Cloud Discovery API list

<table id="table_mr2_1qm_qmb"><tbody><tr><td>

CI Attributes

</td><td>

Azure Attributes

</td></tr><tr><td>

object\_id

</td><td>

response.name

</td></tr><tr><td>

name

</td><td>

response.name

</td></tr><tr><td>

region

</td><td>

response.displayName

</td></tr><tr><td>

status

</td><td>

Installed

</td></tr></tbody>
</table><table id="table_md1_hqm_qmb"><tbody><tr><td>

CI Attributes

</td><td>

Azure Attributes

</td></tr><tr><td>

object\_id

</td><td>

response.id

</td></tr><tr><td>

name

</td><td>

response.name

</td></tr><tr><td>

status

</td><td>

Installed/ Retired

</td></tr><tr><td>

state

</td><td>

 

</td></tr></tbody>
</table><table id="table_q1s_3qm_qmb"><tbody><tr><td>

CI Attributes

</td><td>

Azure Attributes

</td></tr><tr><td>

object\_id

</td><td>

id

</td></tr><tr><td>

name

</td><td>

name

</td></tr><tr><td>

state

</td><td>

available

</td></tr><tr><td>

status

</td><td>

Installed/ Retired

</td></tr></tbody>
</table><table id="table_c5j_jqm_qmb"><tbody><tr><td>

CI Attributes

</td><td>

Azure Attributes

</td></tr><tr><td>

object\_id

</td><td>

id

</td></tr><tr><td>

state

</td><td>

 

</td></tr><tr><td>

name

</td><td>

name

</td></tr><tr><td>

cidr

</td><td>

properties.addressSpace.addressPrefixes

</td></tr></tbody>
</table><table id="table_nfw_jqm_qmb"><tbody><tr><td>

CI Attributes

</td><td>

Azure Attributes

</td></tr><tr><td>

subnetName

</td><td>

response.name

</td></tr><tr><td>

subnetId

</td><td>

response.id

</td></tr><tr><td>

resourceGroup

</td><td>

response.properties.resourceGuid

</td></tr><tr><td>

networkId

</td><td>

response.id.split\('/subnets/'\)

</td></tr><tr><td>

networkName

</td><td>

getNetwork\(networkId\)

</td></tr><tr><td>

cidrBlock

</td><td>

response.properties.addressSpace.addressPrefixes

</td></tr></tbody>
</table><table id="table_i3l_kqm_qmb"><tbody><tr><td>

CI Attributes

</td><td>

Azure Attributes

</td></tr><tr><td>

state

</td><td>

properties.provisioningState

</td></tr><tr><td>

storage\_type

</td><td>

properties.BlobType

</td></tr><tr><td>

volume\_id

</td><td>

id

</td></tr><tr><td>

name

</td><td>

name

</td></tr><tr><td>

size\_bytes

</td><td>

properties.diskSizeGB \* 1024 \* 1024 \* 1024

</td></tr><tr><td>

object\_id

</td><td>

id

</td></tr><tr><td>

size

</td><td>

response.properties.diskSizeGB

</td></tr><tr><td>

"volume\_container"

</td><td>

containerName

</td></tr><tr><td>

status

</td><td>

Installed/ Retired

</td></tr></tbody>
</table><table id="table_wdg_lqm_qmb"><tbody><tr><td>

CI Attributes

</td><td>

Azure Attributes

</td></tr><tr><td>

object\_id

</td><td>

id

</td></tr><tr><td>

name

</td><td>

name

</td></tr><tr><td>

state

</td><td>

properties.provisioningState

</td></tr></tbody>
</table><table id="table_flf_mqm_qmb"><tbody><tr><td>

CI Attributes

</td><td>

Azure Attributes

</td></tr><tr><td>

memory

</td><td>

properties.hardwareProfile.vmSize

</td></tr><tr><td>

state

</td><td>

The instance statuses:-   succeeded: on
-   running: succeeded/stopping
-   deallocating: stopping/stopped
-   deallocated: off
-   terminated: error

</td></tr><tr><td>

object\_id

</td><td>

id

</td></tr><tr><td>

cpus

</td><td>

properties.hardwareProfile.vmSize

</td></tr><tr><td>

disks

</td><td>

properties.storageProfile.dataDisks

</td></tr><tr><td>

nics

</td><td>

properties.networkProfile.networkInterfaces\[\].size

</td></tr><tr><td>

vm\_inst\_id

</td><td>

properties.vmId

</td></tr><tr><td>

name

</td><td>

name

</td></tr><tr><td>

status

</td><td>

Installed/ Retired

</td></tr></tbody>
</table><table id="table_g25_mqm_qmb"><tbody><tr><td>

CI Attributes

</td><td>

Azure Attributes

</td></tr><tr><td>

name

</td><td>

name

</td></tr><tr><td>

object\_id

</td><td>

name

</td></tr><tr><td>

vcpus

</td><td>

numberOfCores

</td></tr><tr><td>

memory\_mb

</td><td>

memoryInMB

</td></tr><tr><td>

local\_storage\_gb

</td><td>

resourceDiskSizeInMB

</td></tr><tr><td>

cores

</td><td>

numberOfCores

</td></tr></tbody>
</table><table id="table_udj_nqm_qmb"><tbody><tr><td>

CI Attributes

</td><td>

Azure Attributes

</td></tr><tr><td>

object\_id

</td><td>

response.id

</td></tr><tr><td>

name

</td><td>

response.name

</td></tr><tr><td>

public\_dns

</td><td>

properties.dnsSettings.fqdn

</td></tr><tr><td>

public\_ip\_address

</td><td>

properties.ipAddress

</td></tr></tbody>
</table><table id="table_jkz_rqm_qmb"><tbody><tr><td>

CI Attributes

</td><td>

Azure Attributes

</td></tr><tr><td>

object\_id

</td><td>

"properties.frontendIPConfigurations.properties.privateIPAddress OR properties.frontendIPConfigurations.properties.publicIPAddress, then call Public IP Address API"

</td></tr><tr><td>

name

</td><td>

"properties.frontendIPConfigurations.properties.privateIPAddress OR properties.frontendIPConfigurations.properties.publicIPAddress, then call Public IP Address API"

</td></tr><tr><td>

ipaddress\_type

</td><td>

"properties.frontendIPConfigurations.properties.privateIPAddress ==&gt; Private IP Address OR properties.frontendIPConfigurations.properties.publicIPAddress ==&gt; Public IP Address"

</td></tr><tr><td>

status

</td><td>

Installed

</td></tr></tbody>
</table><table id="table_jrd_tqm_qmb"><tbody><tr><td>

CI Attributes

</td><td>

Azure Attributes

</td></tr><tr><td>

object\_id

</td><td>

id

</td></tr><tr><td>

name

</td><td>

name

</td></tr><tr><td>

private\_ip

</td><td>

properties.ipConfigurations

</td></tr><tr><td>

public\_dns

</td><td>

call public ip address api - properties.dnsSettings.fqdn

</td></tr><tr><td>

state

</td><td>

properties.provisioningState

</td></tr><tr><td>

is\_static

</td><td>

properties.ipConfigurations

</td></tr><tr><td>

mac\_address

</td><td>

properties.macAddress

</td></tr><tr><td>

public\_ip

</td><td>

call public ip address api -

</td></tr></tbody>
</table><table id="table_irp_wqm_qmb"><tbody><tr><td>

CI Attributes

</td><td>

Azure Attributes

</td></tr><tr><td>

name

</td><td>

response.id

</td></tr><tr><td>

object\_id

</td><td>

response.name

</td></tr><tr><td>

guest\_os

</td><td>

properties.storageProfile.osDisk.osType

</td></tr><tr><td>

image\_source

</td><td>

id

</td></tr><tr><td>

status

</td><td>

Installed/ Retired

</td></tr></tbody>
</table><table id="table_sf4_yqm_qmb"><tbody><tr><td>

CI Attributes

</td><td>

Azure Attributes

</td></tr><tr><td>

name

</td><td>

name

</td></tr><tr><td>

object\_id

</td><td>

id

</td></tr><tr><td>

sku\_name

</td><td>

sku.name

</td></tr><tr><td>

state

</td><td>

properties.provisioningState

</td></tr></tbody>
</table><table id="table_kcf_zqm_qmb"><tbody><tr><td>

CI Attributes

</td><td>

Azure Attributes

</td></tr><tr><td>

object\_id

</td><td>

response.id

</td></tr><tr><td>

name

</td><td>

response.name

</td></tr><tr><td>

state

</td><td>

 

</td></tr><tr><td>

dns\_name

</td><td>

properties.

</td></tr><tr><td>

fqdn

</td><td>

 

</td></tr><tr><td>

canonical\_hosted\_zone\_name

</td><td>

 

</td></tr></tbody>
</table>