---
title: Hyper-V discovery
description: The ServiceNow Discovery application finds Microsoft Hyper-V hypervisors in your environment.When importing \(cloning\) Hyper-V virtual machines, make sure each virtual machine has a unique ID. Discovery identifies virtual machines with duplicate IDs as the same machine.
locale: en-US
release: xanadu
product: ITOM Visibility
classification: itom-visibility
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 7
breadcrumb: [Operating systems discovery, Data collected by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Hyper-V discovery

The ServiceNow Discovery application finds Microsoft Hyper-V hypervisors in your environment.

Hyper-V is a hypervisor developed by Microsoft that enables you to create and manage virtual machines \(VMs\) on a physical server or computer. It enables hardware virtualization, enabling multiple virtual machines to run on a single physical machine while sharing the underlying hardware resources, such as CPU, memory, storage, and networking.

**Note:** See the knowledge article [KB0687582](https://support.servicenow.com/kb_view.do?sysparm_article=KB0687582) for information on model\_id and manufacturer.

Hyper-V supports the following functionality:

-   Failover clustering: Failover is managed with Failover Cluster Manager.
-   Live migration: Virtual machines can be moved between failover cluster nodes without bringing down the virtual machine.

**Note:** For information on Probe to Pattern migration see the knowledge article [KB0694477](https://support.servicenow.com/kb_view.do?sysparm_article=KB0694477).

## Supported versions

Discovery is supported for Hyper-V running on the following Windows Server versions:

-   2008
-   2012
-   2012 R2
-   2016
-   2019
-   2022
-   2025

**Important:** Discovery of Hyper-V running on Windows starting from version 2016 supports pattern discovery only. If you upgraded and are still using probes and sensors for discovery, see [KB0694773](https://support.servicenow.com/nav_to.do?uri=%2Fkb_view.do%3Fsys_kb_id%3D86df2e9adb3793045ed4a851ca9619e3) for instructions on configuring Hyper-V probes.

## Hyper-V data models

There are 2 types of Hyper-V:

-   Hyper-V on Windows Server: This model, installed as a server role on Windows Servers, is designed for enterprises needing both virtualization and other server roles \(for example: file servers, Active Directory, web servers\) on the same machine.
-   Hyper-V Server \(Standalone\): A free, lightweight version of Windows Server specifically designed for virtualization. It includes only the Hyper-V hypervisor and no graphical user interface \(GUI\) or additional server roles.

Discovery supports identifying and mapping both types of Hyper-V environments. However, the CMDB data models differ between the two deployment types.

![Key differences between Windows Server with Hyper-V role and Hyper-V Server using a VM with Windows OS example](../../service-mapping/image/MMASSET0020901-hyper-v-data-model-horizontal.png "Example of Windows Server with Hyper-V role vs. Hyper-V Server (VM shown with Windows OS)")

<table id="table_jqg_nht_qdc"><thead><tr><th>

Key aspects

</th><th>

Windows Server with Hyper-V role

</th><th>

Hyper-V Server

</th></tr></thead><tbody><tr><td>

Hyper-V Server CI

</td><td>

-   Name of the CI includes the **@Hyper-V Server** suffix. For example: hyperv1@Hyper-V Server.
-   The **Windows Host** field references the parent Windows Servers table, which represents the physical host of the Hyper-V Server.

</td><td>

Name of the CI is the Hyper-V Server.

</td></tr><tr><td>

Hyper-V Cluster has **Members::Member of** relationship with Hyper-V Server

</td><td>

YesThe Hyper-V Server table:

-   Has **Is virtual** field set to true
-   Doesn't have software installation

</td><td>

YesThe Hyper-V Server table:

-   Has **Is virtual** field set to false
-   Doesn't have software installation

</td></tr><tr><td>

Hyper-V Server has **Runs on::Runs** relationship with Windows Server

</td><td>

YesThe Windows Server table:

-   Represents the physical host
-   Has **Is virtual** field set to false
-   Has Windows Server software installation

</td><td>

No

</td></tr><tr><td>

Operating system \(OS\) installed on the VM has **Virtualized by::Virtualizes** relationship with Hyper-V Server

</td><td>

YesThe OS table \(for example: Windows Server/Linux Server\):

-   Represents the individual virtual machines \(VMs\)
-   Has **Is virtual** field set to true
-   Has OS software installation, such as Windows or Linux Server
-   Has other software installations deployed on the VM

</td><td>

YesThe OS table \(for example: Windows Server/Linux Server\):

-   Has **Is virtual** field set to true
-   Has OS software installation, such as Windows or Linux Server
-   Has other software installations deployed on the VM

</td></tr><tr><td>

OS installed on the VM has **Instantiates::Instantiated by** relationship with Hyper-V Virtual Machine Instance

</td><td>

Yes

</td><td>

Yes

</td></tr><tr><td>

CPU cores count

</td><td>

Is identical between the physical Windows Server host and the Hyper-V Server

</td><td>

The parent Windows Servers table reflects the physical cores, while the Hyper-V Server table displays the virtual cores

</td></tr></tbody>
</table>## Credentials

Configure [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US) with Domain administrator rights. You should also [Enable PowerShell](r_PowerShellForDiscovery.md) for the MID Server used to discover Hyper-V servers and instances.

## Classifier, probes, and pattern

<table id="table_vxz_csf_nbb"><thead><tr><th>

Classifier

</th><th>

Probes

</th><th>

Pattern

</th></tr></thead><tbody><tr><td>

Hyper-V ServerThe classification applies to standalone Hyper-V servers only \(servers NOT running on Windows 2008\).

</td><td>

-   Horizontal discovery probe: Launches patterns
-   Windows - ADM^
-   Windows - Installed Software^
-   Hyper-V - Cluster\*
-   Hyper-V - Resource Pools\*
-   Hyper-V - Virtual Machines\*
-   Hyper-V - Virtual Networks\*
-   Several other [Windows probes](r_DataCollDiscoWindowsComputers.md) also run, such as Windows - Identity, Windows - software, and so on.\*

</td><td>

Hyper-V Server

</td></tr></tbody>
</table>\*These probes aren't active on the classifier, as Discovery uses patterns by default for these discoveries.

^These probes remain active by default, even when Discovery uses pattern discovery.

To use patterns, verify that the correct pattern is specified in the horizontal pattern probe on the classifier. See [Add the Horizontal Pattern probe to a classifier](../concept/c-UsingPatternsForHorizontalDiscovery.md#) for instructions.

## Data collected by Discovery during horizontal discovery

<table id="table_qlk_ctw_gpb"><thead><tr><th>

Label

</th><th>

Field Name

</th><th>

Data Description

</th><th>

Stored in Table

</th></tr></thead><tbody><tr><td>

Object ID ^

</td><td>

object\_id

</td><td>

ID

</td><td>

`cmdb_ci_hyper_v_instance`

</td></tr><tr><td>

Name^

</td><td>

name

</td><td>

name

</td><td>

`cmdb_ci_hyper_v_instance`

</td></tr><tr><td>

State

</td><td>

state

</td><td>

-   On
-   Off

</td><td>

`cmdb_ci_hyper_v_instance` \*

</td></tr><tr><td>

CPUs

</td><td>

cpus

</td><td>

Count

</td><td>

`cmdb_ci_hyper_v_instance` \*

</td></tr><tr><td>

Memory

</td><td>

memory

</td><td>

Quantity in MB

</td><td>

`cmdb_ci_hyper_v_instance` \*

</td></tr><tr><td>

Network adapters

</td><td>

nics

</td><td>

Count

</td><td>

`cmdb_ci_hyper_v_instance` \*

</td></tr><tr><td>

Disks

</td><td>

disks

</td><td>

Count+

</td><td>

`cmdb_ci_hyper_v_instance` \*

</td></tr><tr><td>

Disks size

</td><td>

disks\_size

</td><td>

Capacity in GB+

</td><td>

`cmdb_ci_hyper_v_instance` \*

</td></tr><tr><td>

Virtual Base Board Serial Number

</td><td>

baseboard\_serial

</td><td>

Virtual serial number

</td><td>

`cmdb_ci_hyper_v_instance`

</td></tr><tr><td>

BIOS Serial Number

</td><td>

bios\_serial

</td><td>

Virtual serial number

</td><td>

`cmdb_ci_hyper_v_instance`

</td></tr><tr><td>

Chassis Serial Number

</td><td>

chassis\_serial

</td><td>

Virtual serial number

</td><td>

`cmdb_ci_hyper_v_instance`

</td></tr><tr><td>

BIOS GUID

</td><td>

bios\_guid

</td><td>

Globally unique identifier \(GUID\)

</td><td>

`cmdb_ci_hyper_v_instance`

</td></tr></tbody>
</table>\*Attributes that are put in the `cmdb_ci_hyper_v_instance` table when using the Hyper-V Server pattern. For upgrades, probes and sensors continue to put these attributes in the `cmdb_ci_vm_instance` table.

^Newly discovered attribute when using the Hyper-V Server pattern.

+Discovery can only return this information if the virtual machine is running.

|Label|Field|Store in table|
|-----|-----|--------------|
|Name|name|`cmdb_ci_hyper_v_server`|
|Chassis type|chassis\_type|`cmdb_ci_hyper_v_server`|
|Description|short\_description|`cmdb_ci_hyper_v_server`|
|OS Address Width \(bits\)|os\_address\_width|`cmdb_ci_hyper_v_server`|
|Operating System|OS|`cmdb_ci_hyper_v_server`|
|Host name|hostname|`cmdb_ci_hyper_v_server`|
|IP Address|ip\_address|`cmdb_ci_hyper_v_server`|
|OS Version|os\_version|`cmdb_ci_hyper_v_server`|
|OS Service Pack|os\_service\_pack|`cmdb_ci_hyper_v_server`|
|Is virtual|virtual|`cmdb_ci_hyper_v_server`|

|Label|Field Name|Data Description|Stored in Table|
|-----|----------|----------------|---------------|
|Name|name|Name of the virtual network|`cmdb_ci_hyper_v_network` \*|
|ID|object\_id|Globally unique identifier \(GUID\)|`cmdb_ci_hyper_v_network` \*|

\*Attributes that are put in the `cmdb_ci_hyper_v_network` table when using the Hyper-V Server pattern. For upgrades, probes and sensors continue to put these attributes in the `cmdb_ci` table \(name\) and the `cmdb_ci_vm_object` table \(object\_id\).

|Label|Field Name|Data Description|Stored in Table|
|-----|----------|----------------|---------------|
|Name^|name|Name of the resource pool.|`cmdb_ci_hyper_v_resource_pool`|
|ID|object\_id|Globally unique identifier \(GUID\)|`cmdb_ci_hyper_v_rpool_comp`|
|Capacity|capacity|Maximum amount of the appropriate allocation unit|`cmdb_ci_hyper_v_rpool_comp`|
|Allocation units|allocation\_units|Units of measurement used \(for example, MB or GB\)|`cmdb_ci_hyper_v_rpool_comp`|
|Resource type|resource\_type|Type of resource discovered \(for example, memory, or hard drive space\)|`cmdb_ci_hyper_v_rpool_comp`|

|Label|Field Name|Data Description|Stored in Table|Reference Table|
|-----|----------|----------------|---------------|---------------|
|Windows Cluster|name|Reference field displaying the Windows Cluster on which the Hyper-V cluster resides.|`cmdb_ci_hyper_v_cluster`|`cmdb_ci_win_cluster`|

## Relationships

Discovery creates records in the CMDB for the host machine, the parent partition running Windows Server 2008, and all the virtual machines running on the Hyper-V server. Discovery finds the stored templates and maps all the relationships between components.

The instance modifies these tables for use with multiple virtualization products:

<table id="table_eyp_ttf_nbb"><thead><tr><th>

Table

</th><th>

Purpose

</th></tr></thead><tbody><tr><td>

Virtualization Server \[cmdb\_ci\_virtualization\_server\]

</td><td>

Contains data on all discovered virtualization servers.

</td></tr><tr><td>

Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]

</td><td>

Contains data on all discovered virtual machine instances.

</td></tr><tr><td>

Virtual Machine Object \[cmdb\_ci\_vm\_object\]

</td><td>

Contains data about various objects associated with a Hyper-V server, such as partitions, networks, resource pools, and clusters.

</td></tr></tbody>
</table>|Parent table|Relationship|Child table|
|------------|------------|-----------|
|Hyper-V Virtual Machine Instance \[cmdb\_ci\_hyper\_v\_instance\]|Registered on::Has registered|Hyper-V Server \[cmdb\_ci\_hyper\_v\_server\]|
|Hyper-V Virtual Machine Instance \[cmdb\_ci\_hyper\_v\_instance\]|Connected by ::Connects|Hyper-V Network \[cmdb\_ci\_hyper\_v\_network\]|
|Hyper-V Network \[cmdb\_ci\_hyper\_v\_network\]|Provided::Provides|Hyper-V Server \[cmdb\_ci\_hyper\_v\_server\]|
|Hyper-V Resource Pool \[cmdb\_ci\_hyper\_v\_resource\_pool\]|Defines resources for:Gets resources from|Hyper-V Server \[cmdb\_ci\_hyper\_v\_server\]|
|Hyper-V Resource Pool Components \[cmdb\_ci\_hyper\_v\_rpool\_comp\]|Contained by::Contains|Hyper-V Resource Pool \[cmdb\_ci\_hyper\_v\_resource\_pool\]|
|Hyper-V Cluster \[cmdb\_ci\_hyper\_v\_cluster\]|Members::Member of|Hyper-V Server \[cmdb\_ci\_hyper\_v\_server\]|
|Hyper-V Server \[cmdb\_ci\_hyper\_v\_server\]|Runs on::Runs|Windows Servers \[cmdb\_ci\_win\_server\]|
|Windows Servers \[cmdb\_ci\_win\_server\]|Instantiates::Instantiated by|Hyper-V Virtual Machine Instance \[cmdb\_ci\_hyper\_v\_instance\]|
|Windows Servers \[cmdb\_ci\_win\_server\]|Virtualized by::Virtualizes|Hyper-V Server \[cmdb\_ci\_hyper\_v\_server\]|

**Parent Topic:**[Operating systems discovery](../concept/c_Computers.md)

## Clone Hyper-V virtual machines

When importing \(cloning\) Hyper-V virtual machines, make sure each virtual machine has a unique ID. Discovery identifies virtual machines with duplicate IDs as the same machine.

1.  Export the virtual machine from the Hyper-V server.
2.  Import the virtual machine into a different server, making one of the these choices:
    -   Move or restore the virtual machine: This selection clones the image, using the same ID, and moves it to another server. The original image remains on the Hyper-V server.
    -   Copy the virtual machine: This selection copies the virtual machine, using a different ID, and moves it from the Hyper-V server. This is the best selection and does not require any further action before you run Discovery.
3.  If you import the Hyper-V clone using the **Move or restore** selection, be sure to delete the original image from the Hyper-V server.

    When Discovery encounters two virtual machines with the same equivalent serial numbers, it creates only one configuration item \(CI\).


