---
title: Azure virtual machine pattern-based discovery
description: Discovery and Service Mapping Patterns finds Azure virtual machines \(VMs\) on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: zurich
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 6
keywords: [Azure Virtual Machine, Azure discovery, Azure VM, Azure patterns, Virtual Machine pattern]
breadcrumb: [Microsoft Azure discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Azure virtual machine pattern-based discovery

Discovery and Service Mapping Patterns finds Azure virtual machines \(VMs\) on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

-   **Verify the Microsoft Azure discovery prerequisites**

    For more information, see the prerequisites section in [Microsoft Azure Cloud discovery using patterns](azure-cloud-discovery-patterns.md).

-   **\(Optional\) Exclude temporary Azure Databricks VMs**

    Starting with Discovery and Service Mapping Patterns version 1.30.2, you can reduce short-lived configuration item \(CI\) records by excluding temporary Azure Databricks VMs. For more information, see [Exclude temporary Azure Databricks virtual machines](../task/exclude-temp-azure-databricks-vms.md).


## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Azure - Virtual Machine \(LP\) pattern.

<table id="table_vm_instance"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \[name\]

</td><td>

Name of the virtual machine.

</td></tr><tr><td>

Object ID \[object\_id\]

</td><td>

A unique identifier allocated by Azure for this virtual machine.

</td></tr><tr><td>

VM Instance ID \[vm\_inst\_id\]

</td><td>

The unique virtual machine identifier assigned by Azure.

</td></tr><tr><td>

State \[state\]

</td><td>

Power state of the virtual machine. Possible values include: On, Off, or Terminated.

</td></tr><tr><td>

Memory \(MB\) \[memory\]

</td><td>

Memory capacity of the virtual machine in megabytes \(MB\).

</td></tr><tr><td>

CPUs \[cpus\]

</td><td>

Number of virtual CPUs \(vCPUs\) allocated to the virtual machine.

</td></tr><tr><td>

Disks \[disks\]

</td><td>

Total number of disks attached to the virtual machine, including OS disk and data disks.

</td></tr><tr><td>

Disk size \[disks\_size\]

</td><td>

Total size of all disks attached to the virtual machine in gigabytes \(GB\).

</td></tr><tr><td>

Network adapters \[nics\]

</td><td>

Number of network interface cards \(NICs\) attached to the virtual machine.

</td></tr><tr><td>

Install Status \[install\_status\]

</td><td>

Install status of the resource. Default value is Installed.

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|Object ID \[object\_id\]|A unique identifier allocated by Azure for this Virtual Machine Scale Set instance.|

|Field|Description|
|-----|-----------|
|Object ID \[object\_id\]|A unique identifier for the managed disk.|
|Name \[name\]|Name of the managed disk.|

|Field|Description|
|-----|-----------|
|Object ID \[object\_id\]|A unique identifier for the disk endpoint.|
|Name \[name\]|Name of the disk endpoint.|
|Host \[host\]|The virtual machine object ID to which this disk endpoint is attached.|

|Field|Description|
|-----|-----------|
|Object ID \[object\_id\]|A unique identifier for the NIC.|
|Primary \[primary\]|Indicates whether this NIC is the primary network interface.|

|Field|Description|
|-----|-----------|
|Object ID \[object\_id\]|A unique identifier for the virtual network interface endpoint.|
|Name \[name\]|Name of the virtual network interface endpoint.|

|Field|Description|
|-----|-----------|
|Object ID \[object\_id\]|A unique identifier for the availability zone in the format: region-zone.|
|Name \[name\]|A unique identifier for the availability zone in the format: region-zone.|
|Install Status \[install\_status\]|Install status of the resource. Default value is Installed.|

<table id="table_os_image"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object ID \[object\_id\]

</td><td>

A unique identifier for the OS image or custom image.

</td></tr><tr><td>

Name \[name\]

</td><td>

Name of the OS image or custom image.

</td></tr><tr><td>

Provider \[provider\]

</td><td>

Cloud provider. The value is set to **AZURE**. This field is only populated in the Cloud Image \[cmdb\_ci\_cloud\_os\_image\] table.

</td></tr></tbody>
</table>**Note:** When using the Image \[cmdb\_ci\_os\_template\] table to store Cloud OS images, you may notice an unusually large number of records. To avoid this issue, you can store the discovered OS images in the Cloud Image \[cmdb\_ci\_cloud\_os\_image\] table. For more information, see [Enable Cloud OS Image discovery](../../discovery/task/enable-cloud-os-image-discovery-pattern.md).

<table id="table_hardware_type"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object ID \[object\_id\]

</td><td>

The VM size Stock Keeping Unit \(SKU\) name.

</td></tr><tr><td>

Provider \[provider\]

</td><td>

Cloud provider. The value is set to **AZURE**. This field is only populated in the Cloud Hardware Type \[cmdb\_ci\_cloud\_hardware\_type\] table.

</td></tr></tbody>
</table>**Note:** When using the Hardware Type \[cmdb\_ci\_compute\_template\] table to store the hardware types, you may notice an unusually large number of records. To avoid this issue, you can store the discovered hardware types in the Cloud Hardware Type \[cmdb\_ci\_cloud\_hardware\_type\] table. For more information, see [Enable the Cloud Hardware Type class extension](../../discovery/task/enable-hardware-type-class-extension.md).

## CI relationships

The Azure - Virtual Machine \(LP\) pattern creates these relationships to support Azure VM discovery.

|CI|Relationship|CI|
|---|------------|---|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Managed by::Manages|Instance Scale Set \[cmdb\_ci\_instance\_scale\_set\]|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Hosted on::Hosts|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Provisioned From::Provisioned|Hardware Type \[cmdb\_ci\_compute\_template\] or Cloud Hardware Type \[cmdb\_ci\_cloud\_hardware\_type\]|
|Storage Volume \[cmdb\_ci\_storage\_volume\]|Hosted on::Hosts|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|
|Block Endpoint \[cmdb\_ci\_endpoint\_block\]|Implement End Point To::Implement End Point From|Storage Volume \[cmdb\_ci\_storage\_volume\]|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Use End Point To::Use End Point From|Block Endpoint \[cmdb\_ci\_endpoint\_block\]|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Use End Point To::Use End Point From|VNIC Endpoint \[cmdb\_ci\_endpoint\_vnic\]|
|VNIC Endpoint \[cmdb\_ci\_endpoint\_vnic\]|Implement End Point To::Implement End Point From|Cloud Mgmt Network Interface \[cmdb\_ci\_nic\]|
|Resource Group \[cmdb\_ci\_resource\_group\]|Contains::Contained by|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Provisioned From::Provisioned|Image \[cmdb\_ci\_os\_template\] or Cloud Image \[cmdb\_ci\_cloud\_os\_image\]|
|Image \[cmdb\_ci\_os\_template\] or Cloud Image \[cmdb\_ci\_cloud\_os\_image\]|Hosted on::Hosts|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|
|Availability Zone \[cmdb\_ci\_availability\_zone\]|Contains::Contained by|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|
|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|Contains::Contained by|Availability Zone \[cmdb\_ci\_availability\_zone\]|
|Availability Set \[cmdb\_ci\_availability\_set\]|Contains::Contained by|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|
|Key Value \[cmdb\_key\_value\]|References|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|

## Azure Tag discovery

The Azure - Virtual Machine \(LP\) pattern collects tags and populates them in the Key Value \[cmdb\_key\_value\] table.

|Field|Description|
|-----|-----------|
|Key \[key\]|Tag name.|
|Value \[value\]|Tag value.|
|Configuration item \[configuration\_item\]|References the Virtual Machine Instance \[cmdb\_ci\_vm\_instance\] table.|

## Azure BYOL discovery

The pattern extension section discovers the following license types for Windows and Red Hat Enterprise Linux \(RHEL\) VMs:

-   Bring Your Own License \(BYOL\)
-   License included

The pattern stores the license type and model in the Key Value \[cmdb\_key\_value\] table.

**Note:**

-   For Windows VM using a custom image, Discovery populates key values only when the primary OS disk details are available.
-   For RHEL VMs, Discovery populates information only for VMs that use Marketplace images.

<table id="table_lms_grx_h3c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Key \[key\]

</td><td>

The license type key, which is one of the following:-   Windows\_OS\_License\_Type\_automatic
-   RHEL\_OS\_License\_Type\_automatic

</td></tr><tr><td>

Value \[value\]

</td><td>

The license model, which is one of the following:-   BYOL
-   License Included

</td></tr><tr><td>

Configuration item \[configuration\_item\]

</td><td>

References the Virtual Machine Instance \[cmdb\_ci\_vm\_instance\] table.

</td></tr></tbody>
</table>-   **[Exclude temporary Azure Databricks virtual machines](../task/exclude-temp-azure-databricks-vms.md)**  
Reduce short-lived configuration item \(CI\) records by excluding temporary Azure Databricks virtual machines \(VMs\).

**Parent Topic:**[Microsoft Azure Cloud discovery using patterns](azure-cloud-discovery-patterns.md)

