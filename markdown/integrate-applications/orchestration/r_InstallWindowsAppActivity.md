---
title: Install Windows App activity
description: The Install Windows App activity installs an application from an MSI package on a Windows target machine.To install software on Windows machines using the Install Windows App activity, enable WMI Windows Installer provider on all target machines.
locale: en-US
release: zurich
product: Orchestration
classification: orchestration
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [PowerShell activity pack, Orchestration activity packs, Classic Orchestration, Workflow Data Fabric]
---

# Install Windows App activity

The Install Windows App activity installs an application from an MSI package on a Windows target machine.

**Note:** This activity replaces a Powershell activity by the same name available in releases prior to Geneva. If you have a workflow created in a previous version that uses the deprecated activity, your workflow will continue to work normally after upgrading to Geneva. However, all new workflows must use the custom version of this activity. This activity was built with the [PowerShell activity designer](../../orchestration-activity-designer/concept/c_PowershellActivityDesigner.md), which gives workflow administrators the ability to store input and output variables in the [databus](../../orchestration-activity-designer/concept/c_OrchestrationDatabus.md#).

## Input variables

|Variable|Description|
|--------|-----------|
|hostname|Hostname or IP address of the target Windows machine on which the service is installed. Use the Resolve DNS [MID Server capabilities](https://www.servicenow.com/docs/access?context=t_ConfigureCapabilities&version=zurich&pubname=zurich-servicenow-platform&section=r_MIDServerCapabilities&ft:locale=en-US) to resolve hostnames into IP addresses.|
|installerpath|Path to the installer. The installer can be on any machine that is visible to both the MID Server and the target machine \(local drive, UNC path, mapped drive, etc.\).|
|installer|Name of the installer file, such as `winzip150.msi`. The installer must be an MSI package.|
|arguments|The parameter that contains the command line arguments to the MSI package. These are name=value pairs, separated by a space. For example, the argument might appear as: `INSTALLDIR=c:\myinstallfolder ADDDESKTOPICON=0`. These arguments are dependent on the what the actual MSI being installed defines. If there are no arguments, leave the field empty.|

## Output variables

|Variable|Description|
|--------|-----------|
|result|Either **success** or **failure**.|
|errorMessage|The **executionResult.errorMessages** from the [Activity designer parsing sources](../../orchestration-activity-designer/task/t_CreateAParsingRule.md#).|

## Conditions

The activity state tells the workflow engine what to do with the activity.

|Name|Description|
|----|-----------|
|Success|The Windows application was successfully installed on the target machine.|
|Failure|The Windows application failed to install on the target machine|

**Parent Topic:**[PowerShell activity pack](../concept/c_OrchestrPwrshellActivityPack.md)

## Enable WMI Windows Installer provider

To install software on Windows machines using the Install Windows App activity, enable WMI Windows Installer provider on all target machines.

### Before you begin

-   It is recommended that the MID Server, the target machine, and the installer source machine be on the same Active Directory domain. However, if these computers are on separate domains, those domains must have a [trust relationship](http://technet.microsoft.com/en-us/library/cc961481.aspx) established between them.
-   If the installer path is a [UNC file sharing](http://compnetworking.about.com/od/windowsnetworking/g/unc-name.htm) machine, the Active Directory account of the target computer must be trusted for delegation. For instructions on this configuration, see the posting on the community for [installing and uninstalling Windows applications](https://community.servicenow.com/people/russ.sarbora/blog/2011/09/30/2540).

### About this task

**Note:** See [WMI Providers](http://msdn.microsoft.com/en-us/library/aa394570(v=vs.85).aspx) for a list of Windows operating systems that provide this tool by default.

### Procedure

1.  Open the Control Panel.

2.  Go to **Add or Remove Programs**.

3.  Select **Add/Remove Windows Components**.

4.  Double-click **Management and Monitoring Tools**.

    This action opens a secondary window displaying additional selections.

5.  Select **WMI Windows Installer Provider** check box.

6.  Click **OK** to return to the Windows Components Wizard window.

7.  Click **Next**.

    You might be asked for the Windows installation CD to complete this process.


