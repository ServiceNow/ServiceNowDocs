---
title: PowerShell remoting for Discovery
description: Probe developers can use the PowerShell remote execution framework to automatically handle remote execution of scripts on target devices. The unified framework removes inconsistencies in remote execution, increases efficiency, and improves stability.
locale: en-US
release: xanadu
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [PowerShell for Discovery and Service Mapping, Advanced Discovery configuration, Discovery, ITOM Visibility, IT Operations Management]
---

# PowerShell remoting for Discovery

Probe developers can use the PowerShell remote execution framework to automatically handle remote execution of scripts on target devices. The unified framework removes inconsistencies in remote execution, increases efficiency, and improves stability.

## Requirements

To use PowerShell remote execution framework, the following requirements must be met:

-   The MID Server must be able to write to and read from the network share of the target.
-   The remote target must have PowerShell 3 or higher \(up to 5.1\).
-   For MID Servers using WinRM or WMI which choose to copy the script to the remote target, the MachinePolicy and UserPolicy scopes must be set to Undefined. If the script is not copied, the execution policy can be any other setting up to Restrictive.

See [Set up MID Servers to use PowerShell](../task/t_SetUpAMIDServerToUsePowerShell.md) for more information.

## Application discovery

The PowerShell remote execution framework has options for copying files to the remote target when executing a scan. Copying files to the target is important for probes like Windows — File discovery because its script invokes itself on the remote target to spawn off a new process. MID Servers using WMI to execute scripts remotely can experience an error with launchProcess if the script is too long. Copying the script to the remote target resolves this error. Copying a script to a remote target may result in anti-virus software on the target flagging the script. To avoid issues with anti-virus software, add the scripts to the permitted list in the anti-virus app.

## Probe configuration

The following is the configuration page for the Windows — Active Connections probe, which is included in the Windows — ADM multiprobe.

![Windows — Active Connections probe configuration page](../image/powershell-remote-probe-config.png)

The **Execute script remotely** check box is visible when the ECC queue topic is WMIRunner or PowerShell. When checked, the script executes on the remote target. Otherwise the script executes on the MID Server.

The **Copy script to target** check box is visible when **Execute script remotely** is checked. If **Copy script to target** is checked, then the script is copied to, and run on, the target. If **Copy script to target** is unchecked, then the script is executed on the target without copying it.

## PowerShell probe development

PowerShell remote execution framework is a unified method of executing PowerShell scripts, contained in a probe parameter, on a remote target server. The framework removes the need for probe developers to write their own remote execution code, which can cause inconsistencies between developers. The probe developer writes the script as if the probe was collecting information locally because the remote execution framework automatically handles remote script execution.

The framework handles remote execution whether the MID Server is configured to use WMI or WinRM. If the MID Server is configured for WMI, the probe uses launchProcess to execute commands on the remote target. Using launchProcess complicates remote execution and can cause failures. However, a MID Server configured for WinRM does not use launchProcess, and so is more efficient and stable.

**Parent Topic:**[PowerShell for Discovery and Service Mapping](../reference/r_PowerShellForDiscovery.md)

