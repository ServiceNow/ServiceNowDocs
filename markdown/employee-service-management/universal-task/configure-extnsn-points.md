---
title: Configure the extension points for Universal Task
description: Provide the implementation for childTaskCancelled, childTaskCompleted, childTasksClosed of the scripted extension point to execute the custom logic of the service, when a universal task is canceled, completed, or closed.
locale: en-US
release: yokohama
product: Universal Task
classification: universal-task
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring your service for Universal Task, Setting up and configuring Universal Task, Universal Task, Employee Service Management]
---

# Configure the extension points for Universal Task

Provide the implementation for childTaskCancelled, childTaskCompleted, childTasksClosed of the scripted extension point to execute the custom logic of the service, when a universal task is canceled, completed, or closed.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Extension Points** &gt; **Scripted Extension Points**.

2.  Search for `sn_uni_task.UniversalTaskCloseEvents`.

3.  To create your service-specific extension point script, click **Create Implementations** in the related list.

    For more information, see [Using extension points to extend application functionality](https://www.servicenow.com/docs/access?context=extension-points&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US).

4.  Click **Update**.


**Parent Topic:**[Configuring your service for Universal Task](../concept/config-service-for-ut.md)

**Previous topic:**[Configure the roles to view employee forms](ut-config-empform-view-roles.md)

**Next topic:**[Display the universal tasks for a request in Now Mobile](ut-mobile-config-tasktab.md)

