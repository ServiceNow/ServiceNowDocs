---
title: PowerShell activity pack
description: PowerShell is built on the Windows .NET Framework and is designed to control and automate the administration of Windows machines and applications.
locale: en-US
release: yokohama
product: Orchestration
classification: orchestration
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Orchestration activity packs, Classic Orchestration, Data and Automation]
---

# PowerShell activity pack

PowerShell is built on the Windows .NET Framework and is designed to control and automate the administration of Windows machines and applications.

Orchestration provides custom PowerShell activities that were created with the PowerShell activity designer template. These activities perform the same functions as PowerShell activities by the same name from previous releases and replace those activities for all new workflows. These custom activities give workflow administrators the ability to store input and output variables in the [databus](../../orchestration-activity-designer/concept/c_OrchestrationDatabus.md#).

**Note:** Existing workflows from earlier versions that were created with legacy PowerShell activities continue to function normally after an upgrade to Geneva. However, all new workflows must use these custom PowerShell activities.

Starting with the Yokohama release, there are the following updates to the PowerShell activity pack:

-   A new PowerShell probe \(V2\), which takes advantage of Integration Hub functionality
-   The ability to insert debug statements in the PowerShell scripts and produce the resulting messages at runtime

To use the PowerShell custom activities, you must [request activation](../task/t_ActivateAnActivityPack.md) of the Orchestration - PowerShell plugin. These activities are available in the Workflow Editor on the **Custom** tab. Expand the **Custom Activities** tree and select the PowerShell category for the activity you want to use.

ServiceNow supports PowerShell 3.0 to 5.1.

-   **[PowerShell activity designer](../../orchestration-activity-designer/concept/c_PowershellActivityDesigner.md)**  
PowerShell activities are configured to return data to a workflow from a host using Microsoft PowerShell.
-   **[PowerShell protocols and troubleshooting](../../../product/orchestration/reference/powershell-protocols.md)**  
PowerShell uses the Windows Management Instrumentation \(WMI\) and Windows Remote Management \(WinRM\) protocols to enable Orchestration activities to run commands on remote Windows hosts.
-   **[Join Domain activity](../reference/r_JoinDomainActivity.md)**  
The Join Domain activity joins a Windows computer to a domain.
-   **[Install Windows App activity](../reference/r_InstallWindowsAppActivity.md#)**  
The Install Windows App activity installs an application from an MSI package on a Windows target machine.
-   **[Change Service State activity](../reference/r_ChangeServiceState.md)**  
The Change Service State activity starts or stops a Windows service on a remote system.
-   **[Restart Windows Server activity](../reference/r_RestartWindowsServerActivity.md)**  
The Restart Windows Server activity stops and then restarts a Windows server using Powershell.
-   **[Uninstall Windows App activity](../reference/r_UninstallWindowsAppActivity.md)**  
The Uninstall Windows App activity uninstalls an application from a Windows target machine.

**Parent Topic:**[Orchestration activity packs](c_OrchestrationActivityPacks.md)

