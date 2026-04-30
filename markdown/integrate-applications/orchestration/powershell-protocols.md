---
title: PowerShell protocols and troubleshooting
description: PowerShell uses the Windows Management Instrumentation \(WMI\) and Windows Remote Management \(WinRM\) protocols to enable Orchestration activities to run commands on remote Windows hosts.
locale: en-US
release: zurich
product: Orchestration
classification: orchestration
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [PowerShell activity pack, Orchestration activity packs, Classic Orchestration, Workflow Data Fabric]
---

# PowerShell protocols and troubleshooting

PowerShell uses the Windows Management Instrumentation \(WMI\) and Windows Remote Management \(WinRM\) protocols to enable Orchestration activities to run commands on remote Windows hosts.

## Windows Management Instrumentation \(WMI\)

WMI provides a uniform interface for any local or remote applications or scripts that obtain management data from a computer system, a network, or an enterprise. WMI contains these components:

-   **Managed objects and WMI providers**: A WMI provider is a COM object that monitors one or more managed objects for WMI. A managed object is a logical or physical enterprise component, such as a hard disk drive, network adapter, database system, operating system, process, or service.
-   **WMI infrastructure**: The WMI infrastructure is a Microsoft Windows operating system component know as the WMI service \(winmgmt\). The WMI infrastructure is composed of the WMI Core and the WMI repository. The WMI repository is organized by WMI namespaces. The WMI service creates namespaces, such as `root\default, root\cimv2`, and `root\subscription`, at system startup and preinstalls a default set of class definitions, including the Win32 Classes, the WMI System Classes, and others. The remaining namespaces found on your system are created by providers for other parts of the operating system or products.
-   **WMI consumers**: A WMI consumer is a management application or script that interacts with the WMI infrastructure. A management application can query, enumerate data, run provider methods, or subscribe to events by calling either the COM API or the Scripting API for WMI.

## WMI installation and configuration

For the MID Server to successfully make a remote connection to the target host, TCP port 135 must be open. The Windows firewall automatically creates an inbound rule for WMI connectivity called Windows Management Instrumentation \(DCOM-In\).

## Windows Remote Management \(WinRM\)

WinRM is the Microsoft implementation of WS-Management Protocol, a standard Simple Object Access Protocol \(SOAP\) protocol that allows hardware and operating systems from different vendors to interoperate.

WinRM contains these components:

-   **WinRM Scripting API**: This scripting API enables Orchestration to obtain data from remote computers, using scripts that perform WS-Management protocol operations.
-   **WMI Service**: The WMI service continues to run side-by-side with WinRM and provides requested data or control through the WMI plug-in. You can continue to obtain data from standard WMI classes, such as as Win32\_Process.

## WinRM configuration

WinRM is automatically installed on Windows 2008 R2 and above operating systems, but must be configured before use.

1.  In a command prompt, enter **winrm quickconfig**. This command is not case sensitive.
2.  When the console displays **Make these changes \[y/n\]?**, enter **y**.

    The `winrm quickconfig` command performs the following operations:

    -   Starts the WinRM service, and sets the service startup type to **auto start**.
    -   Configures a listener for the ports that send and receive WS-Management protocol, using either HTTP or HTTPS on any IP address.
    -   Creates a firewall exception for the current user profile.

-   **[MID Server PowerShell files](mid-server-powershell-files.md)**  
PowerShell functions are stored in script files \(\*.ps1\) that use a PowerShell Script module \(\*.psm1\) file name extension.
-   **[PowerShell troubleshooting](../concept/powershell-troubleshooting.md#)**  
Authentication and access denied errors can prevent PowerShell activities from running a command on a target host.

**Parent Topic:**[PowerShell activity pack](../../../administer/orchestration-activities/concept/c_OrchestrPwrshellActivityPack.md)

