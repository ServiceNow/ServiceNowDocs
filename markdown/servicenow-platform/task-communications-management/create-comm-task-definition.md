---
title: Define a communication task
description: Define a communication task for a communication plan. When a plan gets attached to a table, the tasks related to the plan need to be executed to resolve the issue. You can associate multiple tasks with a communication plan.
locale: en-US
release: yokohama
product: Task Communications Management
classification: task-communications-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Define a communication plan, Working with Task Communications Management, Task Communications Management, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Define a communication task

Define a communication task for a communication plan. When a plan gets attached to a table, the tasks related to the plan need to be executed to resolve the issue. You can associate multiple tasks with a communication plan.

## Before you begin

Role required: sn\_comm\_management.comm\_plan\_admin or admin

You have defined a communication plan.

## Procedure

1.  Navigate to **All** &gt; **Task Communications Management** &gt; **Plan Definitions**.

2.  Click the communication plan for which you want to define a communication task.

3.  Click the Communication Task Definitions related list and then click **New**.

4.  On the form, fill in the fields.

<table id="table_ish_5tl_2db"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Communication plan definition

</td><td>

Unique name of the communication plan definition that you are defining the task for.

</td></tr><tr><td>

Name

</td><td>

Unique name for the communication task definition.

</td></tr><tr><td>

Type

</td><td>

Type of task, such as internal communication, that is applicable globally or to a particular table. **Note:** The value in the **Type** field helps you to filter a task by its type. The value also helps to generate a report of a particular task type or to create SLAs on any communication task.

</td></tr><tr><td>

Application

</td><td>

Application scope of the task definition. The task definition is available for all applications or for scoped applications.

</td></tr><tr><td>

Order

</td><td>

Order that the communication tasks appear in the plan. This field indicates which communication task to execute first.

</td></tr><tr><td>

Active

</td><td>

Option to define whether the task is active or not.

</td></tr><tr><td>

Description

</td><td>

Detailed description of the task definition.

</td></tr><tr><td>

Communication frequency

</td><td>

Frequency of the communication task execution. You can send the notification once or the notification can be repeated.

</td></tr><tr><td>

Duration

</td><td>

Time by which you want to send a notification. For example, if the communication frequency is **One time** and the **Duration** is 15 minutes, then the notification is sent only once in 15 minutes. If the communication frequency is **Recurring**, then the notification is sent every 15 minutes.

</td></tr></tbody>
</table>5.  Click **Update**.

    The communication task is defined for the communication plan.


## What to do next

Define communication channel for the task.

**Parent Topic:**[Define a communication plan](create-comm-plan-definition.md)

**Related topics**  


[Define a communication channel](create-comm-channel-definition.md)

[Define a communication contact](create-comm-contact-definition.md)

