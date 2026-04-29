---
title: AWS virtual server pattern-based discovery
description: Discovery and Service Mapping Patterns finds AWS EC2 virtual machine instances on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
keywords: [AWS Virtual Server, EC2 instances, AWS discovery, AWS patterns, virtual machines]
breadcrumb: [AWS discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# AWS virtual server pattern-based discovery

Discovery and Service Mapping Patterns finds AWS EC2 virtual machine instances on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

Verify the AWS discovery prerequisites section in [AWS discovery using patterns](../../discovery/reference/data-discovered-aws-patterns.md).

## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Amazon AWS - Virtual Server \(LP\) pattern.

<table id="table_vm_instance"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \[name\]

</td><td>

Name of the instance. Possible values are the tag name, if available, or the instance ID.

</td></tr><tr><td>

Object ID \[object\_id\]

</td><td>

Unique identifier for the instance.

</td></tr><tr><td>

State \[state\]

</td><td>

Power state of the instance. Possible values:

-   On: Instance is running
-   Off: Instance is stopped

</td></tr><tr><td>

VM Instance ID \[vm\_inst\_id\]

</td><td>

Instance identifier from AWS.

</td></tr><tr><td>

Memory \(MB\) \[memory\]

</td><td>

Amount of memory allocated to the instance in megabytes \(MB\).

</td></tr><tr><td>

Network adapters \[nics\]

</td><td>

Number of network interface cards \(NICs\) attached to the instance.

</td></tr><tr><td>

Disks \[disks\]

</td><td>

Number of volumes attached to the instance.

</td></tr><tr><td>

CPUs \[cpus\]

</td><td>

Total number of virtual CPUs \(vCPUs\).

</td></tr><tr><td>

IP Address \[ip\_address\]

</td><td>

Private IP address assigned to the instance.

</td></tr><tr><td>

Fully qualified domain name \[fqdn\]

</td><td>

Fully qualified domain name \(FQDN\) assigned to the instance.

</td></tr><tr><td>

Install Status \[install\_status\]

</td><td>

Install status of the resource.For example: Installed or Retired.

</td></tr><tr><td>

Operational status \[operational\_status\]

</td><td>

Operational status of the resource. For example: Operational, Non-Operational, or Retired.

</td></tr></tbody>
</table>**Note:**

If you have reactivated a retired virtual machine \(VM\) and want its active state to be accurately reflected in the **Operational status** and **Install Status** fields in the Virtual Machine Instance \[cmdb\_ci\_vm\_instance\] table, set the **sn\_itom\_pattern.discover\_aws\_instance\_statuses** MID Server property to **true**. Note that this setting involves additional API calls—one for each page of the pattern execution—which may impact performance if you're managing a large number of VMs.

<table id="table_storage_mapping"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \[name\]

</td><td>

Unique identifier for the storage mapping.

</td></tr><tr><td>

Object ID \[object\_id\]

</td><td>

Unique identifier for the storage mapping.

</td></tr><tr><td>

Mapping Type \[mapping\_type\]

</td><td>

The root device type used by the Amazon Machine Image \(AMI\).The AMI can use an EBS volume or an instance store volume.

</td></tr><tr><td>

Mount Point \[mount\_point\]

</td><td>

Device name where the volume is mounted.For example: `/dev/sda1`.

</td></tr><tr><td>

Host \[host\]

</td><td>

Public IP address of the instance, if available.

</td></tr><tr><td>

Install Status \[install\_status\]

</td><td>

Install status of the resource. Default value is Installed.

</td></tr><tr><td>

Operational status \[operational\_status\]

</td><td>

Operational status of the resource. Default value is Operational.

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|Object ID \[object\_id\]|Subnet identifier.|
|Name \[name\]|Subnet identifier.|
|IP Address \[ip\_address\]|IP address associated with the subnet endpoint.|
|Region \[region\]|AWS region where the subnet is located.|

|Field|Description|
|-----|-----------|
|Object ID \[object\_id\]|Subnet identifier.|

|Field|Description|
|-----|-----------|
|Name \[name\]|Domain Name System \(DNS\) name assigned to the instance.|

<table id="table_os_template"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object ID \[object\_id\]

</td><td>

AMI identifier.

</td></tr><tr><td>

Provider \[provider\]

</td><td>

Cloud provider, which is **AWS**.This field is only populated in the Cloud Image \[cmdb\_ci\_cloud\_os\_image\] table.

</td></tr></tbody>
</table>**Note:** When using the Image \[cmdb\_ci\_os\_template\] table to store Cloud OS images, you may notice an unusually large number of records. To avoid this issue, you can store the discovered OS images in the Cloud Image \[cmdb\_ci\_cloud\_os\_image\] table. For more information, see [Enable Cloud OS Image discovery](../../discovery/task/enable-cloud-os-image-discovery-pattern.md).

## CI relationships

The Amazon AWS - Virtual Server \(LP\) pattern creates these relationships to support AWS virtual server discovery.

|CI|Relationship|CI|
|---|------------|---|
|Availability Zone \[cmdb\_ci\_availability\_zone\]|Contains::Contained by|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Contains::Contained by|Storage Mapping \[cmdb\_ci\_storage\_mapping\]|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|
|DNS Name \[cmdb\_ci\_dns\_name\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Provisioned From::Provisioned|Compute Template \[cmdb\_ci\_compute\_template\] or Cloud Hardware Type \[cmdb\_ci\_cloud\_hardware\_type\]|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Provisioned From::Provisioned|Image \[cmdb\_ci\_os\_template\] or Cloud Image \[cmdb\_ci\_cloud\_os\_image\]|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Contains::Contained by|DNS Name \[cmdb\_ci\_dns\_name\]|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Use End Point To::Use End Point From|Subnet Endpoint \[cmdb\_ci\_endpoint\_subnet\]|
|Cloud Subnet \[cmdb\_ci\_cloud\_subnet\]|Implement End Point To::Implement End Point From|Subnet Endpoint \[cmdb\_ci\_endpoint\_subnet\]|
|Network \[cmdb\_ci\_network\]|Contains::Contained by|Cloud Subnet \[cmdb\_ci\_cloud\_subnet\]|
|Image \[cmdb\_ci\_os\_template\] or Cloud Image \[cmdb\_ci\_cloud\_os\_image\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|
|Key Value \[cmdb\_key\_value\]|References|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|

## AWS Tag discovery

The Amazon AWS - Virtual Server \(LP\) pattern collects tags and populates them in the Key Value \[cmdb\_key\_value\] table.

|Field|Description|
|-----|-----------|
|Key \[key\]|Tag name.|
|Value \[value\]|Tag value.|
|Configuration item \[configuration\_item\]|References the Virtual Machine Instance \[cmdb\_ci\_vm\_instance\] table.|

## AWS BYOL discovery

Starting with Discovery and Service Mapping Patterns version 1.30.2, the pattern extension section discovers the following license types for Windows and Red Hat Enterprise Linux \(RHEL\) VMs:

-   Bring Your Own License \(BYOL\)
-   License included

The pattern stores the license type and model in the Key Value \[cmdb\_key\_value\] table.

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
</table>**Parent Topic:**[AWS discovery using patterns](../../discovery/reference/data-discovered-aws-patterns.md)

