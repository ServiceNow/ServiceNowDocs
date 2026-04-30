---
title: Create a universal task
description: Create a universal task for a request and assign it to the employee or create multiple tasks for a request by using Universal Task.
locale: en-US
release: xanadu
product: Universal Task
classification: universal-task
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Using Universal Task, Universal Task, Employee Service Management]
---

# Create a universal task

Create a universal task for a request and assign it to the employee or create multiple tasks for a request by using Universal Task.

## Before you begin

Role required: Configurable by your service

## About this task

Universal Task agents, as configured in [Define the agent criteria for Universal Task](ut-config-extn-point-agent.md) can create a new universal task using the UI action available on the ticket page.

**Note:** To control the access for creating a task, configure the visibility of the UI action for creating Universal Task. For more information, see [Create UI actions for your service with Universal Task](config-uiactions-for-ut.md).

When a universal task is created, it is auto-assigned to the employee as configured in [Configure Universal Task for your service](config-ut-for-service.md). The employee receives a notification and can view or update the task from the ServiceNow Employee Service Center. If the employee accesses the task from the ServiceNow AI Platform, they can only add a comment and add people to the watch list.

## Procedure

1.  Open the ticket that you want to create a universal task for.

2.  Click the UI action for creating a universal task.

    **Note:** The name of the UI action is configurable and can vary. For more information, see [Create UI actions for your service with Universal Task](config-uiactions-for-ut.md)

3.  On the form, fill in the fields.

    See [Universal Task form](../reference/universal-task-form.md) for more information.

4.  Select one of the following.

    |Option|Description|
    |------|-----------|
    |**__Ready for work__**|Task is created. The state of the task changes to Work in Progress, and the employee is notified about the task.|
    |**__Submit__**|Task is created. The state of the task remains New, and no notification is sent to the employee.|


## Result

Employee experience: A new task is created for your request. You can view and complete the task in the **To-Do** tab of the Employee Service Center. You can also view and complete the task in the task tab of the associated request, if configured in standard ticket configuration. You receive notifications if the task is canceled, closed, completed, or if a comment is added to the task. Notifications are sent to the stakeholders when changes are made to the task.

Agent experience: You can now view or edit the task. You can also add more tasks to the same request.

**Parent Topic:**[Using Universal Task](../concept/use-universal-task.md)

