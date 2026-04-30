---
title: ESXi server discovery
description: Discovery identifies and classifies information about ESXi servers and ESXi resource pools through the discovery of vCenter and not from the direct discovery of any ESXi servers.
locale: en-US
release: yokohama
product: ITOM Visibility
classification: itom-visibility
topic_type: reference
last_updated: "2025-12-02"
reading_time_minutes: 5
keywords: [EXSi server discovery, EXSi resource pool, EXSi server]
breadcrumb: [Discovery for VMware virtualization, Operating systems discovery, Data collected by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# ESXi server discovery

Discovery identifies and classifies information about ESXi servers and ESXi resource pools through the discovery of vCenter and not from the direct discovery of any ESXi servers.

**Important:** ESXi server discovery is done through vCenter. Do not specify the IP address of the ESXi server in a Discovery Schedule. Instead, discover the vCenter through the Discovery Schedule.

For a description of the VMware architecture and component relationships, see [Data collected for VMware vCenter Server](r_VCenterDataCollected.md).

For a discussion of how Discovery collects information on datastores and establishes the relationships between the ESXi hosts and the storage disks attached to the datastores, see [Datastore Discovery](../concept/c_DatastoreDiscovery.md)

## Required Roles

Users with the **itil** and **asset** roles can access ESXii and ESXi configuration item \(CI\) records. To run discovery on vCenter servers, users must have the **discovery\_admin** role.

## Credentials

To run a complete Discovery of vCenter/ESXi servers, you need vCenter credentials. If the vmapp port probe is disabled, you must use Windows credentials to access the Windows host on which the vCenter server runs.

**Note:** Make sure to select a credential Type of VMware.

## ESXi server Discovery components

Discovery identifies ESXi servers based on the correlation ID \(BIOS UUID\) , when the hardware manufacturer is on a certified inclusion list. So if the manufacturer is in the compatible manufacturers list, the correlation-id needs to be unique. If the manufacturer is not on the certified inclusion list, we check for the Managed Object Reference ID \(MORID\) and Serial Number as well. After running the vCenter classifier, Discovery launches the VMware - vCenter Datacenters probe, which launches the probes that explore the ESXi server. For the complete list of vCenter probes, see [List of Discovery probes](r_ListOfDiscoveryProbes.md).

|Component|Name|Description|
|---------|----|-----------|
|Classifier|vCenter|Classifies stand-alone vCenter servers.|
|Probe|VMWare - vCenter ESX Hosts|Creates records for ESXi servers and hostmounts. Creates relationships between ESXi servers and vCenter components. Triggers probes for storage Discovery.|
|Probe|VMWare - vCenter ESX Hosts Storage|Creates records for ESXi host hardware: network adapters, disks, HBAs, FC ports, iSCSI and FC disks. Creates relationships between DAS/iSCSI/FC disks and datastore disks.|

## Data collected

Basic server data from ESXi hosts is collected by the VMware - vCenter ESX Hosts probe.

|Label|Table Name|Field Name|
|-----|----------|----------|
|Operating System|cmdb\_ci\_esx\_server|os|
|OS Version|cmdb\_ci\_computer|os\_version|
|Name|cmdb\_ci\_esx\_server|name|
|DNS domain|cmdb\_ci\_esx\_server|dns\_domain|
|Manufacturer|cmdb\_ci\_computer|manufacturer|
|Serial number|cmdb\_ci\_computer|serial\_number|
|CPU type|cmdb\_ci\_esx\_server|cpu\_type|
|CPU speed \(MHz\)|cmdb\_ci\_esx\_server|cpu\_speed|
|CPU count|cmdb\_ci\_esx\_server|cpu\_count|
|CPU core count|cmdb\_ci\_computer|cpu\_core\_count|
|CPU manufacturer|cmdb\_ci\_esx\_server|cpu\_manufacturer|
|Model ID|cmdb\_ci\_computer|model\_id|
|RAM \(MB\)|cmdb\_ci\_esx\_server|ram|
|Disk space \(GB\)|cmdb\_ci\_esx\_server|disk\_space|
|Type|cmdb\_ci\_disk|type|
|Model ID|cmdb\_ci\_disk|model\_id|
|Disk space \(GB\)|cmdb\_ci\_disk|disk\_space|
|Name|cmdb\_ci\_disk|name|
|Name|cmdb\_ci\_network\_adapter|name|
|IP address|cmdb\_ci\_network\_adapter|ip\_address|
|MAC address|cmdb\_ci\_network\_adapter|mac\_address|
|Netmask|cmdb\_ci\_network\_adapter|netmask|
|Managed object reference ID|Visualization Server \[cmdb\_ci\_virtualization\_server\]|morid|
|Serial Number|Serial Number \[cmdb\_serial\_number\]|serial\_number|

## Relationships

Discovery collects the following relationship data for ESXi servers.

|Base Class|Relationship|Dependent Class|
|----------|------------|---------------|
|ESXi Resource Pool \[cmdb\_ci\_esx\_resource\_pool\]|Defines resources for:Gets resources from|ESXi Server \[cmdb\_ci\_esx\_server\]|
|VM Instance \[cmdb\_ci\_vmware\_instance\]|Registered on:Has registered|ESXi Server \[cmdb\_ci\_esx\_server\]|
|ESXi Server \[cmdb\_ci\_esx\_server\]|Provides storage for:Stored on|VM Template \[cmdb\_ci\_vmware\_template\]|
|ESXi Server \[cmdb\_ci\_esx\_server\]|Provided by:Provides|Networks \[cmdb\_ci\_vcenter\_network\]|
|ESXi Server \[cmdb\_ci\_esx\_server\]|Members of:Members|Cluster \[cmdb\_ci\_vcenter\_cluster\]|
|ESXi Server \[cmdb\_ci\_esx\_server\]|Contains:Contained by|Datacenter \[cmdb\_ci\_vcenter\_datacenter\]|

## ESXi resource pools

Resource pools are configured in vCenter and define the maximum amount of resources that virtual machines using that pool can consume. An ESXi server property enables resource pools to expand when necessary if the ESXi server has additional resources to spare. The **Name** and **Owner** fields of each resource pool on the ESXi server must be configured within the ServiceNow AI Platform

in the ESXi Resource Pool \[cmdb\_ci\_esx\_resource\_pool\] table. When Orchestration for VMware executes its manual provisioning tasks, the provisioner must select the proper resource pool for the virtual server requested. Discovery finds resource pools on ESXi machines and populates the fields on the ESXi Resource Pool form automatically. For more information, see [Configure ESXi resource pools](../task/t_ConfigureESXResourcePools.md).

ESXi resource pools requires the Orchestration - VMware Support plugin.

**Note:** Ensure that vCenter and the ESXi server have been fully configured, including the creation of the templates and resource pools.

|Label|Table|Field Name|Source|
|-----|-----|----------|------|
|CPU expandable|ESXi Resource Pool \[cmdb\_ci\_esx\_resource\_pool\]|cpu\_expendable|VMWare - vCenter Clusters probe|
|CPU limit \(MHz\)|ESXi Resource Pool \[cmdb\_ci\_esx\_resource\_pool\]|cpu\_limit\_mhz|VMWare - vCenter Clusters probe|
|CPU reserved \(MHz\)|ESXi Resource Pool \[cmdb\_ci\_esx\_resource\_pool\]|cpu\_reserved\_mhz|VMWare - vCenter Clusters probe|
|CPU shares|ESXi Resource Pool \[cmdb\_ci\_esx\_resource\_pool\]|cpu\_shares|VMWare - vCenter Clusters probe|
|Full path|ESXi Resource Pool \[cmdb\_ci\_esx\_resource\_pool\]|fullpath|VMWare - vCenter Clusters probe|
|Memory expandable|ESXi Resource Pool \[cmdb\_ci\_esx\_resource\_pool\]|mem\_expandable|VMWare - vCenter Clusters probe|
|Memory limit \(MB\)|ESXi Resource Pool \[cmdb\_ci\_esx\_resource\_pool\]|mem\_limit\_mb|VMWare - vCenter Clusters probe|
|Memory reserved \(MB\)|ESXi Resource Pool \[cmdb\_ci\_esx\_resource\_pool\]|mem\_reserved\_mb|VMWare - vCenter Clusters probe|
|Memory shares|ESXi Resource Pool \[cmdb\_ci\_esx\_resource\_pool\]|mem\_shares|VMWare - vCenter Clusters probe|
|Owner|ESXi Resource Pool \[cmdb\_ci\_esx\_resource\_pool\]|owner|VMWare - vCenter Clusters probe|
|Owner Managed Object Reference ID|ESXi Resource Pool \[cmdb\_ci\_esx\_resource\_pool\]|owner\_morid|VMWare - vCenter Clusters probe|

-   **[Configure ESXi resource pools](../task/t_ConfigureESXResourcePools.md)**  
The ESXi server has a default resource pool called Resources that defines normal resources for a virtual machine.

**Parent Topic:**[Discovery for VMware virtualization](../concept/c_DiscoverVMwareInfrastructure.md)

**Related topics**  


[Discovery for VMware vCenter](../concept/c_DiscoveryForVMwareVCenter.md)

[Standalone ESXi discovery](StandaloneESXiDiscovery.md)

[Discovery for VMware virtual machines](../concept/c_VMwareVirtualMachines.md)

[VM instance state and status fields](vm-instance-state-and-status-fields.md)

[Datastore Discovery](../concept/c_DatastoreDiscovery.md)

