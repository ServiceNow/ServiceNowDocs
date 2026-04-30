---
title: Restart Windows Server activity
description: The Restart Windows Server activity stops and then restarts a Windows server using Powershell.
locale: en-US
release: xanadu
product: Orchestration
classification: orchestration
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [PowerShell activity pack, Orchestration activity packs, Classic Orchestration, Creating integrations with applications]
---

# Restart Windows Server activity

The Restart Windows Server activity stops and then restarts a Windows server using Powershell.

**Note:** This activity replaces a Powershell activity by the same name available in releases prior to Geneva. If you have a workflow created in a previous version that uses the deprecated activity, your workflow will continue to work normally after upgrading to Geneva. However, all new workflows must use the custom version of this activity. This activity was built with the [Powershell activity template](../../orchestration-activity-designer/task/t_CreateAPowershellActivity.md#), which gives workflow administrators the ability to store input and output variables in the [databus](../../orchestration-activity-designer/concept/c_OrchestrationDatabus.md#).

## Input variables

|Variable|Description|
|--------|-----------|
|Hostname|Hostname or IP address of the Windows server to restart.|

## Output variables

|Variable|Description|
|--------|-----------|
|result|Either **success** or **failure**.|
|errorMessage|The **executionResult.errorMessages** from the [Activity designer parsing sources](../../orchestration-activity-designer/task/t_CreateAParsingRule.md#). If this variable is not null, the operation has failed.|

## Conditions

|Condition|Description|
|---------|-----------|
|Success|The activity succeeded in restarting the Windows server.|
|Failure|The activity failed to restart the Windows server.|

**Parent Topic:**[PowerShell activity pack](../concept/c_OrchestrPwrshellActivityPack.md)

