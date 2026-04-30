---
title: Join Domain activity
description: The Join Domain activity joins a Windows computer to a domain.
locale: en-US
release: yokohama
product: Orchestration
classification: orchestration
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [PowerShell activity pack, Orchestration activity packs, Classic Orchestration, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Join Domain activity

The Join Domain activity joins a Windows computer to a domain.

If the computer is already a member of a domain, this activity completes without modifying the computer. Joining a domain requires a username and password. This user must have domain administration privileges or privileges to join a computer to the domain.

**Note:** This activity replaces a Powershell activity by the same name available in releases prior to Geneva. If you have a workflow created in a previous version that uses the deprecated activity, your workflow will continue to work normally after upgrading to Geneva. However, all new workflows must use the custom version of this activity. This activity was built with the [PowerShell activity designer](../../orchestration-activity-designer/concept/c_PowershellActivityDesigner.md), which gives workflow administrators the ability to store input and output variables in the [databus](../../orchestration-activity-designer/concept/c_OrchestrationDatabus.md#).

## Input variables

|Variables|Description|
|---------|-----------|
|Hostname|Hostname or IP address of the Windows server that is joining the domain.|
|Domain|Name of the domain to join.|
|Domain\_user|The name of a user who has domain administration privileges or privileges to join a computer to the domain.|
|Domain\_user\_password|The password for the user who has domain administration privileges or privileges to join a computer to the domain.|

## Output variables

|Variables|Description|
|---------|-----------|
|result|Either **success** or **failure**.|
|errorMessage|The **executionResult.errorMessages** from the [Activity designer parsing sources](../../orchestration-activity-designer/task/t_CreateAParsingRule.md#). If this variable is not null, the operation has failed.|

## Conditions

|Condition|Description|
|---------|-----------|
|Success|The activity succeeded in joining the computer to the domain.|
|Failure|The activity failed to join the computer to the domain.|

**Parent Topic:**[PowerShell activity pack](../concept/c_OrchestrPwrshellActivityPack.md)

