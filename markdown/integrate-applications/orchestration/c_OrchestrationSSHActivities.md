---
title: SSH activities
description: SSH activities allow workflows to perform operations on Linux and Unix computers.The Run Command activity runs a command \(including shell scripts\) on a Linux or UNIX computer.The Run SCP activity uses Secure Copy Protocol \(SCP\) to copy a file from one computer to another, including the directory in which the file resides.
locale: en-US
release: zurich
product: Orchestration
classification: orchestration
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Deprecated Orchestration activities, Activate Orchestration, Classic Orchestration, Workflow Data Fabric]
---

# SSH activities

SSH activities allow workflows to perform operations on Linux and Unix computers.

Your ServiceNow instance must have access to a MID Server configured to use SSH to run these Orchestration activities.

**Parent Topic:**[Deprecated Orchestration activities](../reference/r_OrchestrationBasicActivities.md)

## Run Command activity

The Run Command activity runs a command \(including shell scripts\) on a Linux or UNIX computer.

**Important:** The Run Command activity is deprecated in this release. If you have a workflow created in a previous version that uses this activity, your workflow will continue to work normally after upgrading to Helsinki. However, to use this functionality in a new workflow, you must create a custom activity using the [SSH activity template](../../orchestration-activity-designer/task/t_CreateAnSSHActivity.md#) in the ServiceNow® activity designer.

### Input variables

|Field|Description|
|-----|-----------|
|Long running|Select this check box to disable the SSH connection timeout if you think the command will take longer to run than the default 60 seconds. Orchestration periodically checks the running process to determine its status until it is finished.|
|Hostname|Hostname or IP address of destination server for SSH activity.|
|Directory|Name of the working directory.|
|Command|The command to run from this activity.|
|Sudo|Select this check box to use [sudo](http://www.sudo.ws/sudo/sudo.html) to run the command on the host machine.|
|Sensor script|The script to run using the results of the probe. The output from the probe is contained in a variable called *output*. Any error from the probe is contained in a variable called *error*.|

## Run SCP activity

The Run SCP activity uses Secure Copy Protocol \(SCP\) to copy a file from one computer to another, including the directory in which the file resides.

**Note:** This activity is deprecated in the Geneva release and is not available for use in new workflows. If you have a workflow created in a previous version that uses this activity, your workflow will continue to work normally after upgrading. The custom [Secure Copy activity](https://www.servicenow.com/docs/access?context=r_SecureCopyActivity&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US) replaces the Run SCP activity in the Geneva release.

### Input variables

|Field|Description|
|-----|-----------|
|From Host|Hostname or IP address of the source computer.|
|From File|Absolute path to the file to copy. This value can be a directory.|
|To Host|Hostname or IP address of the target computer.|
|To File|Path to the target file. This path can be absolute or relative to the logged in user's home directory. The specified directory must already exist on the target computer.|
|Copy Directory|Check box to copy a directory defined in the **From File** variable and all files contained in that directory.|

