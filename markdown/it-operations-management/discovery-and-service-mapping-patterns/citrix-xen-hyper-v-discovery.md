---
title: Citrix Xen Hyper-V Discovery
description: ServiceNow Discovery uses the Citrix Xen Hyper-V pattern to find and map instances. Discover these resources by installing the pattern applications from the ServiceNow Store and add Citrix Xen Hyper-V to the Linux Server Pattern’s Extension Section.
locale: en-US
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Available on-premise discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Citrix Xen Hyper-V Discovery

ServiceNow Discovery uses the Citrix Xen Hyper-V pattern to find and map instances. Discover these resources by installing the pattern applications from the ServiceNow Store and add Citrix Xen Hyper-V to the Linux Server Pattern’s Extension Section.

Use the Xen \(XE\) and \(XL\) commands to discover Citrix Xen Hyper-V, its components, and respective attributes. Discover information regarding the Hyper-V Server, Associated Pools, VMs, Network and Storage and their relationships with new and existing CIs.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Prerequisites

-   **Verify the following applications are up to date**
    -   Discovery and Service Mapping Patterns
    -   CMDB CI Class Models
-   **Verify pool admin RBAC role**

    This role is required for SSH access to the Linux server hosting the hypervisor and for executing all the necessary commands to extract information from the hypervisor environment. For more information on RBAC role permissions or adding Citrix users to a domain and assigning roles, see the [Citrix documentation](https://docs.citrix.com/).

-   **Verify MID Server reachability**

    Verify MID Server has reachability to the target device.

-   **Create SSH credentials with access to the target Linux host**

    For more information, see [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US)

-   **Create an extension section after the Linux Server pattern**

    Create an extension section after the Linux Server pattern and associate the **Citrix Xen HyperV** pattern to be triggered after the execution of the Linux Server discovery pattern. For more information on creating extension sections, see [Enhance patterns without changing their identification sections](../task/modify-pattern-using-extensions.md).


## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Citrix Xen HyperV pattern.

<table id="table_kwc_skj_vqb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

object\_id

</td><td>

UUID of the Hyper-V resource pool

</td></tr><tr><td>

name

</td><td>

Name of the Hyper-V resource pool

</td></tr><tr><td>

default\_sr

</td><td>

Default storage repository is where the VDIs are stored by default

</td></tr></tbody>
</table><table id="table_gx5_rts_wwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

object\_id

</td><td>

UUID of the Hyper-V Server

</td></tr><tr><td>

name

</td><td>

Name of the Hyper-V Server in format NAME@Hyper-V Server

</td></tr><tr><td>

serial\_number

</td><td>

Serial number of the Linux Server where the Citrix Xen Hyper-V server is running, in the format SERIAL-NUMBER\_hyper\_v\_server in order to distinguish from the Linux Server

</td></tr><tr><td>

manufacturer

</td><td>

Vendor of the Hyper-V Server

</td></tr><tr><td>

model\_id

</td><td>

Model ID of the Hyper-V Server

</td></tr><tr><td>

short\_description

</td><td>

Description of the Hyper-V Server

</td></tr><tr><td>

os

</td><td>

Operating system of the Hyper-V Server

</td></tr><tr><td>

os\_version

</td><td>

Version of the operating system of the Hyper-V Server

</td></tr><tr><td>

host\_name

</td><td>

Host name of the Hyper-V Server

</td></tr><tr><td>

ip\_address

</td><td>

IP address of the Hyper-V Server

</td></tr><tr><td>

virtual

</td><td>

Set to false, as this value is used by calculators to populate the IsVirtual flag on the dashboard \(SAM\).

</td></tr><tr><td>

free\_memory

</td><td>

Available memory of the Hyper-V Server

</td></tr><tr><td>

total\_memory

</td><td>

Total memory of the Hyper-V Server

</td></tr><tr><td>

edition

</td><td>

Edition of the Hyper-V Server

</td></tr><tr><td>

cpu\_core\_count

</td><td>

The number of cores per physical CPU

</td></tr><tr><td>

cpu\_count

</td><td>

Count of the total CPUs

</td></tr><tr><td>

ram

</td><td>

Total RAM memory in MB

</td></tr><tr><td>

cpu\_speed

</td><td>

CPU speed in MHz

</td></tr><tr><td>

cpu\_manufacturer

</td><td>

Manufacturer of the CPU

</td></tr><tr><td>

cpu\_type

</td><td>

Type of the CPU

</td></tr><tr><td>

cpu\_core\_thread

</td><td>

The number of threads per CPU core

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|object\_id|UUID of the Hyper-V Server|
|name|Name of the Hyper-V Server|
|state|State of the Hyper-V instance|
|ip\_address|IP address of the Hyper-V instance|
|host\_id|The UUID of the host where the instance is residing|
|baseboard\_serial|UUID of the Hyper-V instance|
|chassis\_serial|UUID of the Hyper-V instance|
|bios\_serial|UUID of the Hyper-V instance|

|Field|Description|
|-----|-----------|
|object\_id|UUID of the Hyper-V Virtual Network|
|pif\_uuid|UUID of the physical NIC|
|name|Name of the Hyper-V Virtual Network|
|bridge|Type of the network setup: either bridged or not|

|Field|Description|
|-----|-----------|
|object\_id|UUID of the Hyper-V network component|
|mac\_address|MAC address of the Hyper-V network component|
|vm|UUID of the Hyper-V instance, to which the network component is associated|
|name|Name of the Hyper-V network component|

|Field|Description|
|-----|-----------|
|object\_id|LUN of the Hyper-V storage|
|name|Name of the Hyper-V storage|
|description|Description of the Hyper-V storage|
|type|Type of the storage \(SR\)|
|vm\_object\_id|UUID of the Hyper-V instance, to which the storage is associated|
|vm\_id|UUID of the Hyper-V instance, to which the storage is associated|

|Field|Description|
|-----|-----------|
|object\_id|UUID of the virtual disk image \(VDI\)|
|name|Name of the virtual disk image \(VDI\)|
|description|Description of the virtual disk image \(VDI\)|
|type|Type of the storage component \(VDI\)|
|capacity|Total capacity of the virtual disk image \(VDI\)|
|location\_id|Location of the virtual disk image \(VDI\)|
|is\_a\_snapshot|Indication if the virtual disk image \(VDI\) is snapshot or not|
|snapshot\_of|Indication of VDI snapshot of the disks|
|snapshot\_time|Time of the snapshot creation|
|sr\_object\_id|UUID of the storage repository to which the virtual disk image \(VDI\) is associated|
|vm\_object\_id|UUID of the virtual machine associated with the virtual disk image \(VDI\)|

## CI Relationships

Relationships created by Citrix Xen Hyper-V Discovery

|Parent|Relationship|Child|
|------|------------|-----|
|cmdb\_ci\_hyper\_v\_resource\_pool|Contains :: Contained by|cmdb\_ci\_hyper\_v\_server|
|cmdb\_ci\_hyper\_v\_server|Runs on :: Runs|cmdb\_ci\_linux\_server|
|cmdb\_ci\_hyper\_v\_network|Provides :: Provided by|cmdb\_ci\_hyper\_v\_server|
|cmdb\_ci\_hyper\_v\_network\_comp|Provides :: Provided by|cmdb\_ci\_hyper\_v\_server|
|cmdb\_ci\_hyper\_v\_instance|Connected by :: Connects|cmdb\_ci\_hyper\_v\_network\_comp|
|cmdb\_ci\_hyper\_v\_resource\_pool|Reference|cmdb\_ci\_hyper\_v\_storage|
|cmdb\_ci\_hyper\_v\_instance|Contains :: Contained by|cmdb\_ci\_hyper\_v\_storage|
|cmdb\_ci\_hyper\_v\_storage\_comp|Managed by :: Manages|cmdb\_ci\_hyper\_v\_storage|
|cmdb\_ci\_hyper\_v\_storage\_comp|Reference|cmdb\_ci\_hyper\_v\_instance|
|cmdb\_ci\_hyper\_v\_server|Define resources for :: Gets resources from|cmdb\_ci\_hyper\_v\_resource\_pool|
|cmdb\_ci\_hyper\_v\_instance|Registered on :: Has registered|cmdb\_ci\_hyper\_v\_server|

**Parent Topic:**[Available on-premise discovery patterns](../concept/available-patterns.md)

