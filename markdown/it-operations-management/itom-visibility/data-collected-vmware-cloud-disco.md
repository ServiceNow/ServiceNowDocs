---
title: Data collected for VMware Cloud Discovery
description: Discovery collects information about VMware resources in your cloud service accounts.
locale: en-US
release: australia
product: ITOM Visibility
classification: itom-visibility
topic_type: reference
last_updated: "2026-03-23"
reading_time_minutes: 31
breadcrumb: [Cloud resource discovery references, Data collected by ITOM Visibility, ITOM Visibility reference, ITOM Visibility, IT Operations Management]
---

# Data collected for VMware Cloud Discovery

Discovery collects information about VMware resources in your cloud service accounts.

## Distributed Resource Scheduler \(DRS\) discovery

VMware Discovery collects these DRS settings and saves them to the DRS VM Config \[cmdb\_ci\_drs\_vm\_config\] table:

-   DRS settings of vCenter clusters.
-   DRS settings of VMs configured to override cluster behavior.

|Field label and Name|Description|
|--------------------|-----------|
|Cluster \[cluster\]|The vCenter cluster that the VM belongs to.|
|DRS behavior \[drs\_behavior\]|The VM-level Distributed Resource Scheduler behavior that overrides cluster defaults.|
|DRS enabled \[drs\_enabled\]|Indicates whether DRS is active for the VM.|
|Virtual machine \[virtual\_machine\]|The VM instance using these DRS settings.|

## VMware tags

VMware Cloud Discovery finds VMware tags from vCenter and saves them to the Key Value \[cmdb\_key\_value\] table.

|Field label and Name|Description|
|--------------------|-----------|
|Configuration item \[configuration\_item\]|Referenced VM with tag attached in vCenter.|
|Key \[key\]|Category name of the tag applied to the resource in vCenter.|
|Tag \[tag\]|Source in vCenter from which tags are fetched. In this case, the value is always **Tags**.|
|Value \[value\]|Tag name that's applied to the resource in vCenter.|

## Data collected for VMware vCenter Server

Discovery identifies and classifies information and data about VMware vCenter servers.

The vCenter table schema is illustrated in the following diagram:

![vCenter table schema](../image/vcenter_table_schema.png "vCenter table schema")

Several tables are cloud-agnostic tables, meaning that they can be populated for any cloud resource, not just vCenter resources. Look in the sub tables that extend the cloud-agnostic tables to find discovered configuration items \(CIs\).

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

|Field label and Name|Description|
|--------------------|-----------|
|Name \[name\]|The display name of the vCenter instance.|
|IP Address \[ip\_address\]|The IP address of the vCenter server.|
|API version \[api\_version\]|The version of the vCenter API in use.|
|Full name \[fullname\]|The full vCenter instance name returned by VMware.|
|Instance UUID \[instance\_uuid\]|A unique identifier assigned to the vCenter instance.|
|URL \[url\]|The endpoint URL used to connect to vCenter.|
|Fully qualified domain name \[fqdn\]|The fully qualified domain name of the vCenter server.|

The combination of the vCenter instance in the cmdb\_ci\_vcenter table and the object ID in the cmdb\_ci\_vm\_object table identifies a specific vCenter.

The tables extend from the Virtual Machine Objects \[cmdb\_ci\_vm\_object\] table, which holds object IDs for all cloud-based resources, except virtualization servers.

|Field label and Name|Description|
|--------------------|-----------|
|Cluster \[cluster\]|The vCenter cluster that the VM belongs to.|
|DRS behavior \[drs\_behavior\]|The VM-level Distributed Resource Scheduler behavior that overrides cluster defaults.|
|DRS enabled \[drs\_enabled\]|Indicates whether DRS is active for the VM.|
|Virtual machine \[virtual\_machine\]|The VM instance using these DRS settings.|

This table stores DRS behavior for the VMs that override the cluster behavior. For more information on DRS, see VMware's documentation on [Distributed Resource Scheduler](https://www.vmware.com/products/vsphere/drs-dpm.html).

|Field label and Name|Description|
|--------------------|-----------|
|Cluster \[cluster\]|The cluster that this VM group is associated with.|

The VMware vCenter VM group \[cmdb\_ci\_vcenter\_vm\_group\] table has Contains::Contained by relationship with cmdb\_ci\_vmware\_instance. This group has a set of VMs.

|Field label and Name|Description|
|--------------------|-----------|
|Cluster \[cluster\]|The cluster that this host group belongs to.|

The VMware vCenter Host Group \[cmdb\_ci\_vcenter\_host\_group\] table has Contains::Contained by relationship with cmdb\_ci\_vmware\_instance. This group has a set of hosts.

|Field label and Name|Description|
|--------------------|-----------|
|Rule UUID \[rule\_uuid\]|Unique identifier for the DRS rule in vCenter.|
|Active \[active\]|Whether the rule is currently enforced.|
|Cluster \[cluster\]|The cluster that the rule applies to.|

|Field label and Name|Description|
|--------------------|-----------|
|Name \[name\]|VM name as discovered from vCenter.|
|Template \[template\]|Indicates whether this VM is based on a template.|
|CPUs \[cpus\]|Number of assigned virtual CPUs.|
|Disks \[disks\]|Number of virtual disks attached to the VM.|
|Disks size \(GB\) \[disks\_size\]|Combined size of all VM disks.|
|Memory \(MB\) \[memory\]|Memory allocated to the VM.|
|Network adapters \[nics\]|Number of virtual NICs attached.|
|Image path \[image\_path\]|Path to the VM's image on the datastore.|
|State \[state\]|Current VM power or operational state.|
|vCenter Instance UUID \[vcenter\_uuid\]|Unique ID of the vCenter instance managing this VM.|
|vCenter Reference \[vcenter\_ref\]|Reference to the vCenter record in CMDB.|
|BIOS UUID \[bios\_uuid\]|Hardware-level VM UUID from VMware.|
|VM Instance UUID \[vm\_instance\_uuid\]|VMware-provided VM unique ID.|
|IP address \[ip\_address\]|Primary IP detected for the VM.|

