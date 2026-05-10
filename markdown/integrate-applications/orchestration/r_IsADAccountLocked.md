---
title: Is AD Account Locked activity
description: The Is AD Account Locked activity determines whether an Active Directory user account is locked.
locale: en-US
release: australia
product: Orchestration
classification: orchestration
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Active Directory activity pack, Orchestration activity packs, Classic Orchestration, Workflow Data Fabric]
---

# Is AD Account Locked activity

The Is AD Account Locked activity determines whether an Active Directory user account is locked.

An account may be locked automatically if a user enters an incorrect password more times than allowed by the Active Directory security policy. You can unlock an account using the [Unlock AD User Account](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/orchestration/c_OrchActiveDirectoryActivities.md) activity.

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
|output|The query result.|

## Conditions

|Condition|Description|
|---------|-----------|
|Locked|The AD account is locked.|
|Unlocked|The AD account is unlocked.|
|Failure|An error occurred while processing the query. Additional details may be available in the workflow log.|

**Parent Topic:**[Active Directory activity pack](../concept/c_OrchActiveDirectoryActivities.md)

