---
title: Create an execution plan
description: Administrators and catalog administrators can create and manage execution plans and the associated variable tasks.You can add variables of a catalog item to a task to specify information about the requested catalog item.
locale: en-US
release: zurich
product: Service Catalog
classification: service-catalog
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Execution Plans, Service Catalog request fulfillment, Service Catalog configuration, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create an execution plan

Administrators and catalog administrators can create and manage execution plans and the associated variable tasks.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Administration** &gt; **Execution Plans**.

2.  Click **New**.

    ![](../image/CreateAnExecutionPlan.png "New execution plan")

3.  Enter a Name and Short description for the execution plan.

4.  Specify [delivery information](../concept/c_ExecutionPlanTasks.md#) in the Total delivery time and On Calendar fields.

5.  Click **Submit**.


**Parent Topic:**[Execution Plans](../concept/c_ExecutionPlans.md)

## Add catalog item variables to a task

You can add variables of a catalog item to a task to specify information about the requested catalog item.

### Before you begin

Role required: admin

### About this task

For example, when a user requests a laptop, the fulfillment group can need to know what screen size and how much memory to order.

Each catalog item can contain one or more variables for gathering information from the user who requests the item. Assuming that the relevant catalog items have been associated to the execution plan, you can associate these variables to the specific created tasks that need the information.

### Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Administration** &gt; **Execution Plans**.

2.  Open an execution plan.

3.  In the Execution Plan Tasks related list, open a task.

    Ensure that the form shows the Plan view. If not, right-click the header bar and select **View** &gt; **Plan**.

4.  Go to the Available Variables related list and click **Edit**.

5.  Use the slushbucket to select the variables that are appropriate for the task.

    Consider all the types of catalog items that could use this execution plan, and select all the variables that can be assigned to them.

6.  Click **Save** to associate these variables to the execution plan task, making them accessible.


