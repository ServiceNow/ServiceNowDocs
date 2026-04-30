---
title: Reset Linux User Password activity
description: The Reset Linux User Password activity resets the password for a given user on a Linux computer.
locale: en-US
release: xanadu
product: Orchestration
classification: orchestration
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [SSH activity pack, Orchestration activity packs, Classic Orchestration, Creating integrations with applications]
---

# Reset Linux User Password activity

The Reset Linux User Password activity resets the password for a given user on a Linux computer.

This activity requires that the user executing the command be able to run the **chpasswd** command and, if expiring the password immediately, to run **chage** with [MID Server privileged commands](https://www.servicenow.com/docs/access?context=c_PrivilegedCommandsForMIDServer&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

This activity replaces an SSH activity by the same name available in releases prior to Istanbul. If you have a workflow created in a previous version that uses the deprecated activity, your workflow will continue to work normally after upgrading to Istanbul. However, all new workflows must use the custom version of this activity. This activity was built with the [SSH activity template](../../orchestration-activity-designer/task/t_CreateAnSSHActivity.md#), which gives workflow administrators the ability to store input and output variables in the [databus](../../orchestration-activity-designer/concept/c_OrchestrationDatabus.md#).

## Input variables

|Variable|Description|
|--------|-----------|
|hostname|IP address of the target Linux machine.|
|user|Name of the user whose password is being reset.|
|password|New password set for this user. The password is a workflow variable that is encrypted either as a **password2** field or by calling the encryption method of a *Packages.com.glide.util.Encrypter* object.|
|force\_change|Indicates if this password is temporary and to force the named user to change the password at login.|

## Output variables

|Variable|Description|
|--------|-----------|
|return\_code|Indicates whether or not the user password reset action was successful.|
|error\_message|Describes any error that occurred during password reset. If no error occurred, this value is null.|

## Conditions

|Variable|Description|
|--------|-----------|
|Success|Activity successfully changed specified user's password|
|Failure|Activity failed to change specified user's password.|

**Parent Topic:**[SSH activity pack](../concept/c_OrchestrationSSHCustomActivities.md)

