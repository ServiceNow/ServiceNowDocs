---
title: Restart Windows Server activity
description: The Restart Windows Server activity stops and then restarts a Windows server using Powershell.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/integrate-applications/orchestration/r\_RestartWindowsServerActivity.html
release: zurich
product: Orchestration
classification: orchestration
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [PowerShell activity pack, Orchestration activity packs, Classic Orchestration, Workflow Data Fabric]
---

# Restart Windows Server activity

The Restart Windows Server activity stops and then restarts a Windows server using Powershell.

**Note:** This activity replaces a Powershell activity by the same name available in releases prior to Geneva. If you have a workflow created in a previous version that uses the deprecated activity, your workflow will continue to work normally after upgrading to Geneva. However, all new workflows must use the custom version of this activity. This activity was built with the [Powershell activity template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/orchestration/t_CreateAPowershellActivity.md), which gives workflow administrators the ability to store input and output variables in the [databus](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/orchestration/c_OrchestrationDatabus.md).

## Input variables

|Variable|Description|
|--------|-----------|
|Hostname|Hostname or IP address of the Windows server to restart.|

## Output variables

|Variable|Description|
|--------|-----------|
|result|Either **success** or **failure**.|
|errorMessage|The **executionResult.errorMessages** from the [Activity designer parsing sources](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/orchestration/t_CreateAParsingRule.md). If this variable is not null, the operation has failed.|

## Conditions

|Condition|Description|
|---------|-----------|
|Success|The activity succeeded in restarting the Windows server.|
|Failure|The activity failed to restart the Windows server.|

**Parent Topic:**[PowerShell activity pack](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/orchestration/c_OrchestrPwrshellActivityPack.md)

