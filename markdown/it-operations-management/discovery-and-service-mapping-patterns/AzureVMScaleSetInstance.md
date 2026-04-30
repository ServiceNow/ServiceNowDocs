---
title: Azure Virtual Machine Scale Sets \(VMSS\) Instance discovery
description: The Discovery and Service Mapping Patterns application uses the Azure - VM Scale Set \(LP\) and the Azure VM Instance - Uniform Scale Set patterns to find Azure Virtual Machine Scale Sets \(VMSS\). Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: yokohama
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Available discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Azure Virtual Machine Scale Sets \(VMSS\) Instance discovery

The Discovery and Service Mapping Patterns application uses the Azure - VM Scale Set \(LP\) and the Azure VM Instance - Uniform Scale Set patterns to find Azure Virtual Machine Scale Sets \(VMSS\). Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

VMSS let you create and manage a group of load balanced virtual machines \(VMs\). The number of VM instances can automatically increase or decrease in response to demand or a defined schedule. There Uniform Orchestration modes Flexible and achieve.

-   VMSS with Flexible Orchestration achieves high availability at scale with identical or multiple virtual machine types. With Flexible orchestration, Azure provides a unified experience across the Azure VM ecosystem.
-   VMSS with Uniform Orchestration optimized for large-scale stateless workloads with identical instances. VMSS with Uniform orchestration use a virtual machine profile or template to scale up to desired capacity. While there is some ability to manage or customize individual virtual machine instances, Uniform uses identical VM instances.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

To learn about VMSS and their versions that you can discover, refer to [Detailed information on products discovered by ITOM Visibility](../../service-mapping/reference/r_SupportedApplications.md).

## Prerequisites

Verify the Azure discovery prerequisites section in [Microsoft Azure Cloud components discovery using patterns](../../service-mapping/reference/azure-cloud-discovery-patterns.md).

## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Azure - VM Scale Set \(LP\) Pattern.

|Field|Description|
|-----|-----------|
|Install Status \[install\_status\]|Install status of the instance scale set. Default value is Installed.|
|State \[state\]|Provisioning state of the instance scale set. Possible values are Available or Terminated.|
|Object ID \[object\_id\]|A unique identifier for the instance scale set.|
|Name \[name\]|Name of the instance scale set.|

Discovery populates the data in the CMDB when running the Azure VM Instance - Uniform Scale Set pattern.

|Field|Description|
|-----|-----------|
|Network adapters \[nics\]|Number of Network Interface Cards \(NICs\) attached to the virtual machine \(VM\) instance.|
|State \[state\]|Current state of the instance. For example: On, Off, or Terminated.|
|Install Status \[install\_status\]|Install status of the instance. Default value is Installed.|
|Operational status \[operational\_status\]|Operational status of the instance. Default value is Operational.|
|Disks \[disks\]|Number of disks attached to the instance.|
|Disks size \(GB\) \[disk\_size\]|Total storage capacity of all disks attached to the VM, in gigabytes \(GB\).|

|Field|Description|
|-----|-----------|
|Name \[name\]|Name or ID for the storage volume.|
|Object ID \[object\_id\]|A unique identifier, allocated by Microsoft Azure for this resource.|
|Install Status \[install\_status\]|Install status of the storage volume. Default value is Installed.|
|Operational status \[operational\_status\]|Operational status of the storage volume. Default value is Operational.|

|Field|Description|
|-----|-----------|
|Name \[name\]|Name or ID for the network interface.|
|Object ID \[object\_id\]|A unique identifier, allocated by Microsoft Azure for this resource.|
|Install Status \[install\_status\]|Install status of the network interface. Default status is Installed.|
|Operational status \[operational\_status\]|Operational status of the network interface. Default status is Operational.|

|Field|Description|
|-----|-----------|
|Name \[name\]|Name or ID for the endpoint.|
|Object ID \[object\_id\]|A unique identifier, allocated by Microsoft Azure for this resource.|

