---
title: OCI virtual machine pattern-based discovery
description: Discovery and Service Mapping Patterns finds OCI virtual machines \(VMs\) on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/discovery-and-service-mapping-patterns/oracle-vm-pattern.html
release: zurich
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-07-12"
reading_time_minutes: 3
keywords: [Oracle OCI Virtual Machine, Oracle discovery, Oracle patterns, virtual machine pattern]
breadcrumb: [OCI discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# OCI virtual machine pattern-based discovery

Discovery and Service Mapping Patterns finds OCI virtual machines \(VMs\) on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

-   **Verify the OCI discovery prerequisites**

    For more information, see the prerequisites section in [Oracle Cloud Infrastructure \(OCI\) discovery]().

-   **Configure the Discovery schedule to support GovCloud**

    Discovering Oracle GovCloud \(US\) accounts requires using a datacenter URL when setting up an Oracle service account. For more information, see [Create OCI service accounts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/create-oci-service-accounts.md).


## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Oracle OCI - Virtual Machine \(LP\) pattern.

<table id="table_vm_instance"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \[name\]

</td><td>

The display name of the VM instance.

</td></tr><tr><td>

Object ID \[object\_id\]

</td><td>

A unique identifier, allocated by Oracle OCI for this resource.

</td></tr><tr><td>

CPUs \[cpus\]

</td><td>

The number of Oracle CPU \(OCPUs\) available to the instance.

</td></tr><tr><td>

Memory \(MB\) \[memory\]

</td><td>

The amount of memory available to the instance, in gigabytes.

</td></tr><tr><td>

IP Address \[ip\_address\]

</td><td>

The private IP address of the primary network interface attached to the instance.

</td></tr><tr><td>

State \[state\]

</td><td>

The current state of the virtual machine instance. For example: on, off, starting, stopping, scheduled, terminated, or error.

</td></tr><tr><td>

Install Status \[install\_status\]

</td><td>

Install status of the resource. Default value is Installed.

</td></tr><tr><td>

Operational status \[operational\_status\]

</td><td>

Operational status of the resource. Default value is Operational.

</td></tr></tbody>
</table><table id="table_os_template"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object ID \[object\_id\]

</td><td>

A unique identifier, allocated by Oracle OCI for this image.

</td></tr><tr><td>

Provider \[provider\]

</td><td>

The cloud provider, which is **OCI**.This field is only populated in the Cloud Image \[cmdb\_ci\_cloud\_os\_image\] table.

</td></tr></tbody>
</table>**Note:** When using the Image \[cmdb\_ci\_os\_template\] table to store Cloud OS images, you may notice an unusually large number of records. To avoid this issue, you can store the discovered OS images in the Cloud Image \[cmdb\_ci\_cloud\_os\_image\] table. For more information, see [Enable Cloud OS Image discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery-and-service-mapping-patterns/enable-cloud-os-image-discovery-pattern.md).

## CI relationships

The Oracle OCI - Virtual Machine \(LP\) pattern creates the following relationships and references to support OCI VM discovery. References link to records in other tables and don't appear in the CI Relationship \[cmdb\_rel\_ci\] table.

|CI|Relationship|CI|
|---|------------|---|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Hosted on::Hosts|OCI Datacenter \[cmdb\_ci\_oci\_datacenter\]|
|Availability Zone \[cmdb\_ci\_availability\_zone\]|Contains::Contained by|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|DR provided by::Provides DR for|Availability Zone \[cmdb\_ci\_availability\_zone\]|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Provisioned From::Provisioned|Image \[cmdb\_ci\_os\_template\] or Cloud Image \[cmdb\_ci\_cloud\_os\_image\]|
|Image \[cmdb\_ci\_os\_template\] or Cloud Image \[cmdb\_ci\_cloud\_os\_image\]|Hosted on::Hosts|OCI Datacenter \[cmdb\_ci\_oci\_datacenter\]|
|Server \[cmdb\_ci\_server\]|Virtualized by::Virtualizes|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Use End Point To::Use End Point From|VNIC Endpoint \[cmdb\_ci\_endpoint\_vnic\]|
|VNIC Endpoint \[cmdb\_ci\_endpoint\_vnic\]|Implement End Point To::Implement End Point From|Cloud Mgmt Network Interface \[cmdb\_ci\_nic\]|

|CI|Field|Referenced CI|
|---|-----|-------------|
|Key Value \[cmdb\_key\_value\]|Configuration item \[configuration\_item\]|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|

## OCI Tag discovery

The Oracle OCI - Virtual Machine \(LP\) pattern collects tags and populates them in the Key Value \[cmdb\_key\_value\] table.

|Field|Description|
|-----|-----------|
|Key \[key\]|Tag name.|
|Value \[value\]|Tag value.|
|Configuration item \[configuration\_item\]|References the Virtual Machine Instance \[cmdb\_ci\_vm\_instance\] table.|

**Parent Topic:**[Oracle Cloud Infrastructure \(OCI\) discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery-and-service-mapping-patterns/oracle-cloud-infrastructure-discovery.md)

