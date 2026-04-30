---
title: Nutanix extension classes
description: The CMDB CI Class Models store app adds or updates classes for Nutanix.
locale: en-US
release: yokohama
product: CMDB CI Class Models
classification: cmdb-ci-class-models
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 8
breadcrumb: [CMDB CI Class Models, Exploring CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Nutanix extension classes

The CMDB CI Class Models store app adds or updates classes for Nutanix.

The CMDB CI Class Models app adds class models that extend the CMDB class hierarchy, including class descriptions, identification rules, identifier entries, and, if applicable, dependent relationships. You can use the added classes just like any other CMDB class. Applications such as Discovery and Service Mapping Patterns can use the class extensions to populate CIs and discover technologies and software.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Nutanix Enterprise Cloud platform

The Nutanix Enterprise Cloud platform is a converged, scale-out compute and storage system that hosts and stores virtual machines. All nodes in a Nutanix cluster share the management of cluster resources. The foundational unit for the cluster is a Nutanix node which runs a standard hypervisor and contains processors, memory, and local storage \(SSDs and hard disks\). A Nutanix Controller virtual machine runs on each node, enabling the pooling of local storage from all nodes in the cluster.

See the [full release notes for all CMDB CI Class Models](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/it-operations-management/store-rn-itom-cmdb-class-models.html?emcs_t=S2h8ZW1haWx8Ym9hcmRfc3Vic2NyaXB0aW9ufE1FMlVTSFREVDc3S0hTfDMzNDcxMjV8U1VCU0NSSVBUSU9OU3xoSw).

## Classes

This section lists the classes that the CMDB CI Class Models store app adds or updates. See the class columns table for further details about the columns added for each class.

CMDB CI Class Models: Release 1.6.0 adds the following classes for Nutanix. For the list of classes in the base system, including classes that this app might extend, see [CMDB tables descriptions](../reference/cmdb-tables-details.md).

<table id="table_qnc_3b5_rkb"><thead><tr><th>

Class

</th><th>

Extends

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Nutanix Prism Central\[cmdb\_ci\_nutanix\_prism\_central\]

</td><td>

Virtual Machine Object\[cmdb\_ci\_vm\_object\]

</td><td>

Multi-cluster manager responsible for managing multiple Acropolis Clusters to provide a single, centralized management interface.

</td></tr></tbody>
</table>CMDB CI Class Models: Release 1.2.0 adds the following classes for Nutanix.

<table id="table_x53_n4v_phb"><thead><tr><th>

Class

</th><th>

Extends

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Nutanix Cluster\[cmdb\_ci\_nutanix\_cluster\]

</td><td>

Virtual Machine Object\[cmdb\_ci\_vm\_object\]

</td><td>

Cluster comprising of the physical nodes running Nutanix software.

</td></tr><tr><td>

Nutanix Controller VM\[cmdb\_ci\_nutanix\_controller\_vm\]

</td><td>

Application \[cmdb\_ci\_appl\]

</td><td>

Nutanix controller virtual machine that is present in each node and that provides the storage clustering and management capabilities.

</td></tr><tr><td>

Nutanix Storage Container\[cmdb\_ci\_nutanix\_storage\_container\]

</td><td>

Storage Volume \[cmdb\_ci\_storage\_volume\]

</td><td>

Subset of Nutanix storage pool used to apply policies such as reserved capacity, replication factor, and storage optimization options.

</td></tr><tr><td>

Nutanix Storage Pool\[cmdb\_ci\_nutanix\_storage\_pool\]

</td><td>

Storage Pool \[cmdb\_ci\_storage\_pool\]

</td><td>

Grouping of physical disks within a Nutanix cluster which is typically used to create physical separation between virtual machines.

</td></tr><tr><td>

Nutanix Host \[cmdb\_ci\_nutanix\_host\]

</td><td>

Virtualization Server\[cmdb\_ci\_virtualization\_server\]

</td><td>

Physical host on which all the virtual machines run.

</td></tr><tr><td>

Nutanix Virtual Machine Instance \[cmdb\_ci\_nutanix\_vm\_instance\]

</td><td>

Virtual Machine Instance\[cmdb\_ci\_vm\_instance\]

</td><td>

A virtual machine that runs on Nutanix infrastructure.

</td></tr></tbody>
</table>CMDB CI Class Models: Release 1.1.5 adds the following classes for Nutanix.

<table id="table_dmt_grt_rkb"><thead><tr><th>

Class

</th><th>

Extends

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Nutanix Cluster\[cmdb\_ci\_nutanix\_cluster\]

</td><td>

Virtual Machine Object\[cmdb\_ci\_vm\_object\]

</td><td>

Cluster comprising of the physical nodes running Nutanix software.

</td></tr><tr><td>

Nutanix Controller VM\[cmdb\_ci\_nutanix\_controller\_vm\]

</td><td>

Application \[cmdb\_ci\_appl\]

</td><td>

Nutanix controller virtual machine that is present in each node and that provides the storage clustering and management capabilities.

</td></tr><tr><td>

Nutanix Storage Container\[cmdb\_ci\_nutanix\_storage\_container\]

</td><td>

Storage Volume \[cmdb\_ci\_storage\_volume\]

</td><td>

Subset of Nutanix storage pool used to apply policies such as reserved capacity, replication factor, and storage optimization options.

</td></tr><tr><td>

Nutanix Storage Pool\[cmdb\_ci\_nutanix\_storage\_pool\]

</td><td>

Storage Pool \[cmdb\_ci\_storage\_pool\]

</td><td>

Grouping of physical disks within a Nutanix cluster which is typically used to create physical separation between virtual machines.

</td></tr><tr><td>

Nutanix Host \[cmdb\_ci\_nutanix\_host\]

</td><td>

Virtualization Server\[cmdb\_ci\_virtualization\_server\]

</td><td>

Physical host on which all the virtual machines run.

</td></tr><tr><td>

Nutanix Virtual Machine Instance \[cmdb\_ci\_nutanix\_vm\_instance\]

</td><td>

Virtual Machine Instance\[cmdb\_ci\_vm\_instance\]

</td><td>

A virtual machine that runs on Nutanix infrastructure.

</td></tr></tbody>
</table>CMDB CI Class Models: Release 1.1.4 adds the following classes for Nutanix.

<table id="table_nfj_hwt_rkb"><thead><tr><th>

 

</th><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

Nutanix Cluster\[cmdb\_ci\_nutanix\_cluster\]

</td><td>

Virtual Machine Object\[cmdb\_ci\_vm\_object\]

</td><td>

Cluster comprising of the physical nodes running Nutanix software.

</td></tr><tr><td>

Nutanix Controller VM\[cmdb\_ci\_nutanix\_controller\_vm\]

</td><td>

Application \[cmdb\_ci\_appl\]

</td><td>

Nutanix controller virtual machine that is present in each node and that provides the storage clustering and management capabilities.

</td></tr><tr><td>

Nutanix Storage Container\[cmdb\_ci\_nutanix\_storage\_container\]

</td><td>

Storage Volume \[cmdb\_ci\_storage\_volume\]

</td><td>

Subset of Nutanix storage pool used to apply policies such as reserved capacity, replication factor, and storage optimization options.

</td></tr><tr><td>

Nutanix Storage Pool\[cmdb\_ci\_nutanix\_storage\_pool\]

</td><td>

Storage Pool \[cmdb\_ci\_storage\_pool\]

</td><td>

Grouping of physical disks within a Nutanix cluster which is typically used to create physical separation between virtual machines.

</td></tr><tr><td>

Nutanix Host \[cmdb\_ci\_nutanix\_host\]

</td><td>

Virtualization Server\[cmdb\_ci\_virtualization\_server\]

</td><td>

Physical host on which all the virtual machines run.

</td></tr><tr><td>

Nutanix Virtual Machine Instance \[cmdb\_ci\_nutanix\_vm\_instance\]

</td><td>

Virtual Machine Instance\[cmdb\_ci\_vm\_instance\]

</td><td>

A virtual machine that runs on Nutanix infrastructure.

</td></tr></tbody>
</table>## Class columns

CMDB CI Class Models: Release 1.6.0 adds no columns to the Nutanix Prism Central \[cmdb\_ci\_nutanix\_prism\_central\] class.

CMDB CI Class Models: Release 1.2.0 adds the following columns to the respective classes.

<table id="table_avg_2r1_qhb"><thead><tr><th>

Added columns

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Block Serial Numbers

</td><td>

Serial numbers of blocks that are connected to the cluster.

</td></tr><tr><td>

Cluster ID

</td><td>

UUID \(Universal Unique Identifier\) of the cluster.

</td></tr><tr><td>

External Subnet

</td><td>

Subnet of the external IP address of the cluster.

</td></tr><tr><td>

Full Version

</td><td>

Full version of the cluster.

 For example: el7.3-release-euphrates-5.10.3.1-stable-655d4def34bf18785782f2adb8cdd5f8457d1fe3

</td></tr><tr><td>

Hypervisor Types

</td><td>

Types of hypervisors that are related to this cluster.

</td></tr><tr><td>

Internal Subnet

</td><td>

Subnet of internal IP addresses.

</td></tr><tr><td>

NCC Version

</td><td>

Nutanix cluster check version.

</td></tr><tr><td>

NTP Servers

</td><td>

NTP servers that are related to this cluster.

</td></tr><tr><td>

Number of Nodes

</td><td>

Number of nodes that are connected to the cluster.

</td></tr><tr><td>

Timezone

</td><td>

Timezone of the cluster.

</td></tr><tr><td>

Version

</td><td>

Version of the cluster.

 For example: 5.10.3.1

</td></tr></tbody>
</table>|Added columns|Description|
|-------------|-----------|
|Hypervisor Type|Type of hypervisor.|
|Memory \(MB\)|Amount of memory \(in MB\) available on the controller.|
|State|On/off power state of controller.|
|VM ID|UUID of the controller virtual machine.|
|Object ID|ID of the controller virtual machine.|

<table id="table_y2k_wpv_phb"><thead><tr><th>

Added columns

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Compression

</td><td>

Indicates whether compression is enabled.

</td></tr><tr><td>

Container ID

</td><td>

UUID of the container.

</td></tr><tr><td>

Deduplication

</td><td>

Indicates whether on disk deduplication is enabled, that is dedup compression applied to data on hard disks \(HDD\).

 Performance tier deduplication is a prerequisite for on disk deduplication.

</td></tr><tr><td>

Erasure Code

</td><td>

Indicates whether erasure coding is enabled.

</td></tr><tr><td>

Replication Factor

</td><td>

Number of maintained data copies. The replication factor is specified \(2 or 3\) when the container is created.

</td></tr></tbody>
</table>The following classes have no added columns:

-   Nutanix Storage Pool \[cmdb\_ci\_nutanix\_storage\_pool\]
-   Nutanix Host \[cmdb\_ci\_nutanix\_host\]
-   Nutanix Virtual Machine Instance \[cmdb\_ci\_nutanix\_vm\_instance\]

CMDB CI Class Models: Release 1.1.5 adds the following columns to the respective classes.

<table id="table_p2h_r5t_rkb"><thead><tr><th>

Added columns

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Block Serial Numbers

</td><td>

Serial numbers of blocks that are connected to the cluster.

</td></tr><tr><td>

Cluster ID

</td><td>

UUID \(Universal Unique Identifier\) of the cluster.

</td></tr><tr><td>

External Subnet

</td><td>

Subnet of the external IP address of the cluster.

</td></tr><tr><td>

Full Version

</td><td>

Full version of the cluster.

 For example: el7.3-release-euphrates-5.10.3.1-stable-655d4def34bf18785782f2adb8cdd5f8457d1fe3

</td></tr><tr><td>

Hypervisor Types

</td><td>

Types of hypervisors that are related to this cluster.

</td></tr><tr><td>

Internal Subnet

</td><td>

Subnet of internal IP addresses.

</td></tr><tr><td>

NCC Version

</td><td>

Nutanix cluster check version.

</td></tr><tr><td>

NTP Servers

</td><td>

NTP servers that are related to this cluster.

</td></tr><tr><td>

Number of Nodes

</td><td>

Number of nodes that are connected to the cluster.

</td></tr><tr><td>

Timezone

</td><td>

Timezone of the cluster.

</td></tr><tr><td>

Version

</td><td>

Version of the cluster.

 For example: 5.10.3.1

</td></tr></tbody>
</table>|Added columns|Description|
|-------------|-----------|
|Hypervisor Type|Type of hypervisor.|
|Memory|Amount of memory \(in MB\) available to the virtual machine.|
|State|On/off state of power.|
|VM ID|UUID of the controller virtual machine.|
|Object ID|ID of the controller virtual machine.|

<table id="table_lmw_hvt_rkb"><thead><tr><th>

Added columns

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Compression

</td><td>

Indicates whether compression is enabled.

</td></tr><tr><td>

Container ID

</td><td>

UUID of the container.

</td></tr><tr><td>

Deduplication

</td><td>

Indicates whether on disk deduplication is enabled, that is dedup compression applied to data on hard disks \(HDD\).

 Performance tier deduplication is a prerequisite for on disk deduplication.

</td></tr><tr><td>

Erasure Code

</td><td>

Indicates whether erasure coding is enabled.

</td></tr><tr><td>

Replication Factor

</td><td>

Number of maintained data copies. The replication factor is specified \(2 or 3\) when the container is created.

</td></tr></tbody>
</table>The following classes have no added columns:

-   Nutanix Storage Pool \[cmdb\_ci\_nutanix\_storage\_pool\]
-   Nutanix Host \[cmdb\_ci\_nutanix\_host\]
-   Nutanix Virtual Machine Instance \[cmdb\_ci\_nutanix\_vm\_instance\]

CMDB CI Class Models: Release 1.1.4 adds the following columns to the respective classes.

<table id="table_igw_vxt_rkb"><thead><tr><th>

Added columns

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Block Serial Numbers

</td><td>

Serial numbers of blocks that are connected to the cluster.

</td></tr><tr><td>

Cluster ID

</td><td>

UUID \(Universal Unique Identifier\) of the cluster.

</td></tr><tr><td>

External Subnet

</td><td>

Subnet of the external IP address of the cluster.

</td></tr><tr><td>

Full Version

</td><td>

Full version of the cluster.

 For example: el7.3-release-euphrates-5.10.3.1-stable-655d4def34bf18785782f2adb8cdd5f8457d1fe3

</td></tr><tr><td>

Hypervisor Types

</td><td>

Types of hypervisors that are related to this cluster.

</td></tr><tr><td>

Internal Subnet

</td><td>

Subnet of internal IP addresses.

</td></tr><tr><td>

NCC Version

</td><td>

Nutanix cluster check version.

</td></tr><tr><td>

NTP Servers

</td><td>

NTP servers that are related to this cluster.

</td></tr><tr><td>

Number of Nodes

</td><td>

Number of nodes that are connected to the cluster.

</td></tr><tr><td>

Timezone

</td><td>

Timezone of the cluster.

</td></tr><tr><td>

Version

</td><td>

Version of the cluster.

 For example: 5.10.3.1

</td></tr></tbody>
</table>|Added columns|Description|
|-------------|-----------|
|Hypervisor Type|Type of hypervisor.|
|Memory|Amount of memory \(in MB\) available to the virtual machine.|
|State|On/off state of power.|
|VM ID|UUID of the controller virtual machine.|
|Object ID|ID of the controller virtual machine.|

<table id="table_mvk_2yt_rkb"><thead><tr><th>

Added columns

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Compression

</td><td>

Indicates whether compression is enabled.

</td></tr><tr><td>

Container ID

</td><td>

UUID of the container.

</td></tr><tr><td>

Deduplication

</td><td>

Indicates whether on disk deduplication is enabled, that is dedup compression applied to data on hard disks \(HDD\).

 Performance tier deduplication is a prerequisite for on disk deduplication.

</td></tr><tr><td>

Erasure Code

</td><td>

Indicates whether erasure coding is enabled.

</td></tr><tr><td>

Replication Factor

</td><td>

Number of maintained data copies. The replication factor is specified \(2 or 3\) when the container is created.

</td></tr></tbody>
</table>The following classes have no added columns:

-   Nutanix Storage Pool \[cmdb\_ci\_nutanix\_storage\_pool\]
-   Nutanix Host \[cmdb\_ci\_nutanix\_host\]
-   Nutanix Virtual Machine Instance \[cmdb\_ci\_nutanix\_vm\_instance\]

**Related topics**  


[CMDB schema model](c_ConfigurationManagementDatabase.md)