|Field label and Name|Description|
|--------------------|-----------|
|Name \[name\]|Name of the port group.|
|vCenter Instance UUID \[vcenter\_uuid\]|vCenter instance that manages this port group.|
|Distributed Virtual Switch Reference \[dvs\_ref\]|Reference to the switch that the port group belongs to.|

|Field label and Name|Description|
|--------------------|-----------|
|Name \[The template name from VMWare.\]|Template name in vCenter.|
|CPUs \[cpus\]|Number of CPUs assigned when deployed.|
|Disks size \(GB\) \[disks\_size\]|Disk size of the template.|
|Guest ID \[guest\_id\]|VMware guest OS identifier.|
|Memory \(MB\) \[memory\]|Allocated template memory.|
|Image path \[image\_path\]|Path to the template image.|
|vCenter Instance UUID \[vcenter\_uuid\]|vCenter instance where the template resides.|
|vCenter Reference \[vcenter\_ref\]|CMDB reference to vCenter record.|
|Network adapters \[nics\]|Number of NICs defined in the template.|
|Base name \[base\_name\]|The base name used for naming VMs created from this template.|
|VM namer \[vm\_namer\]|VMware auto-naming method for derived VMs.|
|BIOS UUID \[bios\_uuid\]|Template UUID.|
|VM Instance UUID \[vm\_instance\_uuid\]|Unique template instance ID.|

|Field label and Name|Description|
|--------------------|-----------|
|Managed object reference ID \[morid\]|Unique Managed Object Reference ID in vCenter.|
|vCenter Instance UUID \[vcenter\_uuid\]|vCenter that owns this object.|
|vCenter Reference \[vcenter\_ref\]|CMDB reference to the vCenter record.|

|Field label and Name|Description|
|--------------------|-----------|
|Region \[region\]|Geographic or logical region of the datacenter.|
|Managed object reference ID \[morid\]|VMware Managed Object Reference ID.|
|vCenter Instance UUID \[vcenter\_uuid\]|vCenter that manages this datacenter.|
|vCenter Reference \[vcenter\_ref\]|CMDB reference back to vCenter.|
|Top-level folder for VMs \[folder\_moreid\]|Top-level folder where VMs reside.|
|Top-level folder for hosts \[host\_morid\]|Top-level folder for hosts.|

\*The VMware vCenter Datacenter \[cmdb\_ci\_vcenter\_datacenter\] table is extended from the \[cmdb\_ci\_logical\_datacenter\] table.

|Field label and Name|Description|
|--------------------|-----------|
|Managed object reference ID \[morid\]|Object reference ID in vCenter.|
|vCenter Instance UUID \[vcenter\_uuid\]|Parent vCenter instance.|
|vCenter Reference \[vcenter\_ref\]|CMDB reference to vCenter.|
|Network accessible by either hosts or virtual machines \[accessible\]|Whether hosts or VMs can connect to the network.|

\*The VMware vCenter Network \[cmdb\_ci\_vcenter\_network\] table is extended from the \[cmdb\_ci\_network\] table.

|Field label and Name|Description|
|--------------------|-----------|
|VMCount \[vm\_count\]|Number of VMs attached to the switch.|
|Host count \[host\_count\]|Number of ESXi hosts connected.|

|Field label and Name|Description|
|--------------------|-----------|
|Managed object reference ID \[morid\]|VMware folder identifier.|
|vCenter Instance UUID \[vcenter\_uuid\]|vCenter managing the folder.|
|vCenter Reference \[vcenter\_ref\]|CMDB reference to vCenter.|
|Full path \[fullpath\]|Full folder hierarchy path.|

|Field label and Name|Description|
|--------------------|-----------|
|Managed object reference ID \[morid\]|VMware Managed Object Reference ID.|
|vCenter Instance UUID \[vcenter\]|vCenter that manages this pool.|
|vCenter Reference \[vcenter\_ref\]|CMDB reference.|
|Owner \[owner\]|The VM or host that owns the pool.|
|Owner Managed Object Reference ID \[owner\_morid\]|Managed Object Reference of the owner.|
|CPU expandable \[cpu\_expandable\]|Whether CPU resources can exceed limits.|
|CPU limit \(MHz\) \[cpu\_limit\_mhz\]|Max CPU allocation in MHz.|
|CPU reserved \(MHz\) \[cpu\_reserved\_mhz\]|CPU reserved for the pool.|
|CPU shares \[cpu\_shares\]|CPU scheduling weight.|
|Full path \[fullpath\]|Location path in vCenter hierarchy.|
|Memory expandable \[mem\_expandable\]|Whether memory can exceed the configured maximum.|
|Memory limit \(MB\) \[mem\_limit\_mb\]|Memory limit in MB.|
|Memory reserved \(MB\) \[mem\_reserved\_mb\]|Memory guaranteed for the pool.|
|Memory shares \[mem\_shares\]|Memory scheduling weight.|

|Field label and Name|Description|
|--------------------|-----------|
|Managed object reference ID \[morid\]|ID of the datastore in vCenter.|
|vCenter Instance UUID \[vcenter\_uuid\]|Parent vCenter ID.|
|Accessible \[accessible\]|Indicates if hosts can access it.|
|vCenter Reference \[vcenter\_ref\]|CMDB reference.|
|Type \[type\]|Filesystem type \(NFS, VMFS, etc.\).|
|Capacity \(GB\) \[capacity\]|Total datastore capacity.|
|Free space \(GB\) \[freespace\]|Remaining space.|
|URL \[url\]|Unique locator.|
|Clustered \[clustered\]|Whether it belongs to a storage pod.|

The VMware vCenter Datastore \[cmdb\_ci\_vcenter\_datastore\] table is extended from the \[cmdb\_ci\_datastore\] table.

