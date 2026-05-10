---
title: PowerShell for Discovery and Service Mapping
description: MID Servers use PowerShell and PowerShell Remoting for accessing configuration items \(CIs\) during horizontal and top-down discovery. Review MID Server parameters and script includes, probe parameters, and credentials for using PowerShell.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Advanced Discovery configuration, Configuring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# PowerShell for Discovery and Service Mapping

MID Servers use PowerShell and PowerShell Remoting for accessing configuration items \(CIs\) during horizontal and top-down discovery. Review MID Server parameters and script includes, probe parameters, and credentials for using PowerShell.

PowerShell is used to control and automate the administration of Windows servers and applications.

MID Servers can use PowerShell to directly communicate with Windows servers using both WMI and WinRM protocols. For Windows services using the WinRM protocol, the PowerShell process establishes a secure PSSession \(PowerShell Remoting session\) that stays open until the MID Server finishes querying a Windows server. For Windows servers using the WMI protocol, the PowerShell process sends every PowerShell command with credentials.

PowerShell is also the preferred method for performing discovery over multiple Windows domains. PowerShell allows a single MID Server to authenticate on servers on different domains using credentials stored on the instance.

If you do not configure MID Servers to use PowerShell and PowerShell Remoting, MID Servers use WMI.

## How PowerShell Discovery works

The following descriptions explain how MID Servers use PowerShell to deploy probes.

-   **Probe and sensor**

    When a Windows machine is classified with PowerShell, and an MSSQL instance is detected, a probe called **Windows - MSSQL** is launched. The probe returns the SQL database catalogs and version to a matching sensor.

-   **Probe parameter**

    The **WMI\_ActiveConnections.ps1** probe parameter contains a script that runs `netstat.exe` on a target server when PowerShell is enabled. This script extracts the information on Windows server connections, such as process IDs, ports, and IP addresses.

-   **Credentials**

    Discovery uses Windows PowerShell credentials from the Credentials \[discovery\_credentials\] table or the domain administrator credentials of the MID Server service. If Discovery cannot find PowerShell credentials in the Credentials table of the type \(Windows\) it uses the login credentials of the MID Server service.

-   **MID Server Script Includes**

    The following script includes were added for PowerShell discoveries. These scripts run on the MID Server to generate the scripts that Discovery uses for WMIRunner and PowerShell.

    -   GenerateWMIScriptJS: Generates a Javascript script for the WMIRunner probe.
    -   GenerateWMIScriptPS1: Generates a PowerShell script for PowerShell discovery.
-   **MID Server parameters for PowerShell**

    Optional parameters for the MID Server can be found at [MID Server parameters for PowerShell](mid-server-parameter-powershell.md). After changing the setting for any parameter, be sure to restart the MID Server service.


## PowerShell version requirements

MID Servers using PowerShell must be installed on a supported Windows operating system. ServiceNow supports these PowerShell versions:

-   **Version 3.0**
    -   Regular Discovery
    -   Application Dependency Mapping \(ADM\)
    -   File-based Discovery
    -   PowerShell version 3.0 does not support Windows Server 2003.
-   **Version 4.0**
    -   Regular Discovery
    -   Application Dependency Mapping \(ADM\)
    -   File-based Discovery
-   **Version 5.0**
    -   Regular Discovery
    -   Application Dependency Mapping \(ADM\)
    -   File-based Discovery

**Note:** PowerShell version 6.0 is **not** supported. Many of the cmdlets that discovery relies on have been removed from this version. For example, only cmdlets using WinRM are available for remote operations.

## Windows PowerShell execution policies

Windows PowerShell has four different execution policies. Customers can set the script execution policies with their group policy settings. For more information, see the Microsoft website for [PowerShell](https://docs.microsoft.com/en-us/powershell/) documentation.

-   Restricted: No scripts can be run. Windows PowerShell can be used only in interactive mode.
-   AllSigned: Only scripts signed by a trusted publisher can be run.
-   RemoteSigned: Downloaded scripts must be signed by a trusted publisher before they can be run.
-   Unrestricted: No restrictions; all scripts can be run.

**Note:** If you have any policy other than Unrestricted, the script needs to be signed.

-   **[Set up MID Servers to use PowerShell](../task/t_SetUpAMIDServerToUsePowerShell.md)**  
Configure MID Servers in your organization to use PowerShell for horizontal and top-down discovery of Windows servers.
-   **[PowerShell remoting for Discovery](../concept/powershell-remoting.md)**  
Probe developers can use the PowerShell remote execution framework to automatically handle remote execution of scripts on target devices. The unified framework removes inconsistencies in remote execution, increases efficiency, and improves stability.
-   **[PowerShell commands run by Discovery](powershell-cmdlets-run-by-discovery.md)**  
These are the PowerShell cmdlets and their parameters that Discovery runs to control and automate the administration of Windows servers and applications. Included are the probe parameters and MID Server scripts that contain the commands.
-   **[MID Server parameters for PowerShell](mid-server-parameter-powershell.md)**  
Parameters control the behavior of a particular MID Server and have lower precedence than MID Server properties.

**Parent Topic:**[Advanced Discovery configuration](../concept/c_DiscoveryExtendedCapabilities.md)

