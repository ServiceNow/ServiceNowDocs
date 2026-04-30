---
title: MID Server PowerShell files
description: PowerShell functions are stored in script files \(\*.ps1\) that use a PowerShell Script module \(\*.psm1\) file name extension.
locale: en-US
release: xanadu
product: Orchestration
classification: orchestration
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [PowerShell protocols and troubleshooting, PowerShell activity pack, Orchestration activity packs, Classic Orchestration, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# MID Server PowerShell files

PowerShell functions are stored in script files \(\*.ps1\) that use a PowerShell Script module \(\*.psm1\) file name extension.

The PowerShell functions are used by the PowerShell MID Server script files included in these activity packs:

-   Active Directory
-   Exchange
-   SCCM
-   PowerShell

## PSScript.ps1

This script performs a few tasks, such as credential testing, password encryption, and the execution of scripts configured in the Orchestration Activity Designer or in MID Script Files. However, this document focuses on how PSScript.ps1 uses the `credential.psm1` module for testing access to remote hosts.

The PowerShell variables are generally used directly in the [PowerShell execution command](../../../administer/orchestration-activity-designer/task/CreateInputVariables.md#) or as arguments in the MID Server script file you specify. There are special variables that are passed to PSScript.ps1, such as **credType**.

![Using credType in execution parameters](../image/credTypeExample.png "Using credType in execution parameters")

## PowerShell credTypes

The PowerShell credential types:

|Type|Description|
|----|-----------|
|WMI|testCredentialWMI|
|Exchange|testCredentilExchange|
|AD|testCredentilAD|
|SCCM|testCredentilSCCM|

If no credential type is passed to the PSScrip.ps1 script, the MID Server defaults to the WMI test function to test access to the target host. If there is a credential type used, the MID Server runs the corresponding test function for that credential type.

## Exit codes

These exit codes are returned from the PSScript.ps1 script and logged in the MID Server log file.

|Type|Test function|
|----|-------------|
|0|PowerShell command/script ran successfully.|
|1|Test finished successfully, but the command/script failed to execute.|
|2|Incorrect syntax passed to script.|
|3|All credentials including MID Server service account failed to execute the command/script.|
|4|Passed test and executed the activity, but an error was returned. Example user cannot be found.|

## DiagnosticsUtil.psm1

The MID Server uses this module file to perform PowerShell logging that assists debugging any Orchestration activity using PowerShell scripting. You can also add debugging statements directly to custom scripts.

<table id="table_sd2_vkl_4bb"><thead><tr><th>

Utility

</th><th>

Description

</th></tr></thead><tbody><tr><td>

SNCLog-DebugInfo

</td><td>

Log a debug message for a PowerShell script or PowerShell Orchestration activity. Examples: -   `SNCLog-DebugInfo -message "My debug message..."`
-   `SNCLog-DebugInfo "My debug message"`

</td></tr><tr><td>

SNCLog-ParameterInfo

</td><td>

Log a function parameter value. For `"function getHostName{ param( [String] $target )"`, the first value to the PowerShell hashtable is a string to indicate which function executes, and the values for each of the function parameters. Examples: -   Function with single parameter: `SNCLog-ParameterInfo @("Running getHostName", $target)`

**Note:** The debug message shows, '`Running getHostName $target:[actual value of $target]`'.

-   Function with multiple parameters: `SNCLog-ParameterInfo @("Running functionName", $param1, $param2, $param3)`

</td></tr><tr><td>

SNCObfuscate-Value

</td><td>

Use this utility to encrypt values for security purposes. The function displays `"$variableName":***`, where \*\*\* is the obfuscated value. Example: `SNCObfuscate-Value $password`

**Note:** The debug message reads: `"$password : ***"`.

</td></tr></tbody>
</table>## Credentials.psm1

The MID Server uses this module file to test access to a target host. The MID Server loops through all Windows credentials stored in its credentials table using the following access type functions, unless the PowerShell activity has a credential type \(**credType**\) defined. All ServiceNow® authored PowerShell activities are hard-coded to use a specific credential type. As a result, the MID Server only tests credential access against the designated function.

|Function|Description|
|--------|-----------|
|testCredentialWMI|Tests the given user and password on the target host using the **Get-WMI** object.|
|testCredentilAD|Tests the given user and password on the target host using the built-in **DirectoryEntry** object.|
|testCredentialExchange|Tests the given user and password to create a session on an Exchange host. This test uses the built-in PowerShell remoting feature on a remote host. WinRM is configured on Exchange servers by default.|
|testCredentialSCCM|Tests the given user and password to create a session on an SCCM server. This test uses the built-in PowerShell remoting feature on a remote host. This test requires WinRM to be configured.|
|testNoCredentialAccessWMI|Tests the given user and password on the target host, using the **Get-WMI** object. This test is used when no **credType** is used.|

**Note:** If the test passes using one of these functions, that credential is used to run the PowerShell script/command. If the tests fail to access the target host using these functions, the MID Server runs the PowerShell script/command under the account of the MID Server service.

This diagram illustrates the dependency of the credential selection behavior on the host being targeted by the PowerShell activity. If the target host is the IP address or host name of the MID Server, the MID Server bypasses all credentials in the Credentials table and uses the account of the MID Server service. If the target host is not the MID Server, then all Windows credentials are used first. If all credentials in the Credentials table are unsuccessful in running the PowerShell activity, then the MID Server uses the MID Server service account.

![PowerShell credential selection criteria](../image/PowerShellCredentialPickingDiagram.png "PowerShell credential selection criteria")

## ActiveDirectory.psm1

This module file stores the functions used by the PowerShell scripts shipped with the [Active Directory](../../../administer/orchestration-activities/concept/c_OrchActiveDirectoryActivities.md) activity pack.

## Exchange.psm1

This module file stores the functions used by the PowerShell scripts shipped with the [Exchange](../../../administer/orchestration-activities/concept/c_OrchestrationExchangeActivities.md) activity pack.

## SCCM.psm1

This module file stores the functions used by the PowerShell scripts shipped with the [SCCM](../../../administer/orchestration-activities/concept/c_SCCMActivityPack.md) activity pack.

**Parent Topic:**[PowerShell protocols and troubleshooting](powershell-protocols.md)

