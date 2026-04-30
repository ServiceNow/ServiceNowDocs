---
title: Windows discovery
description: Discovery identifies and classifies information about Windows computers that use IPv4 addresses, IPv6 addresses, or both.
locale: en-US
release: yokohama
product: ITOM Visibility
classification: itom-visibility
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Operating systems discovery, Data collected by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Windows discovery

Discovery identifies and classifies information about Windows computers that use IPv4 addresses, IPv6 addresses, or both.

**Note:** For information on Probe to Pattern migration see the knowledge article [KB0694477](https://support.servicenow.com/kb_view.do?sysparm_article=KB0694477).

**Note:** admin$ share access is required for Windows discovery from Madrid P3 and later. A Remote Access role must be configured in the target Windows Server to enable connectivity with ServiceNow Discovery.

## Supported Windows versions

For IPv4 discovery:

-   Windows Workstation 7, 8, 10
-   Windows Server versions:
    -   2008
    -   2008R2
    -   2012R2
    -   2016
    -   2019
    -   2022
    -   2025

For IPv6 discovery:

-   Windows 2019 \(10.0.17763\)
-   Windows Server 2016
-   Windows Desktop 10
-   Windows 2019 Datacenter

**Note:** For fiber channel discovery on a Windows 2008 host, the Microsoft Fibre Channel Information Tool \(`fcinfo.exe`\) must be installed on that machine. The `fcinfo` executable should be available on the environment path. The Microsoft Fibre Channel Information Tool tool is available for download at [http://www.microsoft.com](http://www.microsoft.com).

## IPv6 supportability limitations

The following device types haven’t been verified for IPv6 discovery:

-   Printers
-   Network Storage \(NFS, CIFS, NAS, FC, ISCSI\)
-   Azure virtual machines \(IPv6 native mode isn’t supported by Microsoft\)

## Requirements

-   **Verify PowerShell support**

    ServiceNow now supports PowerShell 3.0 up to 5.1.

-   **Configure Windows credentials**

    For more information, see [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

-   **Verify user access**

    Verify that the user configured for the credential has the following permissions:

    -   Local admin access to the Windows machine.
    -   Access to the WMI service to the current namespace and subnamespaces.
    -   Access to the PowerShell service.
    -   Membership in the Distributed COM Users local security group.
-   **\(Optional\) Populate Virtual Machine Object field in Hardware \[cmdb\_ci\_hardware\] table**

    Starting with Discovery and Service Mapping Patterns version 1.30.2, you can improve query performance by populating the Virtual Machine Object field in the Hardware \[cmdb\_ci\_hardware\] table. For more information, see [Improved query performance with direct field population in CI tables](../../service-mapping/concept/query-service-account-ldc-fields.md).


## Classifiers, probes, and patterns

<table id="table_vdg_xb1_nbb"><thead><tr><th>

Classifiers

</th><th>

Probes

</th><th>

Patterns

</th></tr></thead><tbody><tr><td>

-   Windows
-   Windows 2008 Server
-   Windows 2012 Server
-   Windows 2016 Server
-   Windows 2025 Server

</td><td>

-   Horizontal discovery probe: Launches patterns
-   WMIRunner-Windows - Installed Software^
-   MultiProbe-Windows - ADM^
-   Windows - Identity\*
-   Windows - Network ARP Table\*
-   Windows - Network NDP Table\*
-   Windows - OS Information\*
-   Windows - Cluster\*
-   Windows - CPU/Memory\*
-   Windows - Installed Software\*
-   Windows - Printers\*
-   Windows - Storage 2008\*
-   Windows - Storage 2012\*
-   Windows - Amazon EC2\*
-   Windows - Azure\*
-   DNS\*
-   SNMP - Routing\*

</td><td>

-   Windows OS - Server
-   Windows OS - Desktops

</td></tr><tr><td>

Windows 2019 Server

</td><td>

N/A

</td><td>

Windows OS - Server

</td></tr></tbody>
</table>\*These probes aren't active on the classifier, as Discovery uses patterns by default for these discoveries.

^These probes remain active by default, even when Discovery uses pattern discovery.

To use patterns, verify that the correct pattern is specified in the horizontal pattern probe on the classifier. See [Add the Horizontal Pattern probe to a classifier](../concept/c-UsingPatternsForHorizontalDiscovery.md#) for instructions.

## Data collected

**Note:** See the knowledge article [KB0687582](https://support.servicenow.com/kb_view.do?sysparm_article=KB0687582) for information on model\_id and manufacturer.

|Label|Table name|Field name|Source|
|-----|----------|----------|------|
|Assigned to|cmdb\_ci\_win\_server|assigned\_to|wmi|
|Chassis type|cmdb\_ci\_win\_server|chassis\_type|wmi|
|Command|cmdb\_running\_process|command|wmi|
|Connects to|cmdb\_running\_process|connects\_to|wmi|
|CPU core count\*|cmdb\_ci\_computer|cpu\_core\_count|wmi|
|CPU core thread\*|cmdb\_ci\_computer|cpu\_core\_thread|wmi|
|CPU count\*|cmdb\_ci\_computer|cpu\_count|wmi|
|CPU manufacturer|cmdb\_ci\_computer|cpu\_manufacturer|wmi|
|CPU name|cmdb\_ci\_computer|cpu\_name|wmi|
|CPU speed \(MHz\)|cmdb\_ci\_computer|cpu\_speed|wmi|
|Default gateway|cmdb\_ci\_win\_server|default\_gateway|wmi|
|Description|cmdb\_ci\_disk|short\_description|wmi|
|Disk space \(GB\)|cmdb\_ci\_computer|disk\_space|wmi|
|Disk space \(GB\)|cmdb\_ci\_disk|disk\_space|wmi|
|DHCP enabled|cmdb\_ci\_network\_adapter|dhcp\_enabled|wmi|
|DNS domain|cmdb\_ci\_win\_server|dns\_domain|DNS|
|Free space \(GB\)|cmdb\_ci\_file\_system|free\_space|wmi|
|Hostname|cmdb\_ci\_win\_server|host\_name|DNS, NBT|
|IP address|cmdb\_ci\_network\_adapter|ip\_address|wmi|
|Listening on|cmdb\_running\_process|listening\_on|wmi|
|MAC address|cmdb\_ci\_network\_adapter|mac\_address|wmi|
|Manufacturer|cmdb\_ci\_win\_server|manufacturer|wmi|
|Model ID|cmdb\_ci|model\_id|wmi|
|Name|cmdb\_ci\_win\_server|name|DNS, NBT|
|Name|cmdb\_ci\_disk|name|wmi|
|Name|cmdb\_running\_process|name|wmi|
|Name|cmdb\_ci\_network\_adapter|name|wmi|
|Netmask|cmdb\_ci\_network\_adapter|netmask|wmi|
|Operating System|cmdb\_ci\_computer|os|wmi|
|OS domain|cmdb\_ci\_computer|os\_domain|NBT|
|OS service pack|cmdb\_ci\_computer|os\_service\_pack|wmi|
|OS version|cmdb\_ci\_computer|os\_version|wmi|
|Parameters|cmdb\_running\_process|parameters|wmi|
|PID|cmdb\_running\_process|pid|wmi|
|RAM \(MB\)|cmdb\_ci\_computer|ram|wmi|
|Serial number|cmdb\_ci\_win\_server|serial\_number|wmi|
|Short description|cmdb\_ci\_win\_server|short\_description|wmi|
|Type|cmdb\_ci\_disk|type|wmi|

\* Core counts and threads per core might not be accurate, due to issues with Microsoft reporting.

\*\* The value in the **disk\_space** field is an aggregation of the total capacity \(to include used space\) for all non-removable disks, including both directly attached and SAN storage.

## The Windows registry

Discovery can find software that has been installed on a Windows machine by looking at the Windows Registry. Discovery can find the following attributes of discovered software:

-   **Product Name**: Combination of name and version, such as Windows Imaging Component 3.0.
-   **Name**: Name of the product only without the version.
-   **Version**: Version of the product.
-   **Uninstall String**: Path to the uninstaller, such as `C:\Program Files\Notepad++\uninstall.exe`.
-   **Part of**: Update for which this registry is a part, such as Windows Internet Explorer 8 - Software U.
-   **Install Date**: The date the software was installed. The Windows - Installed Software sensor appends a timestamp of 00:00:00 to the install\_date retrieved from the registry. The installation time of all Windows software is independent of the time zone and is set to midnight of the day it was installed. For example, an install date of **2.19.2017** in the Windows registry appears as **2.19.2017 00:00:00** in the CMDB.
-   **Installed on**: The name of the asset on which the software is installed.

-   **[Windows server cluster discovery](r_WindowsServerClusterDiscovery.md)**  
Discovery establishes the relationships between a Windows server cluster and its nodes.

**Parent Topic:**[Operating systems discovery](../concept/c_Computers.md)

**Related topics**  


[Windows probes and permissions](r_DiscoWinProbesAndPermissions.md)

