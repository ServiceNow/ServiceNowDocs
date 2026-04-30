---
title: Microsoft Azure Cloud discovery using patterns
description: Discovery uses multiple patterns to discover components of the Microsoft Azure Cloud deployment during horizontal discovery. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: zurich
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2025-11-26"
reading_time_minutes: 27
keywords: [Patterns, Azure, Cloud, Discovery]
breadcrumb: [Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Microsoft Azure Cloud discovery using patterns

Discovery uses multiple patterns to discover components of the Microsoft Azure Cloud deployment during horizontal discovery. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Request new or enhanced Patterns on the ServiceNow® Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/application/06a71b1367e4130051c9027e2685ef1e/1.6.0?referer=%2Fstore%2Fsearch%3Flistingtype%3Dallintegrations%25253Bancillary_app%25253Bcertified_apps%25253Bcontent%25253Bindustry_solution%25253Boem%25253Butility%25253Btemplate%26q%3DPatterns&sl=sh) to view all the available updates and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Prerequisites

-   **Verify that the applications are up to date.**
    -   Discovery and Service Mapping Patterns
    -   CMDB CI Class Models
    -   Visibility Content
-   **Activate the cloud-related CI relationships**

    To include discovered components into service instances, enable CI relationships used in tag-based discovery by Service Mapping. These CI relationships are available from the 1.0.68 release on the ServiceNow Store. For operational steps, see [Tag-based discovery configuration](../concept/tag_discovery_configuration.md).

-   **Azure Availability Set**

    Wait for the **Clean-Up job for Availability zone to clear availability set record** schedule job to delete all the pre-populated availability set's Configuration Items \(CI\) in the **cmdb\_ci\_azure\_availability\_set** table.

-   **Azure Availability Zone**

    To run a discovery with Azure Availability Zone, register the subscription ID to the **AvailabilityZonePeering** feature with AZ CLI using `az feature register -n AvailabilityZonePeering --namespace Microsoft.Resources` to use the Check Zone Peering API. Check the status with `az feature show -n AvailabilityZonePeering --namespace Microsoft.Resources` before running discovery.

-   **Set up Azure service accounts**

    Enable Cloud Discovery to access your Azure environment. For more information, see [Set up Azure service accounts](../../it-operations-management/task/setup-azure-service-accounts.md).

-   **Create an Azure cloud discovery schedule**

    For more information, see [Create an Azure Discovery schedule in Discovery Admin Workspace](../../discovery/task/create-azure-schedule-DAW.md).

-   **\(Optional\) Discover datacenters only for new subscriptions**

    Starting with Zurich Patch 2, you can discover datacenters only for new subscriptions added since the last discovery. For more information, see [Discover datacenters only for new cloud accounts](../task/discover-datacenter-only-new-account.md).

-   **\(Optional\) Populate Service Account and Logical Datacenter fields in cloud CIs**

    Starting with Discovery and Service Mapping Patterns version 1.30.2, you can improve query performance by populating Service Account and Logical Datacenter fields directly in cloud CIs. For more information, see [Improved query performance with direct field population in CI tables](../concept/query-service-account-ldc-fields.md).


## Verify the REST API Permissions

