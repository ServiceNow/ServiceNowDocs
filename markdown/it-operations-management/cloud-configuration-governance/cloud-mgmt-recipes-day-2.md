---
title: Cloud Provisioning and Governance Recipes
description: Multi-cloud recipes provide ready content for typical cloud deployment and common operations scenarios across cloud platforms.
locale: en-US
release: zurich
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Cloud Provisioning and Governance Recipes

Multi-cloud recipes provide ready content for typical cloud deployment and common operations scenarios across cloud platforms.

## Recipes for Enterprise Workloads and Day-2 Operations

Cloud Provisioning and Governance recipes are ready-to-use catalog items built from sample CFT and ARM templates to support real-world cloud deployment use-cases. These recipes are ready for use in Proof of Concept as well as non-production environments. For production environments, ensure that the recipes are well tested and internally evaluated. You can avail the recipes, as update sets, to be downloaded from the SHARE in the developer portal under the Cloud Provisioning Recipes category.

## List of Update Sets

|Name|Description|
|----|-----------|
|Catalog Items for Amazon Web Service|
|CFT Single Linux VM|Catalog Item for a single Linux Virtual Machine using CFT.|
|CFT Single Windows VM|Catalog Item for a single Windows Virtual Machine using CFT.|
|CFT Linux VM with Multiple NICs|Catalog Item for a Linux Virtual Machine with multiple network interfaces using CFT.|
|CFT Linux VM with LB and Storage|Catalog Item for a Linux Virtual Machine with load balancing and storage using CFT.|
|CFT Linux VM with Multi VM Multi Disk|Cloud Formation Template for a Linux VM with multiple VMs and multiple virtual disk interfaces.|
|CFT Linux Install Apache|Catalog Item to install an Apache server on a Linux VM using CFT.|
|CFT Simple VM with Approval Policy|Catalog Item for a simple VM with an approval policy, using CFT.|
|CFT Windows VM Multi Disk and LB|Catalog Item for a Windows VM with multiple virtual disk interfaces and load balancing, using CFT.|
|Catalog Items for Azure|
|ARM Windows VM with Multi NICs|Catalog Item for a Windows VM with multiple network interfaces using ARM template.|
|ARM Windows Single VM Multi Disk|Catalog Item for a single VM with multiple virtual disk interfaces, using ARM template.|
|ARM Windows Stack Multi Disk|Catalog Item for a Windows stack with multiple virtual disk interfaces, using ARM template.|
|ARM Windows Stack Multi NIC|Catalog Item for a Windows Stack VM with multiple network interfaces, using ARM template.|
|ARM Linux VM Multi NIC Multi Disk|Catalog Item for a Linux VM with multiple virtual disk and network interfaces, using ARM template.|
|ARM Linux VM Install Apache|Catalog Item to install an Apache server on a Linux VM, using ARM template.|
|ARM Linux VM Install MySQL|Catalog Item to install a MySQL server on a Linux VM, using ARM template.|
|ARM WebApp MySQL|Catalog Item to build a Web app with Azure database for MySQL, using ARM template.|
|ARM VNET Multi Subnet with Approval Policy|Catalog Item for multi subnet VNET with approval policy, using ARM template.|
|ARM VNIC Multi Subnet with Naming Policy|Catalog Item for multi subnet VNIC with a naming policy, using ARM template.|

## Day 2 Operations for AWS VM

An update set is provided for some of the important Day 2 operations on AWS cloud provider. Broadly, Day 2 operations are the type of operations that are executed on workloads after they are provisioned. Day 2 operations can include complex life-cycle processes or simple utilities. In this update set, you have access to the following set of operations:

<table id="table_prx_kbc_qjb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

AttachVolume

</td><td>

Attaches and exposes an Amazon \(Elastic Block Store\) EBS volume to the instance with the specified device name.

</td></tr><tr><td>

CreateSnapshot\[AWS datacenter level discovery operation\]

</td><td>

Creates a snapshot of your Amazon \(Elastic Block Store\) EBS volume.

</td></tr><tr><td>

DescribeSnapshots

</td><td>

Describes the specified Amazon \(Elastic Block Store\) EBS snapshots available to you or all EBS snapshots available to you.

</td></tr><tr><td>

DetachVolume

</td><td>

Detaches an EBS volume from an instance.

</td></tr><tr><td>

ModifyInstanceAttribute \[Only InstanceType\]

</td><td>

Modify the specified attribute of the specified instance.

</td></tr><tr><td>

ModifyVolume \[Only Size\]

</td><td>

Modify parameters of an existing Amazon \(Elastic Block Store\) EBS volume.

</td></tr><tr><td>

Day 2 Operations for AWS VM – Set 1

</td><td>

Catalog Item for Day 2 operations for an AWS VM, Set 1.

</td></tr></tbody>
</table>