---
title: SSH activity pack
description: Orchestration provides an activity pack of SSH activities that were customized using the ServiceNow activity designer.
locale: en-US
release: xanadu
product: Orchestration
classification: orchestration
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Orchestration activity packs, Classic Orchestration, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# SSH activity pack

Orchestration provides an activity pack of SSH activities that were customized using the ServiceNow activity designer.

These activities perform the same functions as SSH activities by the same name from previous releases and replace those activities for all new workflows. The custom SSH activities were built with the [Create an SSH activity](../../orchestration-activity-designer/task/t_CreateAnSSHActivity.md#), which gives workflow administrators the ability to store input and output variables in the [databus](../../orchestration-activity-designer/concept/c_OrchestrationDatabus.md#).

**Note:** Existing workflows from earlier versions that were created with legacy SSH activities continue to function normally after an upgrade to Geneva. However, all new workflows must use these custom SSH activities.

To use the SSH custom activities, you must [request activation](../task/t_ActivateAnActivityPack.md) of the Orchestration - SSH plugin.

-   **[Secure Copy activity](../reference/r_SecureCopyActivity.md)**  
The Secure Copy activity copies a file from one host to another, without storing the copied file on the MID Server.
-   **[Files Compare activity](../reference/r_FilesCompareActivity.md)**  
The Files Compare activity compares two files on a Linux or UNIX computer.
-   **[File Read activity](../reference/r_FileReadActivity.md)**  
The File Read activity reads a file on a Linux or UNIX computer.
-   **[File Write activity](../reference/r_FileWriteActivity.md)**  
The File Write activity writes a file on a Linux or UNIX computer.
-   **[File Copy activity](../reference/r_FileCopyActivity.md)**  
The custom File Copy activity copies a file on a Linux or UNIX computer.
-   **[File Replace String activity](../reference/r_FileReplaceStringActivity.md)**  
The File Replace String activity finds and replaces a string in a file on a Linux or UNIX computer.
-   **[Reset Linux User Password activity](../reference/r_ResetLinuxUserPasswordActivity.md)**  
The Reset Linux User Password activity resets the password for a given user on a Linux computer.

**Parent Topic:**[Orchestration activity packs](c_OrchestrationActivityPacks.md)