|Field label and Name|Description|
|--------------------|-----------|
|Managed object reference ID \[morid\]|Cluster ID.|
|vCenter Instance UUID \[vcenter\_uuid\]|Parent vCenter ID.|
|Effective hosts \[effectivehosts\]|Number of functioning hosts.|
|vCenter Reference \[vcenter\_ref\]|CMDB reference.|
|Effective CPU \[effectivecpu\]|Available CPU capacity.|
|Effective memory \[effectivememory\]|Available RAM.|
|Number of effective hosts \[effectivehosts\]|Count of hosts contributing resources.|
|Number of hosts \[numhosts\]|Total hosts.|
|Total CPU \[totalcpu\]|Total CPU capacity.|
|Total memory \[totalmemory\]|Total memory.|
|Number of CPU cores \[numcpucores\]|Total core count.|
|Number of CPU threads \[numcputhreads\]|Total thread count.|
|DRS Behavior \[drs\_behavior\]|Cluster-level DRS settings.|
|DRS Enabled \[drs\_enabled\]|Whether DRS is active.|
|DRS VMotion Rate \[drs\_vmotion\_rate\]|vMotion automation aggressiveness level.|

\*The VMware vCenter Cluster \[cmdb\_ci\_vcenter\_cluster\] table is extended from the \[cmdb\_ci\_host\_cluster\] table.

|Field label and Name|Description|
|--------------------|-----------|
|VM Group \[vm\_group\]|VM group to which the rule applies.|
|Host Group \[host\_group\]|Host group associated with the rule.|
|Mandatory \[mandatory\]|Indicates whether the rule must be strictly enforced.|
|Affinity \[affinity\]|Whether VMs must run together or be separated.|

|Field label and Name|Description|
|--------------------|-----------|
|Affinity \[affinity\]|Defines whether grouped VMs must stay together.|

The Cluster VM Affinity Rule Info \[cmdb\_ci\_cluster\_vm\_affinity\_rule\] table has Contains::Contained by relationship with cmdb\_ci\_vmware\_instance. This group has a set of VMs for which this affinity is applied.

|Field label and Name|Description|
|--------------------|-----------|
|Name \[name\]|The name of the distributed virtual switch as defined in vCenter.|
|VMCount \[vm\_count\]|The number of virtual machines currently connected to this distributed switch.|
|Host count \[host\_count\]|The number of ESXi hosts participating in this distributed switch.|

Discovery also maps the relationships to VMs and to distributed virtual port groups.

|Field label and Name|Description|
|--------------------|-----------|
|Name \[name\]|The name of the port group that provides network configuration for connected VMs.|
|vCenter Instance UUID \[vcenter\_uuid\]|The VMware-generated UUID of the vCenter instance that manages this port group.|
|Distributed Virtual Switch Reference \[dvs\_ref\]|The switch to which this port group belongs.|

Discovery also maps the relationship to the distributed virtual switch.

You can add these related lists to view additional discovered data:

-   -   **Storage Volumes**

    The virtual disks for this virtual machine. This data is saved in the Storage Volume \[cmdb\_ci\_storage\_volume\] table with the value `type=v Disk`.

    |Field label and Name|Description|
    |--------------------|-----------|
    |Name \[name\]|Name of the storage volume.|
    |Size \[size\]|Size of the disk/volume.|

-   -   **Network Adapters**

    The virtual network adapters for the virtual disks. This data is saved in the Network Adapter \[cmdb\_ci\_network\_adapter\] table.

    |Field label and Name|Description|
    |--------------------|-----------|
    |Name \[name\]|NIC name.|
    |IP Address \[ip\_address\]|Assigned IP.|
    |MAC address \[mac\_address\]|NIC MAC address.|
    |Netmask \[netmask\]|Subnet mask.|


## vCenter discovery with Software Asset Management

If Software Asset Management is active, Discovery populates these vCenter tables using the VMWare - vCenter ESX Hosts License probe.

|Field label and Name|Description|
|--------------------|-----------|
|vCenter Reference \[vcenter\_ref\]|The reference link to the vCenter instance that owns this license.|
|Cost Unit \[cost\_unit\]|The unit used by VMware to measure license cost.|
|Edition \[edition\]|The edition level of the VMware product.|
|Features \[features\]|The list of capabilities enabled by this license.|
|License Key \[license\_key\]|The VMware-issued alphanumeric software license key.|
|Product Name \[product\_name\]|The VMware product that the license applies to.|
|Product Version \[product\_version\]|The version of the licensed product.|
|Rights Owned \[rights\_owned\]|Total entitlements purchased under this license.|
|Rights Used \[rights\_used\]|Entitlements currently consumed by vCenter hosts.|

|Field label and Name|Description|
|--------------------|-----------|
|Rights Used \[rights\_used\]|Number of license units currently in use.|
|Expiration Date \[expiration\_date\]|The date the license expires.|
|Used Features \[used\_features\]|The specific product features being used.|
|License Key \[license\_key\]|The license key to which this usage record applies.|
|Software Install \[software\_install\]|The installation record tied to the consumed license.|
|Used By \[used\_by\]|The asset or component consuming the license.|

## vCenter relationships

Discovery automatically creates relationships for vCenter components using data from a key class. Subsequent discoveries use the same key class to automatically validate and remove relationships that are no longer valid.

vCenter CIs can be members of folders or clusters, which affect how Discovery creates their relationships.

-   If a CI is in a folder, Discovery creates a relationship between that CI and the folder. If that CI isn’t in a folder, Discovery creates the relationship between the CI and the datacenter. These vCenter CIs can be in a folder:
    -   VM Instance
    -   VM Template
    -   vCenter Network
    -   Datastore
    -   vCenter Folder
    -   vCenter Cluster
-   If an ESX server is in a cluster, Discovery creates a relationship between the ESX server and the cluster. If an ESX server isn’t a member of a cluster, then Discovery creates a relationship to the datacenter.
-   If a resource pool is in a cluster, Discovery creates a relationship between the resource pool and the cluster. If the resource pool isn’t a member of a cluster, then Discovery creates a relationship to the ESX server.

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

ESX Server \[cmdb\_ci\_esx\_server\]**Note:** The relationship created from ESX Server and VM Instance to the Guest are created by business rule "Virtual Computer Check." The guest machine must be discovered after the VCenter is discovered to trigger the business rule and create such relationships.

</td></tr><tr><td>

