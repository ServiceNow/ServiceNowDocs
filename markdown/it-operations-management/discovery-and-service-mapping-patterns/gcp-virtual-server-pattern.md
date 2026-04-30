---
title: GCP virtual server pattern-based discovery
description: Discovery and Service Mapping Patterns finds GCP Virtual Machine \(VM\) instances and related resources on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: yokohama
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2025-01-22"
reading_time_minutes: 7
keywords: [GCP Virtual Server, GCP VM instance, Google Cloud virtual machine, GCP discovery, GCP patterns, Compute Engine, Google Cloud Platform Virtual Server discovery]
breadcrumb: [Available discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# GCP virtual server pattern-based discovery

Discovery and Service Mapping Patterns finds GCP Virtual Machine \(VM\) instances and related resources on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

Verify the GCP discovery prerequisites section in [Google Cloud Platform \(GCP\) Cloud components discovery using Patterns](gcp-cloud-discovery-patterns.md).

## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Google Cloud Platform \(GCP\) - Virtual Server pattern.

|Field|Description|
|-----|-----------|
|Account Id \[account\_id\]|Name of the project used for the discovery.|
|Object ID \[object\_id\]|Name of the project used for the discovery.|
|Datacenter Type \[datacenter\_type\]|Datacenter type: Google Datacenter \[cmdb\_ci\_google\_datacenter\].|

|Field|Description|
|-----|-----------|
|Name \[name\]|Name of the availability zone.|
|Description \[short\_description\]|Description of the availability zone.|
|State \[state\]|State of the Availability Zone. Possible values are Available or Terminated.|

|Field|Description|
|-----|-----------|
|Name \[name\]|Datacenter or region name.|
|Region \[region\]|Datacenter or region name.|
|Object ID \[object\_id\]|Unique identifier allocated by GCP for this resource.|
|Description \[short\_description\]|Datacenter or region description.|

<table id="table_vm_instance"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object ID \[object\_id\]

</td><td>

Unique identifier for the VM instance.

</td></tr><tr><td>

VM Instance ID \[vm\_inst\_id\]

</td><td>

Unique identifier for the VM instance.

</td></tr><tr><td>

Name \[name\]

</td><td>

Name of the VM instance.

</td></tr><tr><td>

State \[state\]

</td><td>

Operational state of the virtual machine.For example: On, Off, or Terminated.

</td></tr><tr><td>

Install Status \[install\_status\]

</td><td>

Install status of the resource. Default value is Installed.

</td></tr><tr><td>

CPUs \[cpus\]

</td><td>

Number of virtual CPUs \(vCPUs\) allocated to the instance.

</td></tr><tr><td>

Memory \(MB\) \[memory\]

</td><td>

Amount of memory in megabytes \(MB\) allocated to the instance.

</td></tr><tr><td>

Termination Protection \[termination\_protection\]

</td><td>

Indicates whether deletion protection is enabled and the instance can't be deleted.Possible values are true or false.

</td></tr><tr><td>

Disks \[disks\]

</td><td>

Number of disks attached to the VM instance.

</td></tr><tr><td>

Disks size \(GB\) \[disks\_size\]

</td><td>

Total size of all disks attached to the instance in gigabytes \(GB\).

</td></tr><tr><td>

Network adapters \[nics\]

</td><td>

Number of network interfaces attached to the VM instance.

</td></tr><tr><td>

IP Address \[ip\_address\]

</td><td>

Primary internal IP address of the instance.

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|Object ID \[object\_id\]|Unique identifier for the instance template.|
|Name \[name\]|Name of the instance template.|
|Description \[short\_description\]|Description of the template configuration.|

|Field|Description|
|-----|-----------|
|Object ID \[object\_id\]|Unique identifier combining VM ID and Network Interface Controller \(NIC\) name.|
|Name \[name\]|Name of the network interface.|
|Private IP \[private\_ip\]|Primary internal IP address.|
|IP Address \[ip\_address\]|IP address of the network interface.|
|Public IP \[public\_ip\]|Public IP address of the network interface.|

|Field|Description|
|-----|-----------|
|Object ID \[object\_id\]|Unique identifier for the virtual NIC endpoint.|
|Name \[name\]|Name of the virtual NIC endpoint.|
|Region \[region\]|Region where the endpoint is located.|
|IP Address \[ip\_address\]|IP address of the endpoint.|

<table id="table_storage_volume"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object ID \[object\_id\]

</td><td>

Unique identifier for the persistent disk volume.

</td></tr><tr><td>

Name \[name\]

</td><td>

Name of the disk volume.

</td></tr><tr><td>

Volume ID \[volume\_id\]

</td><td>

Volume identifier.

</td></tr><tr><td>

Storage type \[storage\_type\]

</td><td>

Type of persistent disk.For example: **pd-balanced**, **pd-ssd**, or **pd-standard**.

</td></tr><tr><td>

Size bytes \[size\_bytes\]

</td><td>

Size of the volume in bytes.

</td></tr><tr><td>

State \[state\]

</td><td>

State of the volume.For example: Available, In Use, or Terminated.

</td></tr><tr><td>

Install Status \[install\_status\]

</td><td>

Install status of the resource. Default value is Installed.

</td></tr><tr><td>

Description \[short\_description\]

</td><td>

Description of the volume.

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|Object ID \[object\_id\]|Unique identifier for the block storage endpoint.|
|Name \[name\]|Name of the storage endpoint.|
|Host \[host\]|VM instance name to which the disk is attached.|

<table id="table_os_image"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \[name\]

</td><td>

Name of the operating system \(OS\) image.

</td></tr><tr><td>

Object ID \[object\_id\]

</td><td>

Unique identifier for the OS image.

</td></tr><tr><td>

Image Type \[image\_type\]

</td><td>

Source type of the image.For example: RAW or machine.

</td></tr><tr><td>

Image Source \[image\_source\]

</td><td>

Source of the image in the format: **disk\_name/disk\_id** or **snapshot\_name/snapshot\_id**.

</td></tr><tr><td>

FQDN \[fqdn\]

</td><td>

Fully qualified domain name \(FQDN\) of the image resource.

</td></tr><tr><td>

Provider \[provider\]

</td><td>

The cloud provider, which is **GCP**. This field is only populated in Cloud Image \[cmdb\_ci\_cloud\_os\_image\] table.

</td></tr></tbody>
</table>**Note:** When using the Image \[cmdb\_ci\_os\_template\] table to store Cloud OS images, you may notice an unusually large number of records. To avoid this issue, you can store the discovered OS images in the Cloud Image \[cmdb\_ci\_cloud\_os\_image\] table. For more information, see [Enable Cloud OS Image discovery](../../discovery/task/enable-cloud-os-image-discovery-pattern.md).

<table id="table_hardware_type"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object ID \[object\_id\]

</td><td>

Unique identifier for the machine type.

</td></tr><tr><td>

Name \[name\]

</td><td>

Name of the machine type. For example: **n1-standard-4**.

</td></tr><tr><td>

Short description \[short\_description\]

</td><td>

Description of the machine type configuration.

</td></tr><tr><td>

vCPUs \[vcpus\]

</td><td>

Number of vCPUs in the machine type.

</td></tr><tr><td>

Memory MB \[memory\_mb\]

</td><td>

Amount of memory available in the machine type in MB.

</td></tr><tr><td>

Local storage GB \[local\_storage\_gb\]

</td><td>

Amount of local storage space in GB.

</td></tr><tr><td>

Zone \[zone\]

</td><td>

Availability zone where the machine type is available.For example: **us-west4-b**.

</td></tr><tr><td>

Provider \[provider\]

</td><td>

The cloud provider, which is **GCP**. This field is only populated in Cloud Hardware Type \[cmdb\_ci\_cloud\_hardware\_type\] table.

</td></tr></tbody>
</table>**Note:** When using the Hardware Type \[cmdb\_ci\_compute\_template\] table to store the hardware types, you may notice an unusually large number of records. To avoid this issue, you can store the discovered hardware types in the Cloud Hardware Type \[cmdb\_ci\_cloud\_hardware\_type\] table. For more information, see [Enable the Cloud Hardware Type class extension](../../discovery/task/enable-hardware-type-class-extension.md).

## CI relationships

The Google Cloud Platform \(GCP\) - Virtual Server pattern creates these relationships to support GCP Virtual Machine discovery.

|CI|Relationship|CI|
|---|------------|---|
|Google Datacenter \[cmdb\_ci\_google\_datacenter\]|Hosted on::Hosts|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|
|Google Datacenter \[cmdb\_ci\_google\_datacenter\]|Contains::Contained by|Availability Zone \[cmdb\_ci\_availability\_zone\]|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Hosted on::Hosts|Google Datacenter \[cmdb\_ci\_google\_datacenter\]|
|Availability Zone \[cmdb\_ci\_availability\_zone\]|Contains::Contained by|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|
|Image \[cmdb\_ci\_os\_template\] or Cloud Image \[cmdb\_ci\_cloud\_os\_image\]|Hosted on::Hosts|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|
|Hardware Type \[cmdb\_ci\_compute\_template\] or Cloud Hardware Type \[cmdb\_ci\_cloud\_hardware\_type\]|Hosted on::Hosts|Google Datacenter \[cmdb\_ci\_google\_datacenter\]|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Provisioned From::Provisioned|Hardware Type \[cmdb\_ci\_compute\_template\] or Cloud Hardware Type \[cmdb\_ci\_cloud\_hardware\_type\]|
|Instance template \[cmdb\_ci\_instance\_template\]|Hosted on::Hosts|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|
|Instance template \[cmdb\_ci\_instance\_template\]|Uses::Used by|Hardware Type \[cmdb\_ci\_compute\_template\] or Cloud Hardware Type \[cmdb\_ci\_cloud\_hardware\_type\]|
|Instance template \[cmdb\_ci\_instance\_template\]|Uses::Used by|Image \[cmdb\_ci\_os\_template\] or Cloud Image \[cmdb\_ci\_cloud\_os\_image\]|
|VNIC Endpoint \[cmdb\_ci\_endpoint\_vnic\]|Implement End Point To::Implement End Point From|Cloud Mgmt Network Interface \[cmdb\_ci\_nic\]|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Use End Point To::Use End Point From|VNIC Endpoint \[cmdb\_ci\_endpoint\_vnic\]|
|Cloud Mgmt Network Interface \[cmdb\_ci\_nic\]|Hosted on::Hosts|Google Datacenter \[cmdb\_ci\_google\_datacenter\]|
|Storage Volume \[cmdb\_ci\_storage\_volume\]|Hosted on::Hosts|Google Datacenter \[cmdb\_ci\_google\_datacenter\]|
|Availability Zone \[cmdb\_ci\_availability\_zone\]|Contains::Contained by|Storage Volume \[cmdb\_ci\_storage\_volume\]|
|Block Endpoint \[cmdb\_ci\_endpoint\_block\]|Implement End Point To::Implement End Point From|Storage Volume \[cmdb\_ci\_storage\_volume\]|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Use End Point To::Use End Point From|Block Endpoint \[cmdb\_ci\_endpoint\_block\]|
|Key Value \[cmdb\_key\_value\]|References|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|
|Key Value \[cmdb\_key\_value\]|References|Image \[cmdb\_ci\_os\_template\] or Cloud Image \[cmdb\_ci\_cloud\_os\_image\]|

## GCP label discovery

The pattern extension collects labels and populates them in two entries in the Key Value \[cmdb\_key\_value\] table. One entry references the Virtual Machine Instance table, the other entry references the Image or Cloud Image table.

|Field|Description|
|-----|-----------|
|Key \[key\]|Label name.|
|Value \[value\]|Label value.|
|Configuration item \[configuration\_item\]|References the Virtual Machine Instance \[cmdb\_ci\_vm\_instance\] table.|
|Configuration item \[configuration\_item\]|References the Image \[cmdb\_ci\_os\_template\] or Cloud Image \[cmdb\_ci\_cloud\_os\_image\] table.|

## GCP BYOL discovery

The pattern extension section discovers the following license types for Windows and Red Hat Enterprise Linux \(RHEL\), and SQL Server VMs:

-   Bring Your Own License \(BYOL\)
-   License included

The pattern stores the license type and model in the Key Value \[cmdb\_key\_value\] table.

<table id="table_key_value"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Key \[key\]

</td><td>

The license type key, which is one of the following:-   Windows\_OS\_License\_Type\_automatic
-   RHEL\_OS\_License\_Type\_automatic
-   SQL\_Server\_License\_Type\_automatic

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
</table>**Parent Topic:**[Available discovery patterns](../concept/available-patterns.md)

