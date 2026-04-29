---
title: Create a learning task
description: Create learning tasks for agents to keep track of their learning activities.
locale: en-US
release: australia
product: Workforce Optimization for IT Service Management
classification: workforce-optimization-for-it-service-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Learning, Training your teams, Coaching, Workforce Optimization for ITSM, IT Service Management]
---

# Create a learning task

Create learning tasks for agents to keep track of their learning activities.

## Before you begin

Role required: sn\_wfo\_cfg\_itsm.manager

## About this task

Set learning task completion due dates to include or exclude weekends using the **exclude\_weekends\_on\_learning\_task\_due\_date** system property. For more information, see [Workforce Optimization for ITSM Reference](../reference/configurable-wfo-itsm-coaching-reference.md).

## Procedure

1.  Navigate to **All** &gt; **Workforce Optimization for ITSM** &gt; **Manager Workspace**.

2.  Click the coaching icon \(![Coaching icon](../image/coaching-icon-uib.png)\).

3.  Click the **Learning** tab.

4.  Click **Learning Tasks** and select **All Tasks**.

5.  Create a learning task.

    1.  Click **New**.
    2.  Fill in the following fields.

<table id="table_pr4_zgk_bpb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Assigned to

</td><td>

Name of the agent to whom you want to assign the learning task.

</td></tr><tr><td>

Learning library

</td><td>

The learning library that contains the course item for the learning task.

</td></tr><tr><td>

Course item

</td><td>

The course that needs to be completed by the agent.

</td></tr><tr><td>

Due date

</td><td>

Date when the agent must complete the course. Default is 5 days after the creation of the learning task. This value is calculated from the **Days to Complete** field for the course item. For learning tasks that are assigned or in progress, the due date field is highlighted as follows:-   Green—if the task is due after the current day.
-   Yellow—if the task is due on the current day.
-   Red—if the task was due before the current day.


</td></tr></tbody>
</table>6.  Click **Save**.


**Parent Topic:**[Learning in Workforce Optimization for ITSM](../concept/workforce-learning-configurable-wfo-itsm.md)

