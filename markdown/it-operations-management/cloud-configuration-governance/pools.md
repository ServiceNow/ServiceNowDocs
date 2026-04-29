---
title: Pools and Filters for Cloud Provisioning
description: A resource pool is a query or script that filters a table. You configure a resource pool to limit the values that are available to users when they request a catalog item.
locale: en-US
release: australia
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Pools and Filters for Cloud Provisioning

A resource pool is a query or script that filters a table. You configure a resource pool to limit the values that are available to users when they request a catalog item.

## Example use of a pool

To limit a user to only the networks in a particular logical datacenter, use the resource pool called NetworkPool that runs against the Cloud Network \[cmdb\_ci\_network\] table. The resource pool uses a script to filter networks based on the datacenter that the network belongs to.

![How a pool works](../image/pool-example.jpg)

## How pools work

The naming convention for pools is:

```
get<thisItem>By<condition>
```

Where the `condition` is the top-level entity that forms the relationship between the return values. For example, `getObjectIdByServiceAccount` filters all ObjectIDs that are hosted on the specified service account.

Filters query tables using only the specified condition. Any record that matches the condition is therefore returned.

## Pools and blueprints

When you configure blueprints, you specify variables for form behavior. You can specify resource pools as the data source for each variable and select which resource pools to use. The variable then uses the filtered values.

## Resource Pool in the base system

<table id="table_g1p_r5m_2z"><thead><tr><th>

Pool

</th><th>

Based on this table

</th><th>

Filter type

</th><th>

Filter name and description

</th></tr></thead><tbody><tr><td>

AnsibleInventoryPool

</td><td>

Ansible Tower Inventory \[sn\_cfg\_ansible\_inventory\]

</td><td>

Script

</td><td>

Filters the name of Ansible Tower Inventory.

</td></tr><tr><td>

ApplicationPool

</td><td>

Application

</td><td>

Query

</td><td>

Filters the names of applications.

</td></tr><tr><td>

ApplicationProfilePool

</td><td>

Application Profile \[sn\_cmp\_application\_profile\]

</td><td>

Script

</td><td>

Filters the name of application profiles.

</td></tr><tr><td>

AvailabilityZonePool

</td><td>

Availability zone \[cmdb\_ci\_availability\_zone\]

</td><td>

Script

</td><td>

Filters availability zones based on the logical datacenter they belong to.getNameByLDC: Filters availability zones based on the logical datacenter they belong to.

 The Terraform template for IBM requires the name of the availability zone as input for provisioning.

</td></tr><tr><td>

AzureDevOpsPipelinePool

</td><td>

Config Installable \[sn\_cmp\_cfg\_installable\]

</td><td>

Script

</td><td>

Filters the installable configs.

</td></tr><tr><td>

AzureDevOpsProjectPool

</td><td>

Azure DevOps Project \[sn\_itom\_csc\_cp\_azure\_devops\_project\]

</td><td>

Script

</td><td>

Filters projects based on config provider.

</td></tr><tr><td>

BusinessServicePool

</td><td>

Service \[cmdb\_ci\_service\]

</td><td>

Query

</td><td>

Filters the names of business services.

</td></tr><tr><td>

ChefServerPool

</td><td>

Chef Server \[sn\_cfg\_chef\_server\]

</td><td>

Script

</td><td>

Filters chef server credentials by Chef server.

</td></tr><tr><td>

CloudAccountPool

</td><td>

Cloud Account \[cmdb\_ci\_cmp\_cloud\_account\]

</td><td>

Query

</td><td>

Filters the names of cloud accounts.

</td></tr><tr><td>

CloudKeyPairPool

</td><td>

\[cmdb\_ci\_cloud\_key\_pair\]

</td><td>

Script

</td><td>

getObjectIdByServiceAccount: Filters cloud keypairs based on the service account they belong to.

</td></tr><tr><td>

ComputeProfilePool

</td><td>

Compute Profile \[sn\_cmp\_compute\_profile\]

</td><td>

Script

</td><td>

Filters compute profiles by the logical datacenter and the cloud account it belongs to.

</td></tr><tr><td>

ConfigMgmtPool

</td><td>

 

</td><td>

Script

</td><td>

Filters config management workload provider.

</td></tr><tr><td>

CostCenterPool

</td><td>

Cost Center \[cmn\_cost\_center\]

</td><td>

Script

</td><td>

Filters to list only the cost centers that the user belongs to.

</td></tr><tr><td>

DatastorePool

</td><td>

VMware vCenter datastore \[cmdb\_ci\_vcenter\_datastore\]

</td><td>

Script

</td><td>

Filters datastores based on the logical datacenter they belong to.

