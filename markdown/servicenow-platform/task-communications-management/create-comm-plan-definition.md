---
title: Define a communication plan
description: Define a communication plan for a task record to specify communication task and contact definitions. When specified conditions for the plan definition are met, the communication plan and its associated records are automatically attached to the task record, eliminating manual effort.
locale: en-US
release: xanadu
product: Task Communications Management
classification: task-communications-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Working with Task Communications Management, Task Communications Management, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Define a communication plan

Define a communication plan for a task record to specify communication task and contact definitions. When specified conditions for the plan definition are met, the communication plan and its associated records are automatically attached to the task record, eliminating manual effort.

## Before you begin

Role required: sn\_comm\_management.comm\_plan\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **Task Communications Management** &gt; **Plan Definitions**, and click **New**.

2.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Unique name for the communication plan.|
    |Table|Table that the plan is attached to when the conditions are met.|
    |Type|Type of communication plan such as Technical, Internal, External, Customer.|
    |Order|Order in which the communication plans must be associated to the table.|
    |Condition based|Option to define whether the plan is attached to a table based on the conditions. For example, if you want to attach a communication plan to an incident of priority = 2, you can mention the condition in the **Condition** field.|
    |Active|Option to define whether the plan definition is active.|
    |Description|Detailed description of the plan definition.|
    |Condition|Condition under which a communication plan gets attached to a table.|

3.  Click **Submit**.

    The communication plan is submitted. The following related lists appear in the communication plan definition:

    -   Communication Task Definitions
    -   Communication Contact Definitions

## What to do next

Define a communication task for the plan.

-   **[Define a communication task](create-comm-task-definition.md)**  
Define a communication task for a communication plan. When a plan gets attached to a table, the tasks related to the plan need to be executed to resolve the issue. You can associate multiple tasks with a communication plan.
-   **[Define a communication channel](create-comm-channel-definition.md)**  
Define a communication channel for each communication task to determine which mode of communication to use for the task when a plan is attached to a table.
-   **[Define a communication contact](create-comm-contact-definition.md)**  
Define the recipients of a particular plan to determine the target audience involved in each communication task and the responsibilities the recipients are expected to handle. A notification for a task is sent to all individuals specified for that task.

**Parent Topic:**[Working with Task Communications Management](../concept/working-with-tcm.md)