Computer \[cmdb\_ci\_computer\]

</td><td>

Instantiates::Instantiated by

</td><td>

VM Instance \[cmdb\_ci\_vmware\_instance\]**Note:** The relationship created from ESX Server and VM Instance to the Guest are created by business rule "Virtual Computer Check." The guest machine must be discovered after the VCenter is discovered to trigger the business rule and create such relationships.

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

VMware vCenter datacenters \[cmdb\_ci\_vcenter\_datacenter\]

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

You can attach tags to vSphere objects, such as virtual machines, through the vSphere interface. The tags can then be grouped into categories. Objects with tags are sortable and searchable based on the parameters that you give the tags and categories. The [VMWare — vCenter VM Tags](vcenter-probes.md#section_ffy_jmz_mhb) probe discovers these tags. You can view the discovered tags by opening the virtual machine record in **cmdb\_ci\_vmware\_instance**. Then go to the **Key Values** tab.

|Field label and Name|Description|
|--------------------|-----------|
|Configuration item \[configuration\_item\]|Referenced VM with tag attached in vCenter.|
|Key \[key\]|Category name of the tag applied to the resource in vCenter.|
|Tag \[tag\]|Source in vCenter from which tags are fetched. In this case, the value is **Tags**.|
|Value \[value\]|Tag name that's applied to the resource in vCenter.|

## Datastore data collected by Discovery

Discovery identifies each datastore in the system and creates the relationships with the virtual machines and the ESX servers that use these datastores. Discovery uses the VMWare - vCenter Datastores probe to collect this data.

|Field label and Name|Table Name|Description|
|--------------------|----------|-----------|
|Accessible \[accessible\]|VMware vCenter Datastore \[cmdb\_ci\_vcenter\_datastore\]|Whether the datastore is collected or not|
|Capacity \(GB\) \[capacity\]|VMware vCenter Datastore \[cmdb\_ci\_vcenter\_datastore\]|Amount of space provided by the datastore.|
|Clustered \[clustered\]|VMware vCenter Datastore \[cmdb\_ci\_vcenter\_datastore\]|When the datastore is clustered \(belongs to a storage pod\).|
|Free space \(GB\) \[freespace\]|VMware vCenter Datastore \[cmdb\_ci\_vcenter\_datastore\]|Amount of space still available on the datastore.|
|Type \[type\]|VMware vCenter Datastore \[cmdb\_ci\_vcenter\_datastore\]|The type of file system volume, such as WFS or NFS.|
|URL \[url\]|VMware vCenter Datastore \[cmdb\_ci\_vcenter\_datastore\]|The unique URL locator for the datastore.|

## HostMounts

Discovery uses both the VMWare - vCenter ESX Hosts and VMWare - vCenter Datastores probes to collect datastore host mount data.

|Field label and Column|Table|Description|
|----------------------|-----|-----------|
|Accessible \[accessible\]|VMware Datastore HostMount \[vcenter\_datastore\_hostmount\]|Whether the ESXi host can access the datastore.|
|Access Mode \[access\_mode\]|VMware Datastore HostMount \[vcenter\_datastore\_hostmount\]|The mode in which the ESXi host accesses the datastore.|
|VMware vCenter Datastore \[datastore\]|VMware Datastore HostMount \[vcenter\_datastore\_hostmount\]|The datastore mounted on this ESXi host.|
|ESX Server \[esx\_server\]|VMware Datastore HostMount \[vcenter\_datastore\_hostmount\]|The ESXi host that the datastore is mounted on.|
|vCenter Reference \[vcenter\_ref\]|VMware Datastore HostMount \[vcenter\_datastore\_hostmount\]|The vCenter instance that manages this mount.|

## Datastore Discovery

A datastore is a collection of one or more physical disks, such as an iSCSI disk, and can be used by more than one ESXi host. However, a physical disk can only connect to one datastore. Because ESXi hosts can share datastores, it's easy to move virtual machines between hosts that have a common datastore.

**Note:** From the perspective of a virtual machine attached to a datastore, storage is provided by a single disk.

The advantages to connecting a datastore to multiple disks are:

-   The ability to mirror the disks for failover protection.
-   The ease of adding storage to the datastore.

For information about the tables used by Discovery to store data for physical disks and their relationship to datastores and ESXi hosts, see, ESXi server discovery.

In this example configuration, two ESXi hosts share a common datastore that uses different types of storage.

![Datastore Discovery](../image/DatastoreDiscoveryDiagram.png "Datastore Discovery with different storage types")

## Relationships

ServiceNow provides tables that contain the relationships between an ESXi host and its datastore and the specific disks to which the datastore is connected.

ServiceNow Discovery establishes the relationships between a datastore, the disks attached to the datastore, and the ESXi server that hosts the virtual machines using that datastore. From the perspective of the ESXi host, iSCSI and fibre channel disks connected to the datastore are treated as physical disks. Discovery doesn’t show the direct relationship of the storage disks to the ESXi host.

**Note:** Storage can be hosted on computers that aren’t discovered by Discovery. ESXi hosts are discovered through vCenter, and storage is discovered separately through CIM. The system can only establish the relationship between the two when storage is discovered before ESXi.

|Table|Description|
|-----|-----------|
|cmdb\_ci\_vcenter\_datastore\_disk|Stores the relationship of the physical disk to the datastore.|
|vcenter\_datastore\_hostmount|Stores the relationship between the datastore and the ESXi server to which it’s connected.|
|cmdb\_ci\_disk|Contains the physical disks connected directly to the datastore. This table also contains a reference to the ESXi host.|
|cmdb\_ci\_fc\_disk|Contains the fibre channel disks in a storage area network \(SAN\) connected to the datastore. This table also contains a reference to the ESXi host.|
|cmdb\_ci\_iscsi\_disk|Contains the iSCSI disks in an IP network connected to the datastore. This table also contains a reference to the ESXi host.|

## VM Instance state and status fields

These tables represent the state and status of the cmdb\_ci\_vm\_instance in various flows such as vCenter Discovery and vCenter Events and the business rules which are triggered.

<table id="table_dmt_nxx_mxb"><thead><tr><th>

Source

</th><th>

Script or Event name

</th><th>

Field name

</th><th>

VM previous state

</th><th>

VM new state

</th></tr></thead><tbody><tr><td>

vCenter Discovery

</td><td>

VCenterVMsSensor

</td><td>

Install Status

</td><td>

Retired

</td><td>

Installed

</td></tr><tr><td>

vCenter Discovery

</td><td>

VCenterDatacentersSensor

</td><td>

Install Status

 State

 Operational status

</td><td>

Installed

</td><td>

Retired

 Terminated

 Non-operational

</td></tr></tbody>
</table><table id="table_kvr_2zx_mxb"><thead><tr><th>

Source

</th><th>

Script or Event name

</th><th>

Field name

</th><th>

VM previous state

</th><th>

VM new state

</th></tr></thead><tbody><tr><td>

vCenter events

</td><td>

VCenterVmStateUpdater

 powerOnEvtsToUse = \[ 'VmPoweredOffEvent', 'VmPowerOffOnIsolationEvent', 'VmShutdownOnIsolationEvent', 'VmSuspendedEvent' \],

</td><td>

Install Status

 State

</td><td>

Installed

 Any

</td><td>

Installed

 ON

</td></tr><tr><td>

vCenter events

</td><td>

powerOffEvtsToUse = \[ 'VmPoweredOnEvent', 'DrsVmPoweredOnEvent', 'VmRestartedOnAlternateHostEvent', 'VmSuspendedEvent' \],

</td><td>

Install Status

 State

</td><td>

Installed

 Any

</td><td>

Installed

 OFF

</td></tr><tr><td>

vCenter events

</td><td>

suspendEvtsToUse = \[ 'VmPoweredOnEvent', 'DrsVmPoweredOnEvent', 'VmRestartedOnAlternateHostEvent', 'VmPoweredOffEvent', 'VmPowerOffOnIsolationEvent' \]

</td><td>

Install Status

 State

</td><td>

Installed

 Any

</td><td>

Installed

 Paused

</td></tr><tr><td>

vCenter events

</td><td>

VmRemovedEvent

</td><td>

Install Status

 State

</td><td>

Installed

 Any

</td><td>

Retired

 Terminated

</td></tr></tbody>
</table><table id="table_uc2_g1y_mxb"><thead><tr><th>

Business rule

</th><th>

Field name

</th><th>

Plugin name

</th></tr></thead><tbody><tr><td>

Cascade Operational Status to vminstance

</td><td>

cmdb\_ci\_server: Operational status

</td><td>

Pattern Designer

</td></tr><tr><td>

Sync Ops Status for CMDB CI

</td><td>

-   cmdb\_ci: Operational status, Install Status
-   cmdb\_ci\_hardware: Operational status, Hardware Status, Substatus

</td><td>

CMDB

</td></tr></tbody>
</table>## ESXi server discovery

Discovery identifies and classifies information about ESXi servers and ESXi resource pools through the discovery of vCenter and not from the direct discovery of any ESXi servers.

**Important:** ESXi server discovery is done through vCenter. Don’t specify the IP address of the ESXi server in a Discovery Schedule. Instead, discover the vCenter through the Discovery Schedule.

## Required Roles

Users with the **itil** and **asset** roles can access ESXii and ESXi configuration item \(CI\) records. To run discovery on vCenter servers, users must have the **discovery\_admin** role.

## Credentials

To run a complete Discovery of vCenter/ESXi servers, you need vCenter credentials. If the vmapp port probe is turned off, you must use Windows credentials to access the Windows host on which the vCenter server runs.

**Note:** Make sure to select a credential Type of VMware.

## ESXi server Discovery Components

Discovery identifies ESXi servers based on the correlation ID \(BIOS UUID\), when the hardware manufacturer is on a certified inclusion list. So if the manufacturer is in the compatible manufacturers list, the correlation-id must be unique. If the manufacturer isn’t on the certified inclusion list, we check for the Managed Object Reference ID \(MORID\) and Serial Number as well. After running the vCenter classifier, Discovery launches the VMware - vCenter datacenters probe, which launches the probes that explore the ESXi server. For the complete list of vCenter probes, see [List of Discovery probes](r_ListOfDiscoveryProbes.md).

|Component and Name|Description|
|------------------|-----------|
|Classifier \[vCenter\]|Classifies standalone vCenter servers.|
|Probe \[VMWare - vCenter ESX Hosts\]|Creates records for ESXi servers and host mounts. Creates relationships between ESXi servers and vCenter components. Triggers probes for storage Discovery.|
|Probe \[VMWare - vCenter ESX Hosts Storage\]|Creates records for ESXi host hardware: network adapters, disks, HBAs, FC ports, iSCSI, and FC disks. Creates relationships between DAS/iSCSI/FC disks and datastore disks.|

## Data collected

Basic server data from ESXi hosts is collected by the VMware - vCenter ESX Hosts probe.

|Field label and Name|Table Name|Description|
|--------------------|----------|-----------|
|Operating System \[os\]|cmdb\_ci\_esx\_server|The OS version running on the ESXi host.|
|OS Version \[os\_version\]|cmdb\_ci\_computer|Detailed OS build or release information.|
|Name \[name\]|cmdb\_ci\_esx\_server|Hostname of the ESXi server.|
|DNS domain \[dns\_domain\]|cmdb\_ci\_esx\_server|Domain associated with the ESXi host.|
|Manufacturer \[manufacturer\]|cmdb\_ci\_computer|Hardware vendor of the ESXi host.|
|Serial number \[serial\_number\]|cmdb\_ci\_computer|Physical server hardware serial number.|
|CPU type \[cpu\_type\]|cmdb\_ci\_esx\_server|The CPU model used by the ESXi host.|
|CPU speed \(MHz\) \[cpu\_speed\]|cmdb\_ci\_esx\_server|Clock speed of the processors.|
|CPU count \[cpu\_count\]|cmdb\_ci\_esx\_server|Number of physical CPUs.|
|CPU core count \[cpu\_core\_count\]|cmdb\_ci\_computer|Total number of cores across all CPUs.|
|CPU manufacturer \[cpu\_manufacturer\]|cmdb\_ci\_esx\_server|Vendor of the CPU hardware.|
|Model ID \[model\_id\]|cmdb\_ci\_computer|Hardware model identifier.|
|RAM \(MB\) \[ram\]|cmdb\_ci\_esx\_server|Total physical memory installed.|
|Disk space \(GB\) \[disk\_space\]|cmdb\_ci\_esx\_server|Total disk capacity available.|
|Type \[type\]|cmdb\_ci\_disk|Type of disk.|
|Model ID \[model\_id\]|cmdb\_ci\_disk|Hardware identifier for the disk.|
|Disk space \(GB\) \[disk\_space\]|cmdb\_ci\_disk|Disk capacity of the individual disk.|
|Name \[name\]|cmdb\_ci\_disk|Disk name as detected by ESXi.|
|Name \[name\]|cmdb\_ci\_network\_adapter|Network adapter name.|
|IP address \[ip\_address\]|cmdb\_ci\_network\_adapter|IP assigned to the NIC.|
|MAC address \[mac\_address\]|cmdb\_ci\_network\_adapter|Hardware address of the NIC.|
|Netmask \[netmask\]|cmdb\_ci\_network\_adapter|Subnet mask of the NIC.|
|Managed object reference ID \[morid\]|Visualization Server \[cmdb\_ci\_virtualization\_server\]|Managed Object Reference ID.|
|Serial Number \[serial\_number\]|Serial Number \[cmdb\_serial\_number\]|Serial number record for CMDB correlation.|

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

Resource pools are configured in vCenter and define the maximum amount of resources that virtual machines using that pool can consume. If the ESXi server has additional resources to spare, an ESXi server property enables resource pools to expand. The **Name** and **Owner** fields of each resource pool on the ESXi server must be configured within the ServiceNow AI Platform

in the ESXi Resource Pool \[cmdb\_ci\_esx\_resource\_pool\] table. When Orchestration for VMware executes its manual provisioning tasks, the provisioner must select the proper resource pool for the virtual server requested. Discovery finds resource pools on ESXi machines and populates the fields on the ESXi Resource Pool form automatically. For more information, see [Configure ESXi resource pools](../task/t_ConfigureESXResourcePools.md).

ESXi resource pools require the Orchestration - VMware Support plugin.

**Note:** Confirm that vCenter and the ESXi server have been fully configured, including the creation of the templates and resource pools.

|Field label and Name|Table|Source|Description|
|--------------------|-----|------|-----------|
|CPU expandable \[cpu\_expendable\]|ESXi Resource Pool \[cmdb\_ci\_esx\_resource\_pool\]|VMWare - vCenter Clusters probe|Whether the resource pool can exceed CPU allocation limits.|
|CPU limit \(MHz\) \[cpu\_limit\_mhz\]|ESXi Resource Pool \[cmdb\_ci\_esx\_resource\_pool\]|VMWare - vCenter Clusters probe|Maximum CPU allocation.|
|CPU reserved \(MHz\) \[cpu\_reserved\_mhz\]|ESXi Resource Pool \[cmdb\_ci\_esx\_resource\_pool\]|VMWare - vCenter Clusters probe|CPU guaranteed to the pool.|
|CPU shares \[cpu\_shares\]|ESXi Resource Pool \[cmdb\_ci\_esx\_resource\_pool\]|VMWare - vCenter Clusters probe|CPU priority weight.|
|Full path \[fullpath\]|ESXi Resource Pool \[cmdb\_ci\_esx\_resource\_pool\]|VMWare - vCenter Clusters probe|vCenter folder path.|
|Memory expandable \[mem\_expandable\]|ESXi Resource Pool \[cmdb\_ci\_esx\_resource\_pool\]|VMWare - vCenter Clusters probe|Whether memory can exceed the configured maximum.|
|Memory limit \(MB\) \[mem\_limit\_mb\]|ESXi Resource Pool \[cmdb\_ci\_esx\_resource\_pool\]|VMWare - vCenter Clusters probe|Maximum memory.|
|Memory reserved \(MB\) \[mem\_reserved\_mb\]|ESXi Resource Pool \[cmdb\_ci\_esx\_resource\_pool\]|VMWare - vCenter Clusters probe|Memory guaranteed to the pool.|
|Memory shares \[mem\_shares\]|ESXi Resource Pool \[cmdb\_ci\_esx\_resource\_pool\]|VMWare - vCenter Clusters probe|Memory scheduling weight.|
|Owner \[owner\]|ESXi Resource Pool \[cmdb\_ci\_esx\_resource\_pool\]|VMWare - vCenter Clusters probe|Host or VM owning the pool.|
|Owner Managed Object Reference ID \[owner\_morid\]|ESXi Resource Pool \[cmdb\_ci\_esx\_resource\_pool\]|VMWare - vCenter Clusters probe|VMware reference ID of the owner.|

## Standalone ESXi discovery

Standalone ESXi discovery supports discovery of individual ESXi servers that host virtual machines \(VMs\) and related components without a vCenter. Various CIs and relationships are discovered as part of a discovery schedule.

Required roles:

Users with the **itil** and **asset** roles can access ESXi configuration item \(CI\) records. To run a standalone ESXi discovery, users must have the **discovery\_admin** role.

## VMware credentials

To run a standalone ESXi discovery, you need VMware credentials. Create the credentials by navigating to **Discovery** &gt; **Credentials** &gt; **VMware Credentials.**

If you use a domain account to access the ESXi host, specify the domain with the user name in the credential record in one of the supported formats, such as **Domain\\UserName**.

**Note:** The VMware credentials must have a read-only role in the ESXi host.

## Requirements

-   Make sure the Discovery \(com.snc.discovery\) plugin is installed and activated and that you have upgraded to Australia or later.
-   Activate the ESXi trigger probe. Navigate to the Trigger Probe \[trigger\_probe\_m2m\] table. The esxi record is inactive by default. Mark Active as true to enable Standalone ESXi discovery.
-   Create a new Discovery schedule for the host with the appropriate IP address of the ESXi host.

**Note:** If both SSH and ESXi are triggered, SSH is launched first and may cause Discovery to complete with the message "ESX Discovery is only supported through the vCenter." In this case, open the UNIX - Classify probe and set ESX - OS inactive.

## ESXi server Discovery Components

Discovery identifies ESXi servers based on the correlation ID \(BIOS UUID\), when the hardware manufacturer is on a certified inclusion list. If the manufacturer is on the list, the correlation ID must be unique. If the manufacturer isn’t on the certified inclusion list, the Managed Object Reference ID \(MORID\) and Serial Number are checked as well.

After Shazzam runs, it checks for the port probe esxi. Discovery then launches the VMWare - Standalone ESXi Server probe, which then launches the probes that explore the ESXi server. Other existing Discovery probes are also launched. For the complete list of probes, see [List of Discovery probes](r_ListOfDiscoveryProbes.md).

<table id="table_jmv_4df_4nb"><thead><tr><th>

Component and Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

IP Service \[ESXi\]

</td><td>

IP Service ESXi - VMWare VM console is defined for the Port 902.

</td></tr><tr><td>

Port Probe \[esxi\]

</td><td>

ESXi Server Appliance web user interface. It’s triggered by the IP Service ESXi and it triggers the probe VMWare - Standalone ESXi Server.

</td></tr><tr><td>

Probe \[VMWare - Standalone ESXi Server\]

</td><td>

Probe to get information about an ESXi server.

</td></tr><tr><td>

Probe \[VMWare - vCenter ESX Hosts\]

</td><td>

Creates records for ESXi servers and host mounts. Triggers other probes.-   VMware - vCenter ESX Hosts Storage
-   VMware - vCenter Datastores
-   VMware - vCenter Networks
-   VMware -vCenter VMs

</td></tr><tr><td>

Probe \[VMWare - vCenter ESX Hosts Storage\]

</td><td>

Creates records for ESXi host hardware: network adapters, disks, HBAs, FC ports, iSCSI, and FC disks. Creates relationships between DAS/iSCSI/FC disks and datastore disks.

</td></tr></tbody>
</table>Basic server data from ESXi hosts is collected by the VMware - vCenter ESX Hosts probe.

## ESXi Standalone server data

Discovery uses multiple existing probes to collect this data from ESXi. The data is saved in various tables. Some of the CIs, which have the "server" field have a reference to ESXi Host \(for example, cmdb\_ci\_esx\_server\).

|Field label and Name|Description|
|--------------------|-----------|
|Name \[name\]|VM name.|
|Memory \(MB\) \[memory\]|RAM assigned.|
|CPUs \[cpus\]|Number of vCPUs.|
|Disks \[disks\]|Number of VM disks.|
|Network adapters \[nics\]|Count of NICs.|
|Object ID \[object\_id\]|Unique object ID.|
|Server \[server\]|ESXi host running the VM.|
|State \[state\]|Power state.|
|Correlation ID \[correlation\_id\]|Unique VM identifier for correlation.|
|VM Instance UUID \[vm\_instance\_uuid\]|ESXi VM ID.|
|Status \[install\_status\]|CMDB install status.|

|Field label and Name|Description|
|--------------------|-----------|
|Name \[name\]|Datastore name.|
|Capacity \(GB\) \[capacity\]|Total storage size.|
|Free space \(GB\) \[freespace\]|Available storage.|
|Accessible \[accessible\]|Whether the datastore is reachable.|
|Type \[type\]|Filesystem type.|
|Object ID \[object\_id\]|Unique datastore ID.|
|Server \[server\]|ESXi host providing the datastore.|
|URL \[url\]|Datastore path.|
|Status \[install\_status\]|CMDB install status.|

|Field label and Name|Description|
|--------------------|-----------|
|Name \[name\]|Network name.|
|Object ID \[object\_id\]|Unique network ID.|
|Server \[server\]|ESXi host providing network connectivity.|
|Status \[install\_status\]|CMDB install status.|

|Field label and Name|Description|
|--------------------|-----------|
|Name \[name\]|NIC name.|
|MAC Address \[mac\_address\]|NIC hardware address.|
|IP Address \[ip\_address\]|Assigned IP.|
|Netmask \[netmask\]|Subnet mask.|
|Configuration Item \[cmdb\_ci\]|CI that owns this NIC.|
|Object ID \[object\_id\]|Unique NIC ID.|
|Mac manufacturer \[mac\_manufacturer\]|Vendor of the NIC.|
|DHCP Enabled \[dhcp\_enabled\]|Whether DHCP is active.|
|Status \[install\_status\]|CMDB install status.|

|Field label and Name|Description|
|--------------------|-----------|
|VMware vCenter Datastore \[datastore\]|Mounted datastore.|
|ESX Server \[esx\_server\]|Host using the datastore.|
|Accessible \[accessible\]|Whether the datastore is accessible.|
|Access Mode \[access\_mode\]|Read/write permissions.|

|Field label and Name|Description|
|--------------------|-----------|
|Name \[name\]|Disk name.|
|Manufacturer \[manufacturer\]|Disk vendor.|
|Location \[location\]|Disk physical/virtual location.|
|Description \[short\_description\]|Short description.|
|Class \[sys\_class\_name\]|CMDB class.|
|Updated \[sys\_updated\_on\]|Timestamp of last update.|
|Maintenance schedule \[maintenance\_schedule\]|Maintenance timing.|
|Correlation ID \[correlation\_id\]|Identifier linking disk to datastore.|
|Datastore \[datastore\]|Associated datastore.|
|Status \[install\_status\]|CMDB status.|

|Field label and Name|Description|
|--------------------|-----------|
|Name \[name\]|Resource pool name.|
|CPU reserved \(MHz\) \[cpu\_reserved\_mhz\]|Guaranteed CPU.|
|CPU limit \(MHz\) \[cpu\_limit\_mhz\]|Maximum CPU.|
|CPU shares \[cpu\_shares\]|CPU priority.|
|Memory reserved \(MB\) \[mem\_reserved\_mb\]|Guaranteed memory.|
|Memory limit \(MB\) \[mem\_limit\_mb\]|Maximum memory.|
|Memory shares \[mem\_shares\]|Memory weight.|
|Object ID \[object\_id\]|Unique pool ID.|
|Server \[server\]|ESXi host.|
|Managed object reference ID \[morid\]|Managed Object Reference ID.|
|Status \[install\_status\]|CMDB install status.|

|Field label and Name|Description|
|--------------------|-----------|
|Name \[name\]|ESXi hostname.|
|Manufacturer \[manufacturer\]|Vendor name.|
|Model ID \[model\_id\]|Server hardware model.|
|Operating System \[os\]|OS version.|
|OS Version \[os\_version\]|Detailed OS version.|
|Description \[short\_description\]|Summary information.|
|Class \[sys\_class\_name\]|CMDB class.|
|Status \[install\_status\]|CMDB status.|

|Field label and Name|Description|
|--------------------|-----------|
|Name \[name\]|NIC name.|
|Mac Address \[mac\_address\]|NIC hardware address.|
|Netmask \[netmask\]|Subnet mask.|
|Configuration Item \[cmdb\_ci\]|The CI owning this adapter.|
|Mac manufacturer \[mac\_manufacturer\]|NIC vendor.|
|DHCP Enabled \[dhcp\_enabled\]|Whether DHCP is used.|
|Status \[install\_status\]|CMDB install status.|

|Field label and Name|Description|
|--------------------|-----------|
|Name \[name\]|Disk name.|
|Computer \[computer\]|System owning the disk.|
|Size \[size\]|Disk capacity.|
|Manufacturer \[manufacturer\]|Disk vendor.|
|Model ID \[model\_id\]|Model identifier.|
|Status \[install\_status\]|CMDB install status.|

|Field label and Name|Description|
|--------------------|-----------|
|Name \[name\]|HBA name.|
|Model ID \[model\_id\]|HBA model number.|
|Computer \[computer\]|ESXi host.|
|WWNN \[wwnn\]|Worldwide Node Name.|
|Status \[install\_status\]|CMDB install status.|

|Field label and Name|Description|
|--------------------|-----------|
|Name \[name\]|Port name.|
|WWNN \[wwnn\]|Node Name.|
|WWPN \[wwpn\]|Port Name.|
|Speed \[speed\]|Link speed.|
|Controller \[controller\]|HBA controller.|
|Computer \[computer\]|Host system.|
|Status \[install\_status\]|CMDB status.|

|Field label and Name|Description|
|--------------------|-----------|
|Name \[name\]|Disk name.|
|Computer \[computer\]|Host accessing the disk.|
|Size \[size\]|Disk size.|
|Provided by \[provided\_by\]|Storage system provider.|
|IQN \[iqn\]|iSCSI Qualified Name.|
|Device LUN \[device\_lun\]|Logical Unit Number.|
|Storage type \[storage\_type\]|Storage type.|
|Status \[install\_status\]|CMDB status.|

|Field label and Name|Description|
|--------------------|-----------|
|Name \[name\]|Disk name.|
|Computer \[computer\]|Host using this disk.|
|Size \[size\]|Disk capacity.|
|Provided by \[provided\_by\]|Storage array.|
|Device LUN \[device\_lun\]|LUN identifier.|
|WWN \[wwn\]|Worldwide Name.|
|Status \[install\_status\]|CMDB install status.|

|Field label and Name|Description|
|--------------------|-----------|
|IP Address \[ip\_address\]|Assigned network address.|
|IP version \[ip\_version\]|IPv4 or IPv6.|
|Netmask \[netmask\]|Subnet mask.|
|Nic \[nic\]|NIC owning the IP.|
|Status \[install\_status\]|CMDB status.|

## Relationships

![Flowchart of standalone ESXi discovery relationships](../image/standalone_ESXi_relationships_.png "Standalone ESXi discovery relationships")

## Resource pools

Standalone ESXi discovery also fetches the resource pools on the host including the root resource pool. This root resource pool is hidden for every ESXi host. The root resource pool may not be visible in the VSphere web client for the ESXi host, but you can view it using the mob browser.

Navigate to this URL: **&lt;domain name/or ip\_address&gt;/mob/?moid=ha-root-pool**

The root resource pool groups the resources of that host. Other child resource pools can also be created from the root resource pool. The root is identified in the ESXi host with the Managed Object ID: ha-root-pool.

## Forward migration

If you were using standalone ESXi discovery and now the same ESXi is part of vCenter, you can use vCenter discovery instead. Create a vCenter discovery schedule and trigger it. Triggering a vCenter discovery creates duplicate CIs in the following tables as the identifiers for the CIs are different when ESXi is standalone or part of vCenter:

-   VMware VCenter Network \[cmdb\_ci\_vcenter\_network\]
-   ESX Resource Pool \[cmdb\_ci\_esx\_resource\_pool\]
-   VMware VCenter Datastore \[cmdb\_ci\_vcenter\_datastore\]
-   Datastore Disk \[cmdb\_ci\_vcenter\_datastore\_disk\]

To avoid duplicates, you must mark the CIs created by standalone ESXi discovery in the above four tables as retired. When vCenter discovery is triggered, the vCenterESXHostsSensor script include checks for all the ESXi servers whether they were previously discovered as standalone ESXi server. If yes, it automatically triggers the ESXMigrationUtil script to mark all the previously discovered duplicate CIs as retired.

**Note:** If you want to trigger migration manually, you can do so by executing the following script from the background script: // @params esx\_sys\_ids – array of sys ids of all the ESXi servers that must be migrated.

```
ESXMigrationUtil. retireCIsForESXForwardMigration(esx_sys_ids)
```

Once an ESXi server is migrated to vCenter, triggering a standalone ESXi discovery schedule on the same ESXi host results in an error. Discovery is aborted with an error message that “This ESXi is part of vCenter &lt;IP\_address of Vcenter&gt; discovery schedule. Aborting discovery”.

**Parent Topic:**[Cloud resource discovery references](cloud-discovery-collected-data.md)