</td></tr><tr><td>

HardwareTypePool

</td><td>

\[cmdb\_ci\_compute\_template\]

</td><td>

Script

</td><td>

getObjectIdByAvailabilityZone: Filters hardware templates based on availability zone they belong to.

</td></tr><tr><td>

ImagePool

</td><td>

\[cmdb\_ci\_os\_template\]

</td><td>

Script

</td><td>

getObjectIdByServiceAccount: Filters the resourceId of OS Image by service account. In IBM Cloud, OS Images are not specific to a datacenter, so they are hosted at the service account level. Terraform requires the resourceId as input for provisioning.

</td></tr><tr><td>

IPAddressPool

</td><td>

Cloud IP Address \[cmdb\_ci\_cloud\_ip\_address\]

</td><td>

Query

</td><td>

Filters the IP address.

</td></tr><tr><td>

LaunchConfigurationPool

</td><td>

Server Array Launch Configuration \[cmdb\_ci\_sa\_launch\_config\]

</td><td>

Query

</td><td>

Filters the configuration pool.

</td></tr><tr><td>

NetworkInterfacePool

</td><td>

Cloud Mgmt Network Interface \[cmdb\_ci\_nic\]

</td><td>

Script

</td><td>

Filters the network interface pool.

</td></tr><tr><td>

NetworkPool

</td><td>

Cloud Network \[cmdb\_ci\_network\] table

</td><td>

Script

</td><td>

-   Filters networks based on the logical datacenter they belong to.
-   getObjectIdByLDC: Filters network IDs based on the logical datacenter they belong to.

</td></tr><tr><td>

OSProfilePool

</td><td>

OS Profile \[sn\_cmp\_os\_profile\]

</td><td>

Script

</td><td>

Filters compute profiles by the logical datacenter and the cloud account it belongs to.

</td></tr><tr><td>

ProjectsPool

</td><td>

Project \[pm\_project\]

</td><td>

Query

</td><td>

Filters the names of projects.

</td></tr><tr><td>

ResourceGroupPool

</td><td>

Resource group \[cmdb\_ci\_resource\_group\]

</td><td>

Script

</td><td>

Filters resource group based on the logical datacenter they belong to.

</td></tr><tr><td>

ScheduleTimeZonePool

</td><td>

Choice \[sys\_choice\]

</td><td>

Script

</td><td>

Filters scheduled time zones.

</td></tr><tr><td>

SecurityGroupPool

</td><td>

Compute Security Group \[cmdb\_ci\_compute\_security\_group\]

</td><td>

Script

</td><td>

-   getByNetwork: Filters the security group by the network it belongs to.
-   getObjectIdByServiceAccount: Filters security group IDs based on the service account they belong to.

</td></tr><tr><td>

SecurityGroupProfilePool

</td><td>

Compute Security Group Profile \[sn\_cmp\_security\_grp\_profile\]

</td><td>

Query

</td><td>

Filters the names of security group profiles.

</td></tr><tr><td>

SSHKeyPool

</td><td>

CMP SSH Key Pair \[sn\_cmp\_ssh\_credentials\]

</td><td>

Script

</td><td>

Filters user keys by user.

</td></tr><tr><td>

StorageAccountPool

</td><td>

Cloud Storage Account \[cmdb\_ci\_cloud\_storage\_account\]

</td><td>

Script

</td><td>

Filters cloud storage accounts based on the logical datacenter they belong to.

</td></tr><tr><td>

StorageVolumePool

</td><td>

Storage Volume \[cmdb\_ci\_storage\_volume\]

</td><td>

Query

</td><td>

Filters the names of storage volumes.

</td></tr><tr><td>

SubnetPool

</td><td>

Cloud Subnet \[cmdb\_ci\_cloud\_subnet\]

</td><td>

Script

</td><td>

-   Filters the subnet by the network it belongs to.
-   getObjectIdByNetwork: Filters subnets based on the network they belong to.

</td></tr><tr><td>

UserGroupPool

</td><td>

Group \[sys\_user\_group\]

</td><td>

Script

</td><td>

Returns only the groups that the user belongs to.

</td></tr><tr><td>

VirtualMachinePool

</td><td>

\[sn\_cmp\_resource\_pool\]

</td><td>

Script

</td><td>

getByAvailabilityZone: Filters virtual machine IDs based on the availability zone that they belong to.

</td></tr><tr><td>

VmFolderPool

</td><td>

VMware vCenter folder \[cmdb\_ci\_vcenter\_folder\]

</td><td>

Script

</td><td>

Filters VM folders based on the logical datacenter they belong to.

</td></tr></tbody>
</table>