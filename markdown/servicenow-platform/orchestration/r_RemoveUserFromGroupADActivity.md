---
title: Remove User from Group AD activity
description: The Remove User from Group activity removes a user from a group in Windows Active Directory.
locale: en-US
release: zurich
product: Orchestration
classification: orchestration
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Active Directory activity pack, Orchestration activity packs, Classic Orchestration, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Remove User from Group AD activity

The Remove User from Group activity removes a user from a group in Windows Active Directory.

To access this activity in the Workflow Editor, select the **Custom** tab, and then navigate to **Custom Activities** &gt; **Active Directory**.

## Input variables

|Variable|Description|
|--------|-----------|
|DomainController|IP address of the domain controller machine.|
|UserName|Name of the user to remove from the group.|
|GroupName|Name of the group from which this user is removed.|

## Output variables

|Variable|Description|
|--------|-----------|
|result|Either **success** or **failure**.|
|errorMessage|The **executionResult.errorMessages** from the [Activity designer parsing sources](../../orchestration-activity-designer/task/t_CreateAParsingRule.md#).|

## Conditions

|Condition|Description|
|---------|-----------|
|Success|User was successfully removed from the group.|
|Failure|An error occurred while attempting to remove the user from the group. Additional details may be available in the workflow log.|

**Parent Topic:**[Active Directory activity pack](../concept/c_OrchActiveDirectoryActivities.md)

