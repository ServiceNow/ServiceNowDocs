---
title: Data collected for VMware vCenter Server
description: Discovery identifies and classifies information and data about VMware vCenter servers.
locale: en-US
release: yokohama
product: ITOM Visibility
classification: itom-visibility
topic_type: reference
last_updated: "2025-12-02"
reading_time_minutes: 9
keywords: [data Vmware vCenter, data Vmware server, Data vCenter server]
breadcrumb: [Discovery for VMware vCenter, Discovery for VMware virtualization, Operating systems discovery, Data collected by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Data collected for VMware vCenter Server

Discovery identifies and classifies information and data about VMware vCenter servers.

## vCenter table schema

The vCenter table schema is illustrated in the following diagram:

![vCenter table schema](../image/vcenter_table_schema.png "vCenter table schema")

Several tables are cloud-agnostic tables, meaning that they can be populated for any cloud resource, not just vCenter resources. Look in the sub tables that extend the cloud-agnostic tables to find discovered CIs.

|Cloud-agnostic table|Look in this vCenter-specific table|
|--------------------|-----------------------------------|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|VMware Virtual Machine Instance \[cmdb\_ci\_vmware\_instance\]|
|Operating System Template \[cmdb\_ci\_os\_template\]|VMware Virtual Machine Template \[cmdb\_ci\_vmware\_template\]|
|Logical Datacenter \[cmdb\_ci\_logical\_datacenter\]|VMware vCenter Datacenter \[cmdb\_ci\_vcenter\_datacenter\]|
|Cloud Networks \[cmdb\_ci\_network\]|VMware vCenter Network \[cmdb\_ci\_vcenter\_network\]|
|Datastore \[cmdb\_ci\_datastore\]|VMware vCenter Datastore \[cmdb\_ci\_vcenter\_datastore\]|
|Host Cluster \[cmdb\_ci\_host\_cluster\]|VMware vCenter Cluster \[cmdb\_ci\_vcenter\_cluster\]|

## vCenter data

Discovery uses multiple [vCenter probes](r_ListOfDiscoveryProbes.md) to collect this data from vCenter. The data is saved in tables extend from the Configuration item \[cmdb\_ci\] table.

|Field label|Column name|
|-----------|-----------|
|Name|name|
|IP Address|ip\_address|
|API version|api\_version|
|Full name|fullname|
|Instance UUID|instance\_uuid|
|URL|url|
|Fully qualified domain name|fqdn|

The combination of the vCenter instance in the cmdb\_ci\_vcenter table and the object ID in the cmdb\_ci\_vm\_object table identifies a specific vCenter.

The tables extend from the Virtual Machine Objects \[cmdb\_ci\_vm\_object\] table, which holds object IDs for all cloud-based resources, except virtualization servers.

|Field label|Column name|
|-----------|-----------|
|Cluster|cluster|
|DRS behavior|drs\_behavior|
|DRS enabled|drs\_enabled|
|Virtual machine|virtual\_machine|

This table stores DRS behavior for the VMs that override the cluster behavior. For more information on DRS, see VMware's documentation on [Distributed Resource Scheduler](https://www.vmware.com/products/vsphere/drs-dpm.html).

|Field label|Column name|
|-----------|-----------|
|Cluster|cluster|

The VMware vCenter VM group \[cmdb\_ci\_vcenter\_vm\_group\] table has Contains::Contained by relationship with cmdb\_ci\_vmware\_instance. This group has a set of VMs.

|Field label|Column name|
|-----------|-----------|
|Cluster|cluster|

The VMware vCenter Host Group \[cmdb\_ci\_vcenter\_host\_group\] table has Contains::Contained by relationship with cmdb\_ci\_vmware\_instance. This group has a set of hosts.

|Field label|Column name|
|-----------|-----------|
|Rule UUID|rule\_uuid|
|Active|active|
|Cluster|cluster|

|Field label|Column name|
|-----------|-----------|
|Name|name|
|Template|template|
|CPUs|cpus|
|Disks|disks|
|Disks size \(GB\)|disks\_size|
|Memory \(MB\)|memory|
|Network adapters|nics|
|Image path|image\_path|
|State|state|
|vCenter Instance UUID|vcenter\_uuid|
|vCenter Reference|vcenter\_ref|
|BIOS UUID|bios\_uuid|
|VM Instance UUID|vm\_instance\_uuid|
|IP address|ip\_address|

|Field Label|Column name|
|-----------|-----------|
|Name|name|
|vCenter Instance UUID|vcenter\_uuid|
|Distributed Virtual Switch Reference|dvs\_ref|

|Field label|Column name|
|-----------|-----------|
|Name|The template name from VMWare.|
|CPUs|cpus|
|Disks size \(GB\)|disks\_size|
|Guest ID|guest\_id|
|Memory \(MB\)|memory|
|Image path|image\_path|
|vCenter Instance UUID|vcenter\_uuid|
|vCenter Reference|vcenter\_ref|
|Network adapters|nics|
|Base name|base\_name|
|VM namer|vm\_namer|
|BIOS UUID|bios\_uuid|
|VM Instance UUID|vm\_instance\_uuid|

|Field label|Column name|
|-----------|-----------|
|Managed object reference ID|morid|
|vCenter Instance UUID|vcenter\_uuid|
|vCenter Reference|vcenter\_ref|

|Field label|Column name|
|-----------|-----------|
|Region|region|
|Managed object reference ID|morid|
|vCenter Instance UUID|vcenter\_uuid|
|vCenter Reference|vcenter\_ref|
|Top level folder for VMs|folder\_moreid|
|Top level folder for hosts|host\_morid|

\*The VMware vCenter Datacenter \[cmdb\_ci\_vcenter\_datacenter\] table is extended from the \[cmdb\_ci\_logical\_datacenter\] table.

|Field label|Column name|
|-----------|-----------|
|Managed object reference ID|morid|
|vCenter Instance UUID|vcenter\_uuid|
|vCenter Reference|vcenter\_ref|
|Network accessible by either hosts or virtual machines|accessible|

\*The VMware vCenter Network \[cmdb\_ci\_vcenter\_network\] table is extended from the \[cmdb\_ci\_network\] table.

|Field label|Column name|
|-----------|-----------|
|VMCount|vm\_count|
|Host count|host\_count|

|Field label|Column name|
|-----------|-----------|
|Managed object reference ID|morid|
|vCenter Instance UUID|vcenter\_uuid|
|vCenter Reference|vcenter\_ref|
|Full path|fullpath|

|Field label|Column name|
|-----------|-----------|
|Managed object reference ID|morid|
|vCenter Instance UUID|vcenter|
|vCenter Reference|vcenter\_ref|
|Owner|owner|
|Owner Managed Object Reference ID|owner\_morid|
|CPU expandable|cpu\_expandable|
|CPU limit \(MHz\)|cpu\_limit\_mhz|
|CPU reserved \(MHz\)|cpu\_reserved\_mhz|
|CPU shares|cpu\_shares|
|Full path|fullpath|
|Memory expandable|mem\_expandable|
|Memory limit \(MB\)|mem\_limit\_mb|
|Memory reserved \(MB\)|mem\_reserved\_mb|
|Memory shares|mem\_shares|

|Field label|Column name|
|-----------|-----------|
|Managed object reference ID|morid|
|vCenter Instance UUID|vcenter\_uuid|
|Accessible|accessible|
|vCenter Reference|vcenter\_ref|
|Type|type|
|Capacity \(GB\)|capacity|
|Free space \(GB\)|freespace|
|URL|url|
|Clustered|clustered|

The VMware vCenter Datastore \[cmdb\_ci\_vcenter\_datastore\] table is extended from the \[cmdb\_ci\_datastore\] table.

|Field label|Column name|
|-----------|-----------|
|Managed object reference ID|morid|
|vCenter Instance UUID|vcenter\_uuid|
|Effective hosts|effectivehosts|
|vCenter Reference|vcenter\_ref|
|Effective CPU|effectivecpu|
|Effective memory|effectivememory|
|Number of effective hosts|effectivehosts|
|Number of hosts|numhosts|
|Total CPU|totalcpu|
|Total memory|totalmemory|
|Number of CPU cores|numcpucores|
|Number of CPU threads|numcputhreads|
|DRS Behavior|drs\_behavior|
|DRS Enabled|drs\_enabled|
|DRS VMotion Rate|drs\_vmotion\_rate|

\*The VMware vCenter Cluster \[cmdb\_ci\_vcenter\_cluster\] table is extended from the \[cmdb\_ci\_host\_cluster\] table.

|Field label|Column name|
|-----------|-----------|
|VM Group|vm\_group|
|Host Group|host\_group|
|Mandatory|mandatory|
|Affinity|affinity|

|Field label|Column name|
|-----------|-----------|
|Affinity|affinity|

The Cluster VM Affinity Rule Info \[cmdb\_ci\_cluster\_vm\_affinity\_rule\] table has Contains::Contained by relationship with cmdb\_ci\_vmware\_instance. This group has a set of VMs for which this affinity will be applied.

|Field label|Column name|
|-----------|-----------|
|Name|name|
|VMCount|vm\_count|
|Host count|host\_count|

Discovery also maps the relationships to VMs and to distributed virtual port groups.

|Field label|Column name|
|-----------|-----------|
|Name|name|
|vCenter Instance UUID|vcenter\_uuid|
|Distributed Virtual Switch Reference|dvs\_ref|

Discovery also maps the relationship to the distributed virtual switch.

You can add these related lists to view additional discovered data:

-   -   **Storage Volumes**

    The virtual disks for this virtual machine. This data is saved in the Storage Volume \[cmdb\_ci\_storage\_volume\] table with the value `type=v Disk`.

    |Field label|Column name|
    |-----------|-----------|
    |Name|name|
    |Size|size|

-   -   **Network Adapters**

    The virtual network adapters for the virtual disks. This data is saved in the Network Adapter \[cmdb\_ci\_network\_adapter\] table.

    |Field label|Column name|
    |-----------|-----------|
    |Name|name|
    |IP Address|ip\_address|
    |MAC address|mac\_address|
    |Netmask|netmask|


## vCenter discovery with Software Asset Management

If Software Asset Management is active, Discovery populates these vCenter tables using the VMWare - vCenter ESX Hosts License probe.

|Field label|Column name|
|-----------|-----------|
|vCenter Reference|vcenter\_ref|
|Cost Unit|cost\_unit|
|Edition|edition|
|Features|features|
|License Key|license\_key|
|Product Name|product\_name|
|Product Version|product\_version|
|Rights Owned|rights\_owned|
|Rights Used|rights\_used|

|Field label|Column name|
|-----------|-----------|
|Rights Used|rights\_used|
|Expiration Date|expiration\_date|
|Used Features|used\_features|
|License Key|license\_key|
|Software Install|software\_install|
|Used By|used\_by|

## vCenter relationships

Discovery automatically creates relationships for vCenter components using data from a key class. Subsequent discoveries use the same key class to automatically validate and remove relationships that are no longer valid.

vCenter CIs can be members of folders or clusters, which affect how Discovery creates their relationships.

-   If a CI is in a folder, Discovery creates a relationship between that CI and the folder. If that CI is not in a folder, Discovery creates the relationship between the CI and the datacenter. These vCenter CIs can be in a folder:
    -   VM Instance
    -   VM Template
    -   vCenter Network
    -   Datastore
    -   vCenter Folder
    -   vCenter Cluster
-   If an ESX server is in a cluster, Discovery creates a relationship between the ESX server and the cluster. If an ESX server is not a member of a cluster, then Discovery creates a relationship to the datacenter.
-   If a resource pool is in a cluster, Discovery creates a relationship between the resource pool and the cluster. If the resource pool is not a member of a cluster, then Discovery creates a relationship to the ESX server.

This diagram illustrates vCenter relationships:

![vCenter relationships](../image/vcenter-relationships.png "vCenter relationships")

<table id="table_fzd_bly_5p"><thead><tr><th>

Parent class

</th><th>

Relationship type

</th><th>

Child class

</th></tr></thead><tbody><tr><td>

Computer \[cmdb\_ci\_computer\]

</td><td>

Virtualized by::Virtualizes

</td><td>

ESX Server \[cmdb\_ci\_esx\_server\]**Note:** The relationship created from ESX Server and VM Instance to the Guest are created by business rule "Virtual Computer Check." The guest machine needs to be discovered after the VCenter is discovered to trigger the business rule and create such relationships.

</td></tr><tr><td>

Computer \[cmdb\_ci\_computer\]

</td><td>

Instantiates::Instantiated by

</td><td>

VM Instance \[cmdb\_ci\_vmware\_instance\]**Note:** The relationship created from ESX Server and VM Instance to the Guest are created by business rule "Virtual Computer Check." The guest machine needs to be discovered after the VCenter is discovered to trigger the business rule and create such relationships.

</td></tr><tr><td>

VMware Virtual Machine Instance \[cmdb\_ci\_vmware\_instance\]

</td><td>

Registered on::Has registered

</td><td>

ESX Server \[cmdb\_ci\_esx\_server\]

</td></tr><tr><td>

VMware Virtual Machine Instance \[cmdb\_ci\_vmware\_instance\]

</td><td>

Connected by::Connects

</td><td>

VMware vCenter Network \[cmdb\_ci\_vcenter\_network\]

</td></tr><tr><td>

Virtual Machine Template \[cmdb\_ci\_vmware\_template\]

</td><td>

Connected by::Connects

</td><td>

VMware vCenter Network \[cmdb\_ci\_vcenter\_network\]

</td></tr><tr><td>

VMware vCenter Network \[cmdb\_ci\_vcenter\_network\]

</td><td>

Provided by::Provides

</td><td>

ESX Server \[cmdb\_ci\_esx\_server\]

</td></tr><tr><td>

VMware vCenter Datastore \[cmdb\_ci\_vcenter\_datastore\]

</td><td>

Provides storage for::Stored on

</td><td>

VMware Virtual Machine Instance \[cmdb\_ci\_vmware\_instance\]

</td></tr><tr><td>

VMware vCenter Datastore \[cmdb\_ci\_vcenter\_datastore\]

</td><td>

Used by::Uses

</td><td>

ESX Server \[cmdb\_ci\_esx\_server\]

</td></tr><tr><td>

VMware vCenter Datastore \[cmdb\_ci\_vcenter\_datastore\]

</td><td>

Provides storage for::Stored on

</td><td>

Virtual Machine Template \[cmdb\_ci\_vmware\_template\]

</td></tr><tr><td>

VMware vCenter Cluster \[cmdb\_ci\_vcenter\_cluster\]

</td><td>

Members::Member of

</td><td>

ESX Server \[cmdb\_ci\_esx\_server\]

</td></tr><tr><td>

ESX Resource Pool \[cmdb\_ci\_esx\_resource\_pool\]

</td><td>

Defines resources for::Get resources from

</td><td>

VMware vCenter Cluster \[cmdb\_ci\_vcenter\_cluster\]

</td></tr><tr><td>

ESX Resource Pool \[cmdb\_ci\_esx\_resource\_pool\]

</td><td>

Defines resources for::Get resources from

</td><td>

ESX Server \[cmdb\_ci\_esx\_server\]

</td></tr><tr><td>

VMware vCenter Folder \[cmdb\_ci\_vcenter\_folder\]

</td><td>

Contains::Contained by

</td><td>

VMware vCenter Datastore \[cmdb\_ci\_vcenter\_datastore\]

</td></tr><tr><td>

VMware vCenter Folder \[cmdb\_ci\_vcenter\_folder\]

</td><td>

Contains::Contained by

</td><td>

VMware vCenter Folder \[cmdb\_ci\_vcenter\_folder\]

</td></tr><tr><td>

VMware vCenter Folder \[cmdb\_ci\_vcenter\_folder\]

</td><td>

Contains::Contained by

</td><td>

Virtual Machine Template \[cmdb\_ci\_vmware\_template\]

</td></tr><tr><td>

VMware vCenter Folder \[cmdb\_ci\_vcenter\_folder\]

</td><td>

Contains::Contained by

</td><td>

VMware Virtual Machine Instance \[cmdb\_ci\_vmware\_instance\]

</td></tr><tr><td>

VMware vCenter Datacenter \[cmdb\_ci\_vcenter\_datacenter\]

</td><td>

Contains::Contained by

</td><td>

VMware vCenter Network \[cmdb\_ci\_vcenter\_network\]

</td></tr><tr><td>

VMware vCenter Datacenter \[cmdb\_ci\_vcenter\_datacenter\]

</td><td>

Contains::Contained by

</td><td>

VMware Virtual Machine Instance \[cmdb\_ci\_vmware\_instance\]

</td></tr><tr><td>

VMware vCenter Datacenter \[cmdb\_ci\_vcenter\_datacenter\]

</td><td>

Contains::Contained by

</td><td>

ESX Server \[cmdb\_ci\_esx\_server\]

</td></tr><tr><td>

VMware vCenter Datacenter \[cmdb\_ci\_vcenter\_datacenter\]

</td><td>

Contains::Contained by

</td><td>

VMware vCenter Datastore \[cmdb\_ci\_vcenter\_datastore\]

</td></tr><tr><td>

VMware vCenter Datacenter \[cmdb\_ci\_vcenter\_datacenter\]

</td><td>

Contains::Contained by

</td><td>

VMware vCenter Folder \[cmdb\_ci\_vcenter\_folder\]

</td></tr><tr><td>

VMware vCenter Datacenter \[cmdb\_ci\_vcenter\_datacenter\]

</td><td>

Contains::Contained by

</td><td>

VMware vCenter Cluster \[cmdb\_ci\_vcenter\_cluster\]

</td></tr><tr><td>

VMware vCenter Datacenter \[cmdb\_ci\_vcenter\_datacenter\]

</td><td>

Contains::Contained by

</td><td>

Virtual Machine Template \[cmdb\_ci\_vmware\_template\]

</td></tr></tbody>
</table>## Cloud Management relationships

These additional relationships are created when Cloud Management \(CMP\) is active.

![vCenter relationships for Cloud Management](../image/CMPRelationshipsDiagram.png)

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|ESX Server \[cmdb\_ci\_esx\_server\]|Hosted on::Hosts|vCenter Datacenter \[cmdb\_ci\_vcenter\_datacenter\]|
|vCenter Folder \[cmdb\_ci\_vcenter folder\]|Hosted on::Hosts|vCenter Datacenter \[cmdb\_ci\_vcenter\_datacenter\]|
|vCenter Datacenter \[cmdb\_ci\_vcenter\_datacenter\]|Hosted on::Hosts|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|
|vCenter Cluster \[cmdb\_ci\_vcenter\_cluster\]|Hosted on::Hosts|vCenter Datacenter \[cmdb\_ci\_vcenter\_datacenter\]|
|Resource Pools \[cmdb\_ci\_esx\_resource\_pool\]|Hosted on::Hosts|vCenter Datacenter \[cmdb\_ci\_vcenter\_datacenter\]|
|VM Instance \[cmdb\_ci\_vmware\_instance\]|Hosted on::Hosts|vCenter Datacenter \[cmdb\_ci\_vcenter\_datacenter\]|
|VM Template \[cmdb\_ci\_vmware\_template\]|Hosted on::Hosts|vCenter Datacenter \[cmdb\_ci\_vcenter\_datacenter\]|
|vCenter Network \[cmdb\_ci\_vcenter\_network\]|Hosted on::Hosts|vCenter Datacenter \[cmdb\_ci\_vcenter\_datacenter\]|
|Distributed Virtual Switch \[cmdb\_ci\_vcenter\_dvs\]|Hosted on::Hosts|vCenter Datacenter \[cmdb\_ci\_vcenter\_datacenter\]|
|Distributed Virtual Port Group \[cmdb\_ci\_vcenter\_dv\_port\_group\]|Hosted on::Hosts|vCenter Datacenter \[cmdb\_ci\_vcenter\_datacenter\]|
|Datastore \[cmdb\_ci\_vcenter\_datastore\]|Hosted on::Hosts|vCenter Datacenter \[cmdb\_ci\_vcenter\_datacenter\]|
|Virtual Disk \[cmdb\_ci\_storage\_volume\]|Hosted on::Hosts|vCenter Datacenter \[cmdb\_ci\_vcenter\_datacenter\]|
|Virtual NIC \[cmdb\_ci\_vmware\_nic\]|Hosted on::Hosts|vCenter Datacenter \[cmdb\_ci\_vcenter\_datacenter\]|
|VM Template \[cmdb\_ci\_vmware\_template\]|Use End Point To::Use End Point From|Block Endpoint \[cmdb\_ci\_endpoint\_block\]|
|VM Instance cmdb\_ci\_vmware\_instance|Use End Point To::Use End Point From|Block Endpoint \[cmdb\_ci\_endpoint\_block\]|
|Virtual Disk \[cmdb\_ci\_storage\_volume\]|Implement End Point To::Implement End Point From|Block Endpoint \[cmdb\_ci\_endpoint\_block\]|
|Virtual NIC \[cmdb\_ci\_vmware\_nic\]|Implement End Point To::Implement End Point From|NIC Endpoint \[cmdb\_ci\_endpoint\_nic\]|
|VM Template \[cmdb\_ci\_vmware\_template\]|Use End Point To::Use End Point From|NIC Endpoint \[cmdb\_ci\_endpoint\_nic\]|
|VM Instance \[cmdb\_ci\_vmware\_instance\]|Use End Point To::Use End Point From|NIC Endpoint \[cmdb\_ci\_endpoint\_nic\]|

## VMware tags

You can attach tags to vSphere objects, such as virtual machines, through the vSphere interface. The tags can then be grouped into categories. Objects with tags are sortable and searchable based on the parameters you give the tags and categories. The [VMWare — vCenter VM Tags](vcenter-probes.md#section_ffy_jmz_mhb) probe discovers these tags. You can view the discovered tags by opening the virtual machine record in **cmdb\_ci\_vmware\_instance**. Then go to the **Key Values** tab.

|Field label and name|Description|
|--------------------|-----------|
|Configuration item \[configuration\_item\]|Referenced VM with tag attached in vCenter.|
|Key \[key\]|Category name of the tag applied to the resource in vCenter.|
|Tag \[tag\]|Source in vCenter from which tags are fetched. In this case, the value is always **Tags**.|
|Value \[value\]|Tag name that is applied to the resource in vCenter.|

**Parent Topic:**[Discovery for VMware vCenter](../concept/c_DiscoveryForVMwareVCenter.md)

