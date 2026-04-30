---
title: Assigning preferred agents to work on tasks
description: Preferred agents are agents who are most familiar with the context of tasks they've been assigned and are preferred by customers. For example, they could be agents who work on-site at a customer premise or are associated with the customer contracts or entitlements.
locale: en-US
release: yokohama
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Assigning work order tasks to agents using dynamic scheduling, Scheduling and dispatching work order tasks to agents, Using Field Service Management, Field Service Management]
---

# Assigning preferred agents to work on tasks

Preferred agents are agents who are most familiar with the context of tasks they've been assigned and are preferred by customers. For example, they could be agents who work on-site at a customer premise or are associated with the customer contracts or entitlements.

You can assign preferred agents to tasks using dynamic scheduling when you assign tasks using any of the following methods:

-   Auto-assign using agent recommendation
-   Book an appointment using Appointment Booking

Here are a few scenarios on how tasks can get assigned to preferred agents.

**Note:** The preferred technicians must be added to the respective customer accounts and the preferred technician matching criteria must be added to the dynamic scheduling configuration.

In this example, let's define the roles as follows:

<table id="table_umy_3zj_2jb"><thead><tr><th>

Role

</th><th>

Name

</th></tr></thead><tbody><tr><td>

Customer of Acme Corporation

</td><td>

George Warren

</td></tr><tr><td>

Dispatcher

</td><td>

Lisa Ray

</td></tr><tr><td>

-   Mona Lisa
-   Alex Ray
-   Lynda Caraway

</td><td>

Preferred technicians for Acme Corporation account

</td></tr></tbody>
</table>**Scenario 1: Auto-assign using agent recommendation**

This example shows how tasks that are high priority can get assigned to preferred agents.

**Note:** Lisa Ray is logged in as a dispatcher.

1.  Navigate to **Field Service** &gt; **Dispatching** &gt; **Dispatcher Workspace**
2.  Locate a task for Acme Corporation that must be assigned to a preferred technician. Let's say Mona Lisa is the preferred technician available to work on this task.
3.  Drag the task and drop it to Mona Lisa's schedule in the calendar. The task has now been scheduled.
4.  Now, a high-priority task from Acme Corporation enters the task queue. This task must be assigned to the same preferred agent Mona Lisa and has to be scheduled at the same time when the previous task was scheduled.
5.  Drag the task to Mona Lisa's schedule in the calendar. This task automatically takes the time slot of the previously scheduled task and that task moves to the next available schedule that is available for Mona Lisa.

**Scenario 2: Book an appointment using Appointment Booking**

This example shows how when a customer books an appointment, it’s automatically assigned to the preferred agent.

**Note:** George Warren is logged in as a customer of Acme Corporation.

1.  Navigate to the customer service portal.
2.  Select a service that requires an appointment.
3.  Select the desired time slot and select **Select**.
4.  Select **Submit**.

    Navigate to **Field Service** &gt; **Dispatching** &gt; **Dispatcher Workspace** and see that the task has been assigned to the preferred agent Mona Lisa.


For more information on adding a preferred agent to a work order task see, [Assign preferred agents to tasks](../task/assign-preferred-agents-tasks.md).

**Parent Topic:**[Assigning work order tasks to agents using dynamic scheduling](using-dynamic-scheduling.md)

