---
title: Disable AD User Account activity
description: The Disable AD User Account activity disables a Windows Active Directory user account, making it inactive.
locale: en-US
release: yokohama
product: Orchestration
classification: orchestration
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Active Directory activity pack, Orchestration activity packs, Classic Orchestration, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Disable AD User Account activity

The Disable AD User Account activity disables a Windows Active Directory user account, making it inactive.

To access this activity in the Workflow Editor, select the **Custom** tab, and then navigate to **Custom Activities** &gt; **Active Directory**.

**Note:** This activity replaces an AD activity by the same name available in prior releases. If you have a workflow that uses the deprecated activity, your workflow will continue to work normally after upgrading to Instanbul. However, all new workflows must use the custom version of this activity, which was built with the [PowerShell activity designer](../../orchestration-activity-designer/concept/c_PowershellActivityDesigner.md).

## Input variables

|Variable|Description|
|--------|-----------|
|DomainController|IP address of the domain controller machine.|
|User|The sAMAccountName of the Active Directory user account.|

## Output variables

|Variable|Description|
|--------|-----------|
|result|Either **success** or **failure**.|
|errorMessage|The **executionResult.errorMessages** from the [Activity designer parsing sources](../../orchestration-activity-designer/task/t_CreateAParsingRule.md#).|

## Conditions

|Condition|Description|
|---------|-----------|
|Success|AD user account was successfully disabled.|
|Failure|An error occurred while attempting to disable the account. Additional details may be available in the workflow log.|

**Parent Topic:**[Active Directory activity pack](../concept/c_OrchActiveDirectoryActivities.md)

