---
title: Execution plan tasks
description: An execution plan contains one or more execution plan tasks, such as for obtaining approval. Execution plan tasks are assigned to a fulfillment group.Approval tasks are specific types of tasks within execution plans.Fulfillment groups perform the tasks related to fulfilling an order.When managing execution plans, catalog administrators can specify the delivery information to provide an estimated date of delivery based on the execution plan.If a task is skipped, the request fulfillment process moves on to the next task.
locale: en-US
release: zurich
product: Service Catalog
classification: service-catalog
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Execution Plans, Service Catalog request fulfillment, Service Catalog configuration, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Execution plan tasks

An execution plan contains one or more execution plan tasks, such as for obtaining approval. Execution plan tasks are assigned to a fulfillment group.

Each task represents work to be completed by a specific group as part of the overall request fulfillment process.

Administrators create templates for tasks as part of defining an execution plan. The catalog tasks themselves are then created when the relevant item is requested, based on these task templates.

**Parent Topic:**[Execution Plans](c_ExecutionPlans.md)

## Set up an execution plan approval task

Approval tasks are specific types of tasks within execution plans.

### Before you begin

Role required: admin

### About this task

If an approval task is rejected, the execution plan can roll back to a previous task, but the approval record does not roll back.

To set up an approval task including a rollback action:

### Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Execution Plans**.

2.  Select an execution plan.

3.  From the Execution Plan Tasks related list, select **New Approval** to create the approval task.

4.  Fill in the fields for that approval task.

    ![](../image/ExecutionPlanApprovalTasks1.png "Upon Reject")

5.  Use the Upon reject field to define the action to take if the task is rejected:

    -   Cancel all future Tasks: \[default\] cancels all future tasks in the execution plan and also cancels the parent request item.
    -   Go to a previous Task: displays the Rejection goto field where you can select which task this execution plan rolls back to.
6.  **Save** the task, then scroll down to the Approved By list and select one or more approvers for the tasks.

    You can also use an Approval script to select approvers.

7.  Select **Update** to add the task to the execution plan.

    This example shows how the process works in practice, using a request to order a Blackberry phone.

    First, the request is ordered:

    ![Screenshot for Rollback1](../image/Rollback1.png "Rollback 1")

    Next, complete the first two steps, which leads to the approval task.

    ![Screenshot for Rollback2](../image/Rollback2.png "Rollback 2")

    Reject the request to roll back the execution plan to a previous task, and reset any intermediate tasks to pending:

    ![Screenshot for Rollback3](../image/Rollback3.png "Rollback 3")

    After a plan has been rolled back, ServiceNow adds to the rolled-back task a note indicating that it was rolled back and why.

    **Note:** Rolling back reverts all intermediate tasks within the execution plan. Other plans within the same request are not rolled back, however.


## Set up a fulfillment group

Fulfillment groups perform the tasks related to fulfilling an order.

### Before you begin

Role required: admin

### About this task

This group setting can include approving an order based on characteristics such as content and price, or any direct action required to complete the order. For example, loading software or installing hardware. Any existing user group \(in **User Administration** &gt; **Groups**\) can be assigned fulfillment tasks.

To create a group specifically for order fulfillment:

### Procedure

1.  Navigate to **Service Catalog** &gt; **Catalog Policy** &gt; **Fulfillment Groups**.

2.  Click **New**.

3.  Fill in the Group form as described under creating groups.

    These groups have the type catalog and are assigned the catalog and itil roles, but are otherwise normal groups.


## Delivery information for tasks

When managing execution plans, catalog administrators can specify the delivery information to provide an estimated date of delivery based on the execution plan.

Use the **Total delivery time** field to specify an estimated delivery time for each task in your execution plan. This estimate is calculated based on the combined total of times for the [tasks](c_CreatingExecutionPlanTasks.md#) in that execution plan.

By default, time estimates do not use a "working days" calendar system, but are based on simple elapsed time. For example, for a 5-day execution plan, if you submit the request on a Friday, the delivery date is Wednesday of the following week. This estimate means five elapsed days later, even if your organization does not work on weekends.

Setting the calendar to Monday through Friday \(9-5\) defines each day as being eight hours long, but the task delivery time day is 24 hours. If you create a task that takes one day \(24 hours\), the plan calculates the task as needing three work days \(which are eight hours each\) for the total delivery time. Similarly, if a task takes two days \(48 hours\), the plan calculates eight days of total delivery time. This total breaks down as six work days of eight hours each and, because six days are longer than the five-day work week, two weekend days. When assigning delivery times, keep this calculation process in mind.

Use the On Calendar field to specify a calendar system to apply to the execution plan, to help estimate more accurate delivery times.

If using this calendar system for estimated delivery time, ensure that estimates are expressed in working hours and days. For example, a task which is supposed to take one day on a 9-5 calendar is assumed to take 24 working hours. This process takes three working days.

**Note:** This calendar system is used to help provide delivery estimates only, and is not linked to any SLAs you have set on execution tasks.

## Skipped tasks

If a task is skipped, the request fulfillment process moves on to the next task.

If the last task in an execution plan is skipped, the process is finished and the appropriate request item is closed as complete. Skipped tasks have their state set to **Closed Skipped** and display as gray boxes on a requested items list.

