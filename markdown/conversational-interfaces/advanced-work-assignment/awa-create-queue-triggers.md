---
title: Create and manage queue triggers
description: Create and manage queue triggers to set off multiple actions during customer wait times for a particular queue.
locale: en-US
release: zurich
product: Advanced Work Assignment
classification: advanced-work-assignment
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure, Advanced Work Assignment, Manage people and work, Conversational Interfaces]
---

# Create and manage queue triggers

Create and manage queue triggers to set off multiple actions during customer wait times for a particular queue.

## Before you begin

Role required: awa\_admin or admin

## Procedure

1.  Navigate to the queue settings through one of the following navigation paths:

    -   **All** &gt; **Advanced Work Assignment** &gt; **Home**.

        In the Essential settings section, select **Set up queues**.

    -   **All** &gt; **Advanced Work Assignment** &gt; **Queues**.
2.  Select the queue.

3.  Select the Queue Triggers related list.

    -   To create a queue trigger, select **New**.
    -   To change a queue trigger, select the queue trigger record to be updated.
4.  On the form, fill in the fields.

<table id="table_qkk_w4p_1vb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Queue

</td><td>

Work items that belong to a service channel.

</td></tr><tr><td>

Message

</td><td>

Message that users see because the **Trigger Time** has elapsed.

 If the **Trigger Type** field value is **Max Wait**, this field becomes read-only and displays the value entered in the Queue form's **Max wait time message** field. When the **Max wait time message** appears to users, they’re prompted to select a Virtual Agent topic and if they select a topic, they don’t return to the live agent's queue.

</td></tr><tr><td>

Trigger Type

</td><td>

Type of configurable trigger: **Wait** or **Max Wait**. The **Wait** trigger defines the actions that happen when users are waiting in the queue and the **Max Wait Time** hasn't been met. The **Max Wait** trigger defines the actions that happen when users are waiting in the queue and the **Max Wait Time** is met.

</td></tr><tr><td>

Trigger Time

</td><td>

Time \(days or hours, minutes, seconds\) allotted for the **Trigger Type**.If the **Trigger Type** field value is **Max Wait**, this field becomes read-only and displays the value entered in the Queue form's **Max Wait Time** field.

</td></tr><tr><td>

Flow

</td><td>

Name of the flow or subflow.**Note:** Workflow Studio subflows must have a string input parameter named `conversation_id` for AWA queue triggers to detect the appropriate subflow. Ensure that the subflow you want to use has a string input parameter named `conversation_id` through the **Execution** tab in Workflow Studio.

</td></tr><tr><td>

Virtual Agent topic

</td><td>

Name of the existing Virtual Agent topic that appears to the users when the max wait time is met.

</td></tr></tbody>
</table>5.  Select **Submit** for a new queue or **Update** to change the queue.

    The queue triggers are added to or updated in the Queue Triggers related list.


**Parent Topic:**[Configuring Advanced Work Assignment](installing-awa.md)

