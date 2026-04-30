---
title: Alibaba Cloud virtual machine \(VM\) pattern-based discovery
description: Discovery and Service Mapping Patterns uses the Alibaba - Virtual Machine \(LP\) pattern to discover VMs during horizontal discovery. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: yokohama
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2025-10-22"
reading_time_minutes: 2
keywords: [Alibaba, Virtual Machine]
breadcrumb: [Alibaba Cloud discovery, Available discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Alibaba Cloud virtual machine \(VM\) pattern-based discovery

Discovery and Service Mapping Patterns uses the Alibaba - Virtual Machine \(LP\) pattern to discover VMs during horizontal discovery. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

Verify the Alibaba Cloud discovery prerequisites section in [Alibaba Cloud discovery using patterns](../concept/alibaba-cloud-discovery-pattern.md).

## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Alibaba - Virtual Machine \(LP\) pattern.

<table id="table_ztj_yvl_dhc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \[name\]

</td><td>

Name of the instance.

</td></tr><tr><td>

Object ID \[object\_id\]

</td><td>

Instance ID.

</td></tr><tr><td>

State \[state\]

</td><td>

Status of the instance.For example: Running or Stopped.

</td></tr><tr><td>

CPUs \[cpus\]

</td><td>

Number of Virtual Central Processing Units \(vCPUs\).

</td></tr><tr><td>

Memory \(MB\) \[memory\]

</td><td>

Memory size in megabytes \(MB\).

</td></tr><tr><td>

Disks \[disks\]

</td><td>

Number of local disks attached to the instance.

</td></tr><tr><td>

Guest OS Name \[guest\_os\_fullname\]

</td><td>

Type of the operating system \(OS\) of the instance.Possible values are Windows or Linux.

</td></tr><tr><td>

Install Status \[install\_status\]

</td><td>

Install status of the instance. Default value is Installed.

</td></tr><tr><td>

Operational status \[operational\_status\]

</td><td>

Operational status of the instance. Default value is Operational.

</td></tr><tr><td>

Network adapters \[nics\]

</td><td>

Elastic Network Interfaces \(ENIs\) attached to the instance.

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|Name \[name\]|Name of the ENI.|
|Object ID \[object\_id\]|ID of the ENI.|
|MAC Address \[mac\_address\]|MAC address of the ENI.|
|Private IP \[private\_ip\]|Private IP address of the ENI.|
|IP Address \[ip\_address\]|Public IP addresses of instances.|
|Primary \[primary\]|A Boolean indicating whether a network interface is primary or secondary.|
|Node ID \[node\_id\]|Instance ID.|

<table id="table_yvs_wvl_dhc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object ID \[object\_id\]

</td><td>

ID of the image.-   IDs of public images contain the operating system version, architecture, language, and release date.

For example: **win2008r2\_64\_ent\_sp1\_en-us\_40G\_alibase\_20190318.vhd**.

-   IDs of custom, shared, and community images start with m.

For example: **m-0a1b2c3defghijklm4n5o**.


</td></tr><tr><td>

Provider \[provider\]

</td><td>

Image cloud provider: Alibaba.

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|Object ID \[object\_id\]|ID of the instance type.|
|Provider \[provider\]|Image cloud provider: Alibaba.|

## CI relationships

Discovery creates these relationships to support the Alibaba Cloud virtual machine discovery.

|CI|Relationship|CI|
|---|------------|---|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Implement End Point To::Implement End Point From|Cloud Mgmt Network Interface \[cmdb\_ci\_nic\]|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Hosted on::Hosts|Alibaba Datacenter \[cmdb\_ci\_alibaba\_datacenter\]|
|Availability Zone \[cmdb\_ci\_availability\_zone\]|Contains::Contained by|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Provisioned From::Provisioned|Cloud Image \[cmdb\_ci\_cloud\_os\_image\]|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Provisioned From::Provisioned|Cloud Hardware Type \[cmdb\_ci\_cloud\_hardware\_type\]|
|Cloud Image \[cmdb\_ci\_cloud\_os\_image\]|Hosted on::Hosts|Alibaba Datacenter \[cmdb\_ci\_alibaba\_datacenter\]|
|Key Value \[cmdb\_key\_value\]|References|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|

## Tag discovery

The Alibaba - Virtual Machine \(LP\) pattern collects tags and populates them in the Key Value \[cmdb\_key\_value\] table.

|Field|Description|
|-----|-----------|
|Key \[key\]|Tag key.|
|Value \[value\]|Tag value.|
|Configuration item \[configuration\_item\]|References the Virtual Machine Instance \[cmdb\_ci\_vm\_instance\] table.|

**Parent Topic:**[Alibaba Cloud discovery using patterns](../concept/alibaba-cloud-discovery-pattern.md)