|Field|Description|
|-----|-----------|
|Name \[name\]|Name or ID for the image.|
|Object ID \[object\_id\]|A unique identifier, allocated by Microsoft Azure for this resource.|
|Install Status \[install\_status\]|Install status of the image. Default value is Installed.|
|Operational status \[operational\_status\]|Operational status of the image. Default value is operational.|

**Note:** When using the Image \[cmdb\_ci\_os\_template\] table to store Cloud OS images, you may notice an unusually large number of records. To avoid this issue, you can store the discovered OS images in the Cloud Image \[cmdb\_ci\_cloud\_os\_image\] table. For more information, see [Enable Cloud OS Image discovery](../task/enable-cloud-os-image-discovery-pattern.md).

|Field|Description|
|-----|-----------|
|Name \[name\]|Name of the hardware type.|

**Note:** When using the Hardware Type \[cmdb\_ci\_compute\_template\] table to store the hardware types, you may notice an unusually large number of records. To avoid this issue, you can store the discovered hardware types in the Cloud Hardware Type \[cmdb\_ci\_cloud\_hardware\_type\] table. For more information, see [Enable the Cloud Hardware Type class extension](../task/enable-hardware-type-class-extension.md).

## CI relationships

Discovery creates these relationships to support the VMSS discovery, when running the Azure - VM Scale Set \(LP\) pattern.

|CI|Relationship|CI|
|---|------------|---|
|Resource Group \[cmdb\_ci\_resource\_group\]|Contains::Contained by|Instance Scale Set \[cmdb\_ci\_instance\_scale\_set\]|
|Instance Scale Set \[cmdb\_ci\_instance\_scale\_set\]|Hosted on::Hosts|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|
|Instance Scale Set \[cmdb\_ci\_instance\_scale\_set\]|Consumes::Consumed by|Load Balancer Pool \[cmdb\_ci\_lb\_pool\]|

Discovery creates these relationships to support the VMSS discovery, when running the when running the Azure - VM Scale Set \(LP\) pattern.

|CI|Relationship|CI|
|---|------------|---|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Managed by::Manages|Instance Scale Set \[cmdb\_ci\_instance\_scale\_set\]|
|Storage Volume \[cmdb\_ci\_storage\_volume\]|Hosted on::Hosts|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|
|Block Endpoint \[cmdb\_ci\_endpoint\_block\]|Implement End Point To::Implement End Point From|Storage Volume \[cmdb\_ci\_storage\_volume\]|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Use End Point To::Use End Point From|Block Endpoint \[cmdb\_ci\_endpoint\_block\]|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Hosted on::Hosts|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|
|Hardware Type \[cmdb\_ci\_compute\_template\]|Hosted on::Hosts|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Provisioned From::Provisioned|Hardware Type \[cmdb\_ci\_compute\_template\]|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Provisioned From::Provisioned|Cloud Hardware Type \[cmdb\_ci\_cloud\_hardware\_type\]|
|Cloud Mgmt Network Interface \[cmdb\_ci\_nic\]|Hosted on::Hosts|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Implement End Point To::Implement End Point From|Cloud Mgmt Network Interface \[cmdb\_ci\_nic\]|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Use End Point To::Use End Point From|VNIC Endpoint \[cmdb\_ci\_endpoint\_vnic\]|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Provisioned From::Provisioned|Image \[cmdb\_ci\_os\_template\]|
|Image \[cmdb\_ci\_os\_template\]|Hosted on::Hosts|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|

## Tags discovery

Both the Azure - VM Scale Set \(LP\) and the Azure VM Instance - Uniform Scale Set patterns collect tags and populate them in the Key Value \[cmdb\_key\_value\] table.

|Field|Description|
|-----|-----------|
|Key \[key\]|Tag name.|
|Value \[value\]|Tag value.|

**Parent Topic:**[Available discovery patterns](../../service-mapping/concept/available-patterns.md)