Download the [Cloud Discovery patterns spreadsheet](https://downloads.docs.servicenow.com/resource/enus/api/servicenow-discovery-patterns-api-details.xlsx) so you can grant user permissions required for running the Discovery patterns. In addition to permissions, the spreadsheet also includes useful information such as pattern names, types, CI Classes, and links to vendor documentation. New patterns are available quarterly, so check periodically to be sure you have the latest version of the spreadsheet.

## Azure resources discovery by datacenters

Azure has multiple datacenters around the world, but resources like load balancers and virtual machines are typically deployed in only some of them. The **Azure Datacenter Discovery** pattern executes before all other Azure patterns to identify the datacenters that have resources related to your service account \("active"\) and the datacenters that don't have your resources \("passive"\). This model improves the performance of the Azure discovery. This execution model is more efficient than the previous one, in which all datacenters were discovered regardless of having relevant resources in them.

After identifying the "active" and "passive" datacenters, the Discovery schedule continues to execute all Azure patterns only for the "active" datacenters, to discover your Azure cloud resources. The "passive" datacenters are ignored while running the schedule.

You might notice differences in Azure discovery log, in discovery time and in the CMDB, depending on the service account and MID Server property settings.

Datacenters that have already been discovered before the upgrade to Discovery and Service Mapping Patterns version 1.15.0, remain in the **Azure Datacenters** table. However, the discovery runtime behavior is now determined by the value of the MID Server property **mid.cloud.discovery.sonar.discover\_all\_azure\_datacenters**. The property is set to **false** by default, to limit the discovery execution to the "active" datacenters, rather than all datacenters. You can discover all datacenters for a service account, including "passive" ones, by setting the property to **true**. For more information, see: [Create a MID Server property](https://www.servicenow.com/docs/access?context=r_MIDServerProperties&version=zurich&pubname=zurich-servicenow-platform&section=t_SetMIDServerProperties&ft:locale=en-US).

If the MID Server property is set to **false**, the Azure Datacenters table shows only active datacenters. All other behaviors remain unchanged from previous Discovery and Service Mapping Patterns versions.

|Discovery and Service Mapping Patterns version|MID Server property setting|Discovered datacenters|Datacenters contained in Azure Datacenters table|Datacenters displayed in discovery log|
|----------------------------------------------|---------------------------|----------------------|------------------------------------------------|--------------------------------------|
|Discovery and Service Mapping Patterns starting with version 1.15.0|False \(default\)|Active only|Active only|Active only|
|Discovery and Service Mapping Patterns starting with version 1.15.0|True|All datacenters|All datacenters|All datacenters|
|Discovery and Service Mapping Patterns before version 1.15.0|False \(default\)|Active only|All datacenters|Active only|
|Discovery and Service Mapping Patterns before version 1.15.0|True|All datacenters|All datacenters|All datacenters|

For management groups, Azure Cloud Discovery discovers all Azure datacenters.

Starting with Discovery and Service Mapping Patterns version 1.29.0, the **Refresh Datacenters** flow displays all regions, not just active ones. You don’t need to create another schedule when a resource is added or a datacenter switches from passive to active.

## Azure Hardware Type discovery

Hardware Type discovery has undergone three model changes in recent years. The 1.15.0 model triggers the **Hardware Type** pattern and the **Virtual Machine** pattern after the **Azure Datacenter Discovery** pattern. Starting Discovery and Service Mapping Patterns plugin version 1.15.0, Cloud Discovery identifies which Hardware Type model is used, and launches only one of the two patterns: **Hardware Type \(LP\)** or **Cloud Hardware Type \(LP\)**.

<table id="table_gml_tkv_1bc"><thead><tr><th>

Discovery and Service Mapping Patterns version

</th><th>

Hardware Type Migration status

</th><th>

Which pattern executes

</th><th>

Discovery result

</th></tr></thead><tbody><tr><td>

Prior to 1.0.75

</td><td>

Haven't migrated to the new model

</td><td>

**Hardware Type \(LP\)** pattern

</td><td>

The CI type created: \[cmdb\_ci\_compute\_template\]

</td></tr><tr><td>

Discovery and Service Mapping Patterns version 1.0.75

</td><td>

The migration to the new model is done by migration script. See [KB0955939](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0955939)

</td><td>

**Hardware Type \(LP\)** pattern

</td><td>

The CI type created: \[cmdb\_ci\_cloud\_hardware\_type\]

</td></tr><tr><td>

Discovery and Service Mapping Patterns version 1.6.0

</td><td>

The Hardware Type new model is provided OOB, enabled with the system property: **sn\_itom\_pattern.use a single hardware type for cloud datacenters**. For more information, see[KB1285337](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1285337).

</td><td>

According to [KB1285337](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1285337) Flow Diagram

</td><td>

The CI type created: According to [KB1285337](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1285337)

</td></tr><tr><td>

Discovery and Service Mapping Patterns 1.15.0

</td><td>

The Hardware Type new model is provided OOB enabled with the system property: **sn\_itom\_pattern.use a single hardware type for cloud datacenters**. For more information, see[KB1285337](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1285337).

</td><td>

The flow is as described in [KB1285337](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1285337). However, only one pattern executes. The pattern that used to gracefully terminate doesn't execute.

</td><td>

Either **Hardware Type \(LP\)** pattern or **Cloud Hardware Type \(LP\)** pattern executes.

</td></tr></tbody>
</table>## Azure SQL Managed Instance license discovery

The Azure DataBase \(LP\) pattern extension **Azure SQL Managed Instance license** discovers Azure SQL Managed Instance license information and populates the license type in the Key Value \[cmdb\_key\_value\] table of Cloud Database CI \[cmdb\_ci\_cloud\_database\].

-   **Required plugins and applications**
    -   Software Asset Management Professional for Microsoft
    -   Visibility Content
-   **Discovered resources and relationships**

    [Resources discovered using the Azure DataBase \(LP\) pattern extension: Azure SQL Managed Instance license](azure-cloud-discovery-patterns.md#resources-azure-sql-managed-instance-license)

    [Relationships discovered using the Azure DataBase \(LP\) pattern extension: Azure SQL Managed Instance license](azure-cloud-discovery-patterns.md#relationships-azure-sql-managed-instance-license)


## Azure Marketplace discovery

The Azure - Marketplace LB \(LP\) pattern discovers the following Azure Marketplace products:

-   SaaS
-   Azure Application
-   Virtual Machine

    **Note:** The pattern discovers only virtual machines \(VMs\) created from third-party or commercial marketplace images.


-   **Discovered resources and relationships**

    [Resources discovered by the Azure - Marketplace LB \(LP\) pattern](azure-cloud-discovery-patterns.md#resources-azure-marketplace)

    [Relationships discovered using the Azure - Marketplace LB \(LP\) pattern](azure-cloud-discovery-patterns.md#relationships-azure-marketplace)


## Data collected by Discovery during horizontal discovery

-   **Resources discovered by the Microsoft Azure - Application LB \(LP\) pattern**

    |Field|Description|
    |-----|-----------|
    |Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer​\]|
    |object\_id|A unique identifier, allocated by Microsoft Azure for this resource.|
    |name|The Name or ID if no Name is specified for the load balancer.|
    |location|The path of the load balancer.|
    |state|The current state of the load balancer.|
    |install\_status|Resource provisioning status.|
    |ip\_address​|IP Address of the load balancer.|
    |fqdn|The fully qualified domain name of the load balancer.|
    |dns\_name|The DNS name of the load balancer.|
    |comments|Identifier for internal usage \(deletion strategy\).|
    |Cloud LB IP Address \[cmdb\_ci\_cloud\_lb\_ipaddress\]|
    |object\_id​|A unique identifier, allocated by Microsoft Azure for this resource.|
    |lb\_id​|A unique identifier for the load balancer.|
    |ip\_address​|IP address of the load balancer.|
    |ip\_address\_type|The type of the IP Address, which can be private or public.|
    |fqdn|The fully qualified domain name of the load balancer.|
    |comments|Identifier for internal usage \(deletion strategy\).|
    |install\_status​|Resource provisioning status.|
    |Load Balancer Pool \[cmdb\_ci\_lb\_pool​\]|
    |object\_id​|A unique identifier, allocated by Microsoft Azure for this resource.|
    |name|The Name or ID if no Name is specified for the load balancer pool.|
    |location|Path of the load balancer pool.|
    |install\_status​|Resource provisioning status.|
    |comments|Identifier for internal usage \(deletion strategy\).|
    |Load Balancer Service \[cmdb\_ci\_lb\_service\]|
    |object\_id​|A unique identifier, allocated by Microsoft Azure for this resource.|
    |name|The Name or ID if no Name is specified for the load balancer service.|
    |location|Path of the load balancer service.|
    |port|The TCP port that the load balancer service listens to.|
    |install\_status|Resource provisioning status.|
    |comments|Identifier for internal usage \(deletion strategy\).|

-   **Resources discovered by the Microsoft Azure - Network and Subnet \(LP\) pattern**

    |Field|Description|
    |-----|-----------|
    |Cloud Network \[cmdb\_ci\_network\]|
    |object\_id​|A unique identifier, allocated by Microsoft Azure for this resource.|
    |name|The Name or ID if no Name is specified for the cloud network.|
    |location|Path of the network.|
    |state|The current state of the network.|
    |install\_status​|Resource provisioning status.|
    |cidr|CIDR representation of the network. For example, 10.0.0.0/24.|
    |Cloud Subnet \[cmdb\_ci\_cloud\_subnet​\]|
    |object\_id​|A unique identifier, allocated by Microsoft Azure for this resource.|
    |name|The Name or ID if no Name is specified for the cloud subnet.|
    |location|Identifier for internal usage \(deletion strategy\).|
    |state|The current state of the subnet.|
    |install\_status|Resource provisioning status.|
    |cidr|CIDR representation of the subnet. For example, 10.0.0.0/24.|

-   **Resources discovered by the Microsoft Azure - NIC \(LP\) pattern**

    |Field|Description|
    |-----|-----------|
    |Cloud Mgmt Network Interface \[cmdb\_ci\_nic\]|
    |object\_id​|A unique identifier, allocated by Microsoft Azure for this resource.|
    |name|The Name or ID if no Name is specified for the network interface.|
    |location|Path of the network interface.|
    |install\_status|Resource provisioning status.|
    |state|The current state of the network interface.|
    |public\_ip|The address of the Elastic IP address bound to the network interface.|
    |private\_ip​|The IPv4 address of the network interface within the subnet.|
    |primary|True/False. Defines if the network interface is the primary network interface or not.|
    |mac\_address|The MAC address of the network interface.|
    |public\_dns​|The public DNS name of the network interface.|

-   **Resources discovered by the Microsoft Azure - Private Gateway \(LP\) pattern**

    |Field|Description|
    |-----|-----------|
    |Virtual Private Gateway \[cmdb\_ci\_virtual\_pvt\_gateway\]|
    |object\_id​|A unique identifier, allocated by Microsoft Azure for this resource.|
    |name|The Name or ID if no Name is specified for the private gateway.|
    |location|Path of the private gateway.|
    |connection\_type|Type of VPN connection the gateway supports.|
    |operational\_status|The state of the resource.|
    |install\_status​|Resource provisioning status.|
    |Virtual Private Gateway Endpoint \[cmdb\_ci\_endpoint\_vpg\]|
    |object\_id​|A unique identifier, allocated by Microsoft Azure for this resource.|
    |name|The Name or ID if no Name is specified for the endpoint.|
    |location|Path of the endpoint.|
    |connection\_type​|Type of VPN connection the gateway supports.|

-   **Resources discovered by the Microsoft Azure - Public IP \(LP\) pattern**

    |Field|Description|
    |-----|-----------|
    |Cloud Public IP Address \[cmdb\_ci\_cloud\_public\_ipaddress\]|
    |object\_id​|A unique identifier, allocated by Microsoft Azure for this resource.|
    |name|The Name or ID if no Name is specified for the IP address.|
    |location|Path of the IP address.|
    |state|The current state of the IP address.|
    |public\_ip\_address|The address of the Elastic IP address.|
    |public\_dns​|The public DNS name.|
    |install\_status|Resource provisioning status.|

-   **Resources discovered by the Microsoft Azure - Resource Group \(LP\) pattern**

    |Field|Description|
    |-----|-----------|
    |Resource Group \[cmdb\_ci\_resource\_group\]|
    |object\_id|A unique identifier, allocated by Microsoft Azure for this resource.|
    |name|The Name or ID if no Name is specified for the resource group.|
    |location|Path of the resource group.|
    |state|The current state of the resource group.|
    |install\_status​|Resource provisioning status.|

-   **Resources discovered by the Microsoft Azure - Route Table \(LP\) pattern**

    |Field|Description|
    |-----|-----------|
    |Route Table \[cmdb\_ci\_route\_table\]|
    |object\_id​|A unique identifier, allocated by Microsoft Azure for this resource.|
    |name|The Name or ID if no Name is specified for the route table.|
    |location|Path of the route table.|
    |install\_status|Resource provisioning status.|
    |state|The current state of the route table.|

-   **Resources discovered by the Microsoft Azure - Security Group \(LP\) pattern**

    |Field|Description|
    |-----|-----------|
    |Compute Security Group \[cmdb\_ci\_compute\_security\_group​\]|
    |object\_id​|A unique identifier, allocated by Microsoft Azure for this resource.|
    |name|The Name or ID if no Name is specified for the security group.|
    |location|Path of the security group.|
    |state|The current state of the security group.|
    |install\_status|Resource provisioning status.|

-   **Resources discovered by the Microsoft Azure - SQL Server \(LP\) pattern**

    |Field|Description|
    |-----|-----------|
    |Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|
    |object\_id​|A unique identifier, allocated by Microsoft Azure for this resource.|
    |location|Path of the VM instance.|

<table id="table_x1d_tw1_23c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Key \[key\]

</td><td>

Server\_License\_Type\_automatic

</td></tr><tr><td>

Value \[value\]

</td><td>

The value is one of the following options: -   Azure Hybrid Benefit: **BYOL**
-   Pay-as-you-go licensing: **License Included**


</td></tr><tr><td>

Configuration item \[configuration\_item\]

</td><td>

References the Virtual Machine Instance \[cmdb\_ci\_vm\_instance\] table.

</td></tr></tbody>
</table>-   **Resources discovered by the Microsoft Azure - Storage Account \(LP\) pattern**

    |Field|Description|
    |-----|-----------|
    |Cloud Storage Account \[cmdb\_ci\_cloud\_storage\_account\]|
    |object\_id​|A unique identifier, allocated by Microsoft Azure for this resource.|
    |name|The Name or ID if no Name is specified for the storage account.|
    |location|Path of the storage account.|
    |sku\_name|The name of the SKU \(for backup frequency\).|
    |install\_status​|Resource provisioning status.|
    |state|The current state of the storage account.|

-   **Resources discovered by the Microsoft Azure - Storage Containers \(LP\) pattern**

    |Field|Description|
    |-----|-----------|
    |Storage Volume \[cmdb\_ci\_storage\_volume\]|
    |object\_id|A unique identifier, allocated by Microsoft Azure for this resource.|
    |name|The Name or ID if no Name is specified for the storage volume.|
    |location|Path of the storage volume.|
    |volume\_id|Identifier that holds the volume ID as the value.|
    |volume\_container​|The container name.|
    |comments|Identifier for internal usage \(deletion strategy\).|
    |status|The status of the resource.|
    |Block Endpoint \[cmdb\_ci\_endpoint\_block\]|
    |name|The Name or ID if no Name is specified for the block endpoint.|
    |object\_id|A unique identifier, allocated by Microsoft Azure for this resource.|

-   **Resources discovered by the Microsoft Azure - Storage Volume \(LP\) pattern**

<table id="table_nps_rdl_rnb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Storage Volume \[cmdb\_ci\_storage\_volume\]​

</td></tr><tr><td>

object\_id​

</td><td>

A unique identifier, allocated by Microsoft Azure for this resource.

</td></tr><tr><td>

name

</td><td>

The Name or ID if no Name is specified for the storage volume.

</td></tr><tr><td>

volume\_id​

</td><td>

The volume type. For example:-   `gp2` for General Purpose SSD
-   `io1` for Provisioned IOPS SSD
-   `st1` for Throughput Optimized HDD
-   `sc1` for Cold HDD
-   `standard` for Magnetic volumes


</td></tr><tr><td>

location

</td><td>

Path of the storage volume.

</td></tr><tr><td>

state

</td><td>

The current state of the storage volume.

</td></tr><tr><td>

install\_status​

</td><td>

Resource provisioning status.

</td></tr><tr><td>

size

</td><td>

The size of the volume.

</td></tr><tr><td>

size\_bytes

</td><td>

The size of the volume \(bytes\).

</td></tr><tr><td>

storage\_type

</td><td>

For example, hard-coded value "block".

</td></tr><tr><td>

comments

</td><td>

Identifier for internal usage \(deletion strategy\).

</td></tr></tbody>
</table>-   **Resources discovered by the Microsoft Azure - Sub Account \(LP\) pattern**

    |Field|Description|
    |-----|-----------|
    |Cloud Service Account \[cmdb\_ci\_cloud\_service\_account​\]|
    |object\_id​ ​ ​ ​ ​ ​ ​|A unique identifier, allocated by Microsoft Azure for this resource.|
    |account\_id|The unique identifier \(ID\) of the account.|
    |name|The Name or ID if no Name is specified for the service account.|
    |datacenter\_type|cmdb\_ci\_azure\_datacenter|
    |discovery\_credentials|Reference field to the related Microsoft Azure credentials.|
    |datacenter\_url|The URL of the datacenter.|
    |parent\_account|Reference to the primary account, if it exists.|
    |is\_master\_account​|The Boolean attribute indicating if this is the primary account or not.|


-   **Resources discovered by the Microsoft Azure WebSite \(LP\) pattern and Microsoft Azure WebSite pattern**

    |Field|Description|
    |-----|-----------|
    |Cloud Resource \[cmdb\_ci\_cloud\_webserver\]|
    |Name​ \[name\]|The name of the Azure web server.|
    |Object ID \[object\_id\]|The ID of Azure web server.|
    |IP Address \[ip\_address\]​|The IP address of the web server.|
    |FQDN \[fqdn\]|The fully qualified domain name \(FQDN\) of the web server.|
    |Vendor \[vendor\]|The vendor is Microsoft.|
    |Install Status \[install\_status\]|The install status of the web server.|
    |State \[state\]|The operational state of the web server.|
    |Operational Status \[operational\_status\]|The operational status of the web server.|
    |IP Address \[cmdb\_ci\_ip\_address\]|
    |Name \[name\]|The IP address of the web server.|
    |IP Address \[ip\_address\]|The IP address of the web server.|
    |FQDN \[fqdn\]|The fully qualified domain name \(FQDN\).|
    |Vendor \[vendor\]|The vendor is Microsoft.|
    |Install Status \[install\_status\]|The install status.|
    |Operational Status \[operational\_status\]|The operational status.|
    |Key Value \[cmdb\_key\_value\]|
    |Key \[key\]|The Azure Key Value name.|
    |Value \[value\]|The Azure Key Value value.|

-   **Resources discovered using the Azure DataBase \(LP\) pattern**

    |Field|Description|
    |-----|-----------|
    |Fully qualified domain name \[fqdn\]|The FQDN that Microsoft Azure assigned to your database.|
    |Name \[name\]|The name of the database that you created in Microsoft Azure.|
    |Object ID \[object\_id\]|The identification name of the database.|
    |Operational Status \[operational\_status\]|The operational status of the database.|
    |Type \[type\]|The type of database you created.|
    |State \[state\]|The state of the database: Whether it’s Available or Terminated.|
    |Vendor \[vendor\]|The vendor name is Azure.|
    |Version \[version\]|The version of the database.|
    |Category \[category\]|The stock keeping unit \(SKU\) family.|

    |Field|Description|
    |-----|-----------|
    |Object ID \[object\_id\]|A unique identifier for the hardware type.|
    |Name \[name\]|Name for the hardware type.|
    |vCPUs \[vcpus\]|Number of virtual CPU cores.|
    |Provider \[provider\]|Provider for the hardware type: Azure.|

    |Field|Description|
    |-----|-----------|
    |Netmask \[netmask\]|Netmask of the Azure database.|

-   **Resources discovered using the Azure DataBase \(LP\) pattern extension: Azure SQL Managed Instance license**

<table id="table_jbc_kwd_zbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Key \[key\]

</td><td>

SQL\_Server\_PaaS\_Managed\_Instance\_License\_Type\_automatic

</td></tr><tr><td>

Value \[value\]

</td><td>

License type. The following maps the Azure portal license to ServiceNow values:-   **Azure Hybrid Benefit**: BYOL
-   **Pay as you go**: License Included
-   **Hybrid Failover rights**: Hybrid Failover


</td></tr><tr><td>

Configuration item \[configuration\_item\]

</td><td>

cmdb\_ci\_cloud\_database

</td></tr></tbody>
</table>    |Field|Description|
    |-----|-----------|
    |Object ID \[object\_id\]|Object ID of the Azure cloud database.|
    |Name \[name\]|SKU name.|
    |Cloud Vendor \[cloud\_vendor\]|Cloud vendor of the serverless hardware: MS Azure.|
    |CPU core count \[cpu\_core\_count\]|Number of virtual cores \(vCores\).|
    |CPU core thread \[cpu\_core\_thread\]|Number of vCores.|
    |CPU count \[cpu\_count\]|Number of vCores.|
    |Category \[category\]|vCore purchasing model.|
    |Subcategory \[subcategory\]|SKU tier.|
    |Host Type \[host\_type\]|Host type: PaaS.|

-   **Resources discovered by the Azure - Marketplace LB \(LP\) pattern**

    |Field|Description|
    |-----|-----------|
    |Name \[name\]|Name of the Cloud resource, usually the marketplace offering or SKU name.|
    |Object ID \[object\_id\]|A unique resource ID of the Cloud resource.|
    |Resource Type \[resource\_type\]|Service in Cloud Marketplace.​ For example: microsoft.compute/virtualmachines.|
    |Plan Name \[plan\_name\]|Billing or SKU plan for a resource from the Cloud Marketplace.​ For example: Pay as You Go.|
    |Market \[market\]|International Organization for Standardization \(ISO\) code of the geographical market where the resource is sold in the specified market. For example: US or EU.|
    |Organization Id \[organization\_id\]|A unique identifier for the organization or publisher that owns the marketplace resource.|

    |Field|Description|
    |-----|-----------|
    |Product Code \[product\_code\]|A unique product code of the resource within the Cloud Marketplace.|
    |Publisher Name \[publisher\_name\]|Organization or individual responsible for creating and offering the product or service.|
    |Version \[version\]|Release number or iteration of the product​.|
    |Deployed On \[deployed\_on\]|References the Deployed Marketplace Product \[cmdb\_ci\_deployed\_marketplace\_product\] table.|

    |Field|Description|
    |-----|-----------|
    |Key \[key\]|Azure Key Value name.|
    |Value \[value\]|Azure Key Value value.|

-   **Resources discovered by the Azure - Sub Account \(LP\) pattern extension: Azure Management Groups**

<table id="table_rwt_pws_p2c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \[name\]

</td><td>

Tenant ID or name.-   Tenant ID: When using management-level credentials
-   Tenant name: When using tenant-level credentials


</td></tr><tr><td>

Object ID \[object\_id\]

</td><td>

Tenant ID.

</td></tr><tr><td>

DNS Domain \[dns\_domain\]

</td><td>

Domain name entered during registration. For example: `servicenow.com`. This field is only populated when using tenant-level credentials.

</td></tr></tbody>
</table><table id="table_f3n_vws_p2c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \[name\]

</td><td>

Management group name.

</td></tr><tr><td>

Object ID \[object\_id\]

</td><td>

Management group name and tenant ID in the following format: `name+@+tenantId`. For example: `itomMgmtGroup@8bcff-vdc-btrv`.

</td></tr><tr><td>

Parent \[parent\]

</td><td>

References the direct parent Azure Management Group \[cmdb\_ci\_azure\_management\_group\] table.

</td></tr></tbody>
</table>
## CI relationships

-   **Relationships discovered using the Microsoft Azure - Application LB \(LP\) pattern**

    |CI|Relationship|CI|
    |---|------------|---|
    |cmdb\_ci\_cloud\_load\_balancer|Owns::Owned by|cmdb\_ci\_cloud\_lb\_ipaddress|
    |cmdb\_ci\_cloud\_load\_balancer|Hosted on::Hosts|cmdb\_ci\_azure\_datacenter|
    |cmdb\_ci\_lb\_service|Hosted on::Hosts|cmdb\_ci\_cloud\_load\_balancer|
    |cmdb\_ci\_cloud\_subnet|Contains::Contained by|cmdb\_ci\_cloud\_load\_balancer|
    |cmdb\_ci\_lb\_pool|Hosted on::Hosts|cmdb\_ci\_cloud\_load\_balancer|
    |cmdb\_ci\_resource\_group|Contains::Contained by|cmdb\_ci\_cloud\_load\_balancer|

-   **Relationships discovered using the Microsoft Azure - Network and Subnet \(LP\) pattern**

    |CI|Relationship|CI|
    |---|------------|---|
    |cmdb\_ci\_network|Hosted on::Hosts|cmdb\_ci\_azure\_datacenter|
    |cmdb\_ci\_network|Contains::Contained by|cmdb\_ci\_cloud\_subnet|
    |cmdb\_ci\_resource\_group|Contains::Contained by|cmdb\_ci\_network|

-   **Relationships discovered using the Microsoft Azure - NIC \(LP\) pattern**

    |CI|Relationship|CI|
    |---|------------|---|
    |cmdb\_ci\_nic|Hosted on::Hosts|cmdb\_ci\_azure\_datacenter|
    |cmdb\_ci\_resource\_group|Contains::Contained by|cmdb\_ci\_nic|
    |cmdb\_ci\_cloud\_subnet|Contains::Contained by|cmdb\_ci\_nic|

-   **Relationships discovered using the Microsoft Azure - Private Gateway \(LP\) pattern**

    |CI|Relationship|CI|
    |---|------------|---|
    |cmdb\_ci\_endpoint\_vpg|Implement End Point To::Implement End Point From|cmdb\_ci\_virtual\_pvt\_gateway|
    |cmdb\_ci\_resource\_group|Contains::Contained by|cmdb\_ci\_virtual\_pvt\_gateway|
    |cmdb\_ci\_virtual\_pvt\_gateway|Hosted on::Hosts|cmdb\_ci\_azure\_datacenter|
    |cmdb\_ci\_network|Use End Point To::Use End Point From|cmdb\_ci\_endpoint\_vpg|

-   **Relationships discovered using the Microsoft Azure - Public IP \(LP\) pattern**

    |CI|Relationship|CI|
    |---|------------|---|
    |cmdb\_ci\_cloud\_public\_ipaddress|Hosted on::Hosts|cmdb\_ci\_azure\_datacenter|
    |cmdb\_ci\_nic|Contains::Contained by|cmdb\_ci\_cloud\_public\_ipaddress|
    |cmdb\_ci\_resource\_group|Contains::Contained by|cmdb\_ci\_cloud\_public\_ipaddress|

-   **Relationships discovered using the Microsoft Azure - Resource Group \(LP\) pattern**

    |CI|Relationship|CI|
    |---|------------|---|
    |cmdb\_ci\_azure\_datacenter|Contains::Contained by|cmdb\_ci\_resource\_group|

-   **Relationships discovered using the Microsoft Azure - Route Table \(LP\) pattern**

    |CI|Relationship|CI|
    |---|------------|---|
    |cmdb\_ci\_route\_table|Contains::Contained by|cmdb\_ci\_route|
    |cmdb\_ci\_route\_table|Contains::Contained by|cmdb\_ci\_network|
    |cmdb\_ci\_resource\_group|Contains::Contained by|cmdb\_ci\_route\_table|
    |cmdb\_ci\_azure\_datacenter|Contains::Contained by|cmdb\_ci\_route\_table|

-   **Relationships discovered using the Microsoft Azure - Security Group \(LP\) pattern**

    |CI|Relationship|CI|
    |---|------------|---|
    |cmdb\_ci\_cloud\_subnet|Uses::Used by|cmdb\_ci\_compute\_security\_group|
    |cmdb\_ci\_network|Contains::Contained by|cmdb\_ci\_compute\_security\_group|
    |cmdb\_ci\_resource\_group|Contains::Contained by|cmdb\_ci\_compute\_security\_group|
    |cmdb\_ci\_compute\_security\_group|Hosted on::Hosts|cmdb\_ci\_azure\_datacenter|

-   **Relationships discovered using the Microsoft Azure - Storage Account \(LP\) pattern**

    |CI|Relationship|CI|
    |---|------------|---|
    |cmdb\_ci\_resource\_group|Contains::Contained by|cmdb\_ci\_cloud\_storage\_account|
    |cmdb\_ci\_cloud\_storage\_account|Hosted on::Hosts|cmdb\_ci\_azure\_datacenter|

-   **Relationships discovered using the Microsoft Azure - Storage Containers \(LP\) pattern**

    |CI|Relationship|CI|
    |---|------------|---|
    |cmdb\_ci\_endpoint\_block|Implement End Point To::Implement End Point From|cmdb\_ci\_storage\_volume|
    |cmdb\_ci\_cloud\_storage\_account|Contains::Contained by|cmdb\_ci\_storage\_volume|
    |cmdb\_ci\_resource\_group|Contains::Contained by|cmdb\_ci\_storage\_volume|
    |cmdb\_ci\_storage\_volume|Hosted on::Hosts|cmdb\_ci\_azure\_datacenter|

-   **Relationships discovered using the Microsoft Azure - Storage Volume \(LP\) pattern**

    |CI|Relationship|CI|
    |---|------------|---|
    |cmdb\_ci\_resource\_group|Contains::Contained by|cmdb\_ci\_storage\_volume|
    |cmdb\_ci\_storage\_volume|Hosted on::Hosts|cmdb\_ci\_azure\_datacenter|

-   **Relationships discovered using the Microsoft Azure - Sub Account \(LP\) pattern**

    The Microsoft Azure - Sub Account \(LP\) pattern does not discover any relationships.

-   **Relationships discovered using the Microsoft Azure WebSite \(LP\) and Microsoft Azure WebSite patterns**

    |CI|Relationship|CI|
    |---|------------|---|
    |cmdb\_ci\_cloud\_webserver|Hosted on::Hosts|cmdb\_ci\_azure\_datacenter|
    |cmdb\_ci\_cloud\_webserver|Owns::Owned|cmdb\_ci\_ip\_address|
    |cmdb\_key\_value|Reference only|cmdb\_ci\_cloud\_webserver|

-   **Relationships discovered using the Azure DataBase \(LP\) Pattern.**

    |CI|Relationship|CI|
    |---|------------|---|
    |cmdb\_ci\_cloud\_database|Owns:Owned By|cmdb\_ci\_ip\_address|
    |cmdb\_ci\_cloud\_database|Contains::Contained by|cmdb\_ci\_database|
    |cmdb\_ci\_cloud\_database|Hosted On::Hosted|cmdb\_ci\_azure\_datacenter|
    |cmdb\_ci\_database|Provisioned From::Provisioned|cmdb\_ci\_compute\_template|
    |cmdb\_ci\_database|Provisioned From::Provisioned|cmdb\_ci\_cloud\_hardware\_type|
    |cmdb\_ci\_compute\_template|Hosted On::Hosts|cmdb\_ci\_azure\_datacenter|
    |cmdb\_ci\_compute\_template|Hosted On::Hosts|cmdb\_ci\_cloud\_hardware\_type|

-   **Relationships discovered using the Azure DataBase \(LP\) pattern extension: Azure SQL Managed Instance license**

    |CI|Relationship|CI|
    |---|------------|---|
    |cmdb\_ci\_cloud\_database|Runs on::Runs|cmdb\_ci\_serverless\_hardware|
    |cmdb\_ci\_serverless\_hardware|Hosted on::Hosts|cmdb\_ci\_azure\_datacenter|
    |cmdb\_key\_value|Reference only|cmdb\_ci\_cloud\_database|

-   **Relationships discovered using the Azure - Marketplace LB \(LP\) pattern**

    |CI|Relationship|CI|
    |---|------------|---|
    |Deployed Marketplace Product ​\[cmdb\_ci\_deployed\_marketplace\_product\]|Extends from|Virtual Machine Object \[cmdb\_ci\_vm\_object\]|
    |Deployed Marketplace Product ​\[cmdb\_ci\_deployed\_marketplace\_product\]|Hosted on::Hosts|Cloud Service Account \[cmdb\_ci\_cloud\_sevice\_account\]|
    |Deployed Marketplace Product ​\[cmdb\_ci\_deployed\_marketplace\_product\]|Hosted on::Hosts|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|
    |Marketplace Product Details \[marketplace\_product\_details\]|References|Deployed Marketplace Product ​\[cmdb\_ci\_deployed\_marketplace\_product\]|
    |Resource Group \[cmdb\_ci\_resource\_group\]|Contains::Contained by|Deployed Marketplace Product ​\[cmdb\_ci\_deployed\_marketplace\_product\]|

-   **Relationships discovered using the Azure - Sub Account \(LP\) pattern extension: Azure Management Groups**

    |CI|Relationship|CI|
    |---|------------|---|
    |Azure Management Group \[cmdb\_ci\_azure\_management\_group\]|Contains::Contained by|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|
    |Cloud Organizations \[cmdb\_ci\_cloud\_org\]|Contains::Contained by|Azure Management Group \[cmdb\_ci\_azure\_management\_group\]|
    |Azure Management Group \[cmdb\_ci\_azure\_management\_group\]|Contains::Contained by|Azure Management Group \[cmdb\_ci\_azure\_management\_group\]|
    |**\***Azure Management Group \[cmdb\_ci\_azure\_management\_group\]|References|Azure Management Group \[cmdb\_ci\_azure\_management\_group\]|

    **\***Only references the direct parent-child management group relationship.


## Events discovered by Discovery during horizontal discovery

Discovery uses patterns to find events created for Microsoft Azure components. If there are events that indicate the change of state in one of the Microsoft Azure components, it triggers the discovery of Microsoft Azure components using the patterns.

|Pattern|CI Class|
|-------|--------|
|Azure Application LB Event|Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|
|Azure Availability Set Event|Availability Set \[cmdb\_ci\_availability\_set\]|
|Azure Classic LB Event|Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|
|Azure DataBase Event|Cloud DataBase \[cmdb\_ci\_cloud\_database\]|
|Azure Express Route Circuit Event|Cloud Direct Connect \[cmdb\_ci\_cloud\_direct\_connect\]|
|Azure Functions Event|Cloud Function \[cmdb\_ci\_cloud\_function\]|
|Azure Local Network Gateway Event|Virtual Private Gateway \[cmdb\_ci\_virtual\_pvt\_gateway\]|
|Azure NAT Gateway Event|NAT Gateway \[cmdb\_ci\_nat\_gateway\]|
|Azure Network Event|Cloud Network \[cmdb\_ci\_network\]|
|Azure NIC Event|Cloud Mgmt Network Interface \[cmdb\_ci\_nic\]|
|Azure Private DNS Zone Event|DNS Zone \[cmdb\_ci\_dns\_zone\]|
|Azure Public IP Event|Cloud Public IP Address \[cmdb\_ci\_cloud\_public\_ipaddress\]|
|Azure Resource Group Event|Resource Group \[cmdb\_ci\_resource\_group\]|
|Azure Security Group Event|Compute Security Group \[cmdb\_ci\_compute\_security\_group\]|
|Azure Storage Account Event|Cloud Storage Account \[cmdb\_ci\_cloud\_storage\_account\]|
|Azure Virtual Machine Event|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|
|Azure Virtual Network Gateway Connection Event|Virtual Network Gateway Connection \[cmdb\_ci\_vpc\_gateway\_connection\]|
|Azure Virtual Network Peerings Event|Virtual Network Peering \[cmdb\_ci\_vnet\_peering\]|
|Azure VM Scale Set Event|Instance Scale Set \[cmdb\_ci\_instance\_scale\_set\]|

## Tag information collected by Discovery during horizontal discovery

When running the patterns, tag information is collected to populate the cmdb\_key\_value table.​ Each tag is related to a CI that was discovered during the discovery.​ Tag discovery is done in the extension section of each pattern.

## Data collected by Service Mapping during tag-based discovery

Service Mapping uses tag-based discovery to create service instance maps including the Cloud components. The Service Mapping application comes with the following preconfigured CI relationships used for tag-based discovery. These CI relationships are available from the 1.0.68 release on the ServiceNow Store.

|CI|Relationship|CI|
|---|------------|---|
|Configuration Item \[cmdb\_ci\]|Hosted on::Hosts|Logical Datacenter \[cmdb\_ci\_logical\_datacenter\]|
|Logical Datacenter \[cmdb\_ci\_logical\_datacenter\]|Hosted on::Hosts|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|

-   **[Azure Application Insight Data Collection Rule pattern-based discovery](../../patterns/azure-app-insight-data-collect-rule.md)**  
Discovery and Service Mapping Patterns finds Azure services on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[Azure Blob Storage pattern-based discovery](azure-blob-storage-pattern.md)**  
Discovery and Service Mapping Patterns finds blob resources within Azure Blob Storage on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[Azure Classic Load Balancer pattern-based discovery](azure-classic-load-balancer-pattern.md)**  
Discovery and Service Mapping Patterns finds Azure Classic Load Balancers on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[Azure Cosmos DB for PostgreSQL Cluster pattern-based discovery](../../patterns/azure-cosmos-db-postgresql-cluster.md)**  
Discovery and Service Mapping Patterns finds Azure services on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[Azure Data Explorer Cluster pattern-based discovery](../../patterns/azure-data-explorer-cluster.md)**  
Discovery and Service Mapping Patterns finds Azure services on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[Azure Datacenter discovery pattern-based discovery](azure-datacenter-discovery-pattern.md)**  
Discovery and Service Mapping Patterns finds Azure Datacenter resources on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[Azure Dev Center pattern-based discovery](../../patterns/azure-dev-center.md)**  
Discovery and Service Mapping Patterns finds Azure services on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[Azure Express Route Circuit pattern-based discovery](azure-express-route-circuit-pattern.md)**  
Discovery and Service Mapping Patterns finds Azure Express Route Circuit resources on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[Azure File Share pattern-based discovery](azure-file-share-pattern.md)**  
Discovery and Service Mapping Patterns finds Azure File Share resources within Storage Accounts on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[Azure Firewall Network Security pattern-based discovery](../../patterns/azure-firewall-network-security.md)**  
Discovery and Service Mapping Patterns finds Azure services on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[Azure hardware type pattern-based discovery](azure-hardware-type-pattern.md)**  
Discovery and Service Mapping Patterns finds Azure hardware type configurations on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[Azure Host pattern-based discovery](azure-host-pattern.md)**  
Discovery and Service Mapping Patterns finds Azure Hosts on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[Azure Local Network Gateway pattern-based discovery](azure-local-network-gateway-pattern.md)**  
Discovery and Service Mapping Patterns finds Azure Local Network Gateway resources on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[Azure Log Analytics Workspace pattern-based discovery](../../patterns/azure-log-analytics-workspace.md)**  
Discovery and Service Mapping Patterns finds Azure services on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[Azure Network Address Translation \(NAT\) Gateway pattern-based discovery](azure-nat-gateway-pattern.md)**  
Discovery and Service Mapping Patterns finds Azure NAT Gateway resources on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[Azure OS image pattern-based discovery](azure-os-image-pattern.md)**  
Discovery and Service Mapping Patterns finds Azure OS images on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[Azure Private Domain Name System \(DNS\) Zone pattern-based discovery](azure-private-dns-zone-pattern.md)**  
Discovery and Service Mapping Patterns finds Azure Private DNS Zone resources on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[Azure Recovery Services Vault pattern-based discovery](../../patterns/azure-recovery-services-vault.md)**  
Discovery and Service Mapping Patterns finds Azure services on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[Azure Recovery Services Vault Backup Item pattern-based discovery](../../patterns/azure-recovery-services-vault-backup.md)**  
Discovery and Service Mapping Patterns finds Azure services on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[Azure Service Endpoint Policy pattern-based discovery](../../patterns/azure-service-endpoint-policy.md)**  
Discovery and Service Mapping Patterns finds Azure services on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[Azure Subscriptions Discovery For Management Group pattern-based discovery](azure-sub-mgmt-group-pattern.md)**  
Discovery and Service Mapping Patterns finds Azure Subscription entities under Management Groups on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[Azure virtual machine pattern-based discovery](azure-vm-pattern.md)**  
Discovery and Service Mapping Patterns finds Azure virtual machines \(VMs\) on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[Azure Virtual Network Gateway Connection pattern-based discovery](azure-vng-connection-pattern.md)**  
Discovery and Service Mapping Patterns finds Azure Virtual Network Gateway Connection resources on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[Azure Web Application Firewall Policy pattern-based discovery](../../patterns/azure-web-app-firewall-policy.md)**  
Discovery and Service Mapping Patterns finds Azure services on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

**Parent Topic:**[Available cloud discovery patterns](../concept/available-patterns-cloud.md)

**Related topics**  


[Kubernetes discovery using patterns](../concept/kubernetes-discovery.md)

[Azure Key Vault certificate discovery](../../discovery/reference/azure-certificate-discovery-pattern.md)

[Microsoft Foundry \(Classic\) pattern-based discovery](../../ai-agent-topology-mapping/reference/microsoft-foundry-classic-pattern.md)

