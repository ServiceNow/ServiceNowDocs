---
title: Storage discovery
description: Discovery collects information on Direct Attached Storage \(DAS\), Storage Area Networks \(SAN\), and Network Attached Storage \(NAS\).
locale: en-US
release: zurich
product: ITOM Visibility
classification: itom-visibility
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Data collected by ITOM Visibility, ITOM Visibility reference, ITOM Visibility, IT Operations Management]
---

# Storage discovery

Discovery collects information on Direct Attached Storage \(DAS\), Storage Area Networks \(SAN\), and Network Attached Storage \(NAS\).

Storage can be located on specialized devices, such as Storage Arrays, Fibre Channel Switches, iSCSI disks, or on host operating systems, including Windows, Linux, and Solaris.

Discovery finds and maps dependencies for the following types of storage:

-   Direct-attached storage \(DAS\), network-attached storage \(NAS\), or storage area network \(SAN\).
-   NAS or SAN storage that is discovered via a Storage Management Initiative Specification \(SMI-S\) and Common Information Model \(CIM\).
-   Virtual storage for VMware ESX servers and Linux Kernel-based Virtual Machines \(KVM\). Discovery maps this storage to the underlying physical storage.

Discovery of storage via a host reconciles data and creates relationships between the host's file systems and associated local storage devices. The local storage devices represent the storage available to the host, whether it's directly attached or provided by Fibre Channel or iSCSI. This reconciliation assumes that the storage server has been discovered first.

**Note:** Tape storage drivers are not discovered.

Discovery collects and creates CIs in the CMDB for the following information:

-   File systems \(local and NAS\).
-   Disks \(both SAN disks and DAS drives\).
-   Fibre Channel \(FC\) HBAs and ports.
-   Linux Volume Manager \(LVM\) volumes. LVM volume data resides in the Storage Pool \[cmdb\_ci\_storage\_pool\] table.
-   [Veritas Volume Manager](../reference/r_DataCollDiscoVVMLinux.md) disks, subdisks, disk groups, plexes, and volumes.

**Note:** For details about the discovery of direct attached or multipath block storage provisioned on a Linux host, see [KB0622583](https://support.servicenow.com/kb_view.do?sysparm_article=KB0622583).

## Probes, sensors, and patterns

-   KVM - Storage Pools: identifies storage attached to KVM virtual machines.
-   Linux - Storage: identifies storage attached to systems running the Linux operating system.
-   Solaris - Storage: identifies storage attached to systems running the Solaris operating system.
-   Windows - Storage 2008: identifies storage attached to systems running Windows 2008.
    -   Windows - Storage 2008 - PS: identifies storage attached to systems running Windows 2008, using the PowerShell.
    -   Windows - Storage 2008 - WMI: identifies storage attached to systems running Windows 2008, using WMI Runner.
-   Windows - Storage 2012: identifies storage attached to systems running Windows 2012 and later.
    -   Windows - Storage 2012 - PS: identifies storage attached to Windows systems, using PowerShell.
    -   Windows - Storage 2012 - WMI: identifies storage attached to Windows systems, using WMI Runner.
-   VMWare - vCenter ESX Hosts Storage: collects information about ESX servers and creates relationships from datastores to underlying disks.
-   Patterns for [NetApp storage discovery](netapp-discovery.md):

    -   NetApp 7-mode: finds NetApp servers via REST with two nodes.
    -   NetApp cluster mode: finds NetApp servers via REST when more than two nodes are connected through a cluster interconnect switch.
    **Note:** For information on Probe to Pattern migration see the knowledge article [KB0694477](https://support.servicenow.com/kb_view.do?sysparm_article=KB0694477).


## Requirements

-   **Windows**
    -   Supports the following configurations:
        -   Windows Server 2012, DAS or NAS with Fibre Channel \(FC\) or Internet Small Computer System Interface \(iSCSI\).
        -   Windows Server 2008, DAS or NAS with FC or iSCSI.
    -   Install the `fcinfo.exe` tool on Windows 2008 and 2012 servers that attach to storage via FC.
    -   Install Windows Management Instrumentation \(WMI\).
    -   Enable Powershell on the MID Server host server.
    -   Provide the instance with the necessary credentials to the host server.
    -   Put the MID Server and the target machine in the same domain or add the target machine to the trusted host list on the MID Server machine.
    -   Optionally, install [Windows Remote Management \(WinRM\)](https://msdn.microsoft.com/en-us/library/aa384372%28v=vs.85%29.aspx) on the host server to discover Fibre Channel information. WinRM is on by default for Windows 2012 and Windows 2016 machines, but not for Windows 2008.
-   **Linux**
    -   Supports the following configurations:
        -   Solaris, DAS, NAS, or SAN with iSCSI
        -   CentOS, DAS, NAS, or SAN with FC or iSCSI
        -   Ubuntu Server, DAS, NAS, or SAN with iSCSI
    -   Provide the device with SSH credentials that have root or sudo access.
    -   Provide the MID Server with the necessary credentials to the host server.

## Relationships

Discovery creates the following relationships for storage CIs:

|Parent Component|Relationship|Child Component|
|----------------|------------|---------------|
|Storage Export \[cmdb\_ci\_storage\_export\]|Exports to::Imports from|Storage Device \[cmdb\_ci\_storage\_device\]|
|Fibre Channel Disk \[cmdb\_ci\_fc\_disk\]|Provides::Provided by|File System \[cmdb\_ci\_file\_system\]|
|iSCSI Disk \[cmdb\_ci\_iscsi\_disk\]|Provides::Provided by|File System \[cmdb\_ci\_file\_system\]|

-   **[Configure discovery of hosts with attached storage](configure-discovery-of-hosts-with-attached-storage.md)**  
Discovery can find information about UNIX, Linux, and Windows hosts with attached storage.
-   **[Discovery data collected for storage via a host](../reference/r_DataCollDiscoStorageViaHost.md)**  
Discovery gathers information about storage units that connect to Linux, Solaris, and Windows hosts via a local I/O port or Host Bus Adapter \(HBA\).
-   **[Storage Discovery via SMI-S and CIM](../reference/r_DataCollDiscoStorageviaSMISCIM.md)**  
Discovery can explore storage devices that contain a Storage Management Initiative Specification \(SMI-S\) provider that is a specialized Common Information Model \(CIM\) server.
-   **[Data collected for Veritas Volume Manager on Linux](../reference/r_DataCollDiscoVVMLinux.md)**  
Discovery collects disk and volume information for Veritas Volume Manager \(VxVM\) on Linux hosts and maps file systems mounted on Veritas volumes to the upstream storage provider.
-   **[NetApp Server and Cluster discovery](netapp-discovery.md)**  
Discovery and Service Mapping find NetApp servers and clusters using patterns. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[Manage large storage payloads in Linux and Solaris](../task/manage-lg-payloads-linux-solaris.md)**  
Large payloads for Linux and Solaris direct attached storage can cause out of memory errors if not configured to serialize the processing of the payload.
-   **[Storage discovery examples](../reference/storage-discovery-examples.md)**  
Discovery creates configuration items \(CI\) and CI relationships for physical and logical storage components attached directly to application and database servers or by fibre channel switched fabric in a multi-path configuration.

**Parent Topic:**[Data collected by ITOM Visibility](../reference/data-collected-by-itom-visibility.md)

