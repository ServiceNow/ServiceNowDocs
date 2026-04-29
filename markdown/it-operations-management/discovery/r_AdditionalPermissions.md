---
title: Discovery probe permissions
description: Several probes require additional permissions to run.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Discovery probe management, Discovery probes and sensors, Using Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Discovery probe permissions

Several probes require additional permissions to run.

## Discovering Active Connections

Discovery uses the Windows - Active Connections probe to access active connection information. The [application dependency mapping](r_ApplicationDependencyMapping.md#) feature requires this probe to function.

<table id="table_jrm_cq4_tp"><thead><tr><th>

Probes

</th><th>

Additional Permissions

</th></tr></thead><tbody><tr><td>

Windows - Active Connections

</td><td>

Ability to invoke the \\root\\CIMV2:Win32\_Process objectRead and Write access to the admin$ share

</td></tr></tbody>
</table>## Discovering Application Profiles

Discovery uses these probes to access application profile information.

<table id="table_hfb_tq4_tp"><thead><tr><th>

Probes

</th><th>

Additional Permissions

</th></tr></thead><tbody><tr><td>

Windows - Get APD Environment FilesWindows - Get APD Env File Content

 Windows - Get APD Version File Content

</td><td>

Ability to invoke the \\root\\CIMV2:Win32\_Process objectRead and Write access to the admin$ share

 Write access to the %SystemRoot%\\temp directory

</td></tr></tbody>
</table>## Discovering VMware Workstation

Discovery uses the **Windows - Get VMware Workstation** probe to access information about VMware virtual machines installed on Windows.

<table id="table_skp_dr4_tp"><thead><tr><th>

Probes

</th><th>

Additional Permissions

</th></tr></thead><tbody><tr><td>

Windows - Get VMware Workstation

</td><td>

Ability to invoke the \\root\\CIMV2:Win32\_Process objectRead and Write access to the **admin$ share**

 Write access to the **%SystemRoot%\\temp** directory

 Configure the **PATH** variable to include the path to the `vmrun.exe` command. This command is typically found in the VMware Workstation `install` directory.

</td></tr></tbody>
</table>## Discovering MSSQL

Discovery uses the Windows - MSSQL probe to access information about Microsoft SQL Server installed on Windows.

<table id="table_fdp_kr4_tp"><thead><tr><th>

Probes

</th><th>

Additional Permissions

</th></tr></thead><tbody><tr><td>

Windows - MSSQL

</td><td>

-   Access to the Win32\_Process object
-   Access to the Win32\_Service object
-   Access to the Win32\_NetworkAdapterConfiguration object
-   Access to the Microsoft.SqlServer.Management.Smo object
-   Access to run the nbtstat command
-   Access to HKLM\\SOFTWARE\\Microsoft\\Microsoft SQL Server\\InstalledInstances
-   Access to HKLM\\SOFTWARE\\Microsoft\\MSSQLServer\\$instanceName\\SuperSocketNetLib\\Tcp\\TcpPort where $instanceName is an array of possible values.

</td></tr></tbody>
</table>**Parent Topic:**[Discovery probe management](r_Probes.md)

**Related topics**  


[Discovery commands for probes and patterns](../concept/discovery-command-probe-pattern.md)

