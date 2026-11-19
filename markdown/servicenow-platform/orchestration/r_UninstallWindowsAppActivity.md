---
title: Uninstall Windows App activity
description: The Uninstall Windows App activity uninstalls an application from a Windows target machine.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/servicenow-platform/orchestration/r\_UninstallWindowsAppActivity.html
release: zurich
product: Orchestration
classification: orchestration
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [PowerShell activity pack, Orchestration activity packs, Classic Orchestration, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Uninstall Windows App activity

The Uninstall Windows App activity uninstalls an application from a Windows target machine.

The only applications that can be uninstalled using this activity are those that were installed by a Windows Installer.

**Note:** This activity replaces a Powershell activity by the same name available in releases prior to Geneva. If you have a workflow created in a previous version that uses the deprecated activity, your workflow will continue to work normally after upgrading to Geneva. However, all new workflows must use the custom version of this activity. This activity was built with the [Powershell activity template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/orchestration/t_CreateAPowershellActivity.md), which gives workflow administrators the ability to store input and output variables in the [databus](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/orchestration/c_OrchestrationDatabus.md).

## Input variables

|Variable|Description|
|--------|-----------|
|hostname|Hostname or IP address of the Windows target machine on which to uninstall an application.|
|product|The name of the application to uninstall exactly as it appears in the Windows Add/Remove Programs list.|

## Output variables

|Variable|Description|
|--------|-----------|
|result|Either **success** or **failure**.|
|errorMessage|The **executionResult.errorMessages** from the [Activity designer parsing sources](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/orchestration/t_CreateAParsingRule.md). If this variable is not null, the operation has failed.|

## Conditions

|Condition|Description|
|---------|-----------|
|Success|The activity succeeded in unistalling the application from the Windows server.|
|Failure|The activity failed to uninstall the application from the Windows server.|

**Parent Topic:**[PowerShell activity pack](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/orchestration/c_OrchestrPwrshellActivityPack.md)

