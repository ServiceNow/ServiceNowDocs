---
title: Creating execution plan tasks
description: An execution plan contains one or more task templates. Each task template defines work that can be completed by a specific fulfillment group.Each execution plan contains one or more task templates that define actions that must be taken to fulfill a request.Administrators and catalog administrators can define conditions under which a particular execution plan task runs, or is skipped, when the relevant item is requested.Administrators can use a condition script in addition to or instead of any condition to determine whether a task runs.
locale: en-US
release: yokohama
product: Service Catalog
classification: service-catalog
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Execution Plans, Service Catalog request fulfillment, Configuring Service Catalog, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Creating execution plan tasks

An execution plan contains one or more task templates. Each task template defines work that can be completed by a specific fulfillment group.

Execution plans are associated with catalog items. When the relevant catalog item is requested, these task templates are used to generate tasks. That is, tasks to be performed as part of the request fulfillment process for that requested item. Each generated task within that requested item is assigned a catalog task number.

## Example

The execution plan for an executive desktop computer catalog item could define the following task templates in the execution plan:

-   Obtain managerial approval
-   Order hardware
-   Install standard corporate applications
-   Deliver computer to requester

When this catalog item is ordered, the following request, requested item, and tasks are then created:

Request REQ0002 -- 1 PC

Requested Item ITEM0004 -- 1 X executive desktop

-   Catalog Task0001 -- Obtain managerial approval
-   Catalog Task0002 -- Order hardware
-   Catalog Task0003 -- Install standard corporate application
-   Catalog Task0004 -- Deliver computer to requester

**Parent Topic:**[Execution Plans](c_ExecutionPlans.md)

## Define task templates

Each execution plan contains one or more task templates that define actions that must be taken to fulfill a request.

### Before you begin

Role required: admin

### About this task

After creating the execution plan, define these task templates.

When the relevant catalog item is ordered, request tasks are generated for that requested item, based on this information.

To define an execution plan task template:

### Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Policy** &gt; **Execution Plans**.

2.  Open an execution plan.

3.  In the **Execution Plan Tasks** related list, click **New**.

4.  Fill in the fields on the Execution Plan Task form \(see table\).

5.  Click **Submit**.

    ![](../image/DefineATaskTemplate.png "Cat DP Task1")

<table id="table_cfh_xns_jp"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the task. This name becomes the created task name.

</td></tr><tr><td>

Fulfillment group

</td><td>

The group that performs the task. Whenever a user requests a catalog item associated with this execution plan, the task is automatically assigned to the fulfillment group. Leave blank if automatic assignment to a group is not required.

</td></tr><tr><td>

Assigned to

</td><td>

The individual who performs the task. Leave blank if automatic assignment to a user is not required.

</td></tr><tr><td>

SLA

</td><td>

The service level agreement that applies to catalog items associated with this execution plan. **Note:** This field is normally left blank, as the functionality was superseded by the service level management functionality.

</td></tr><tr><td>

Delivery plan

</td><td>

The parent execution plan for this task.

</td></tr><tr><td>

Order

</td><td>

A number representing the task sequence in the execution plan. It is good practice to "leave gaps" between order numbers \(for example, 100, 200, 300\). That way you can insert new tasks without changing the order number of existing tasks. \(If the order for several execution plan tasks is the same, each of these tasks starts at the same time.\)

</td></tr><tr><td>

Delivery time

</td><td>

Amount of time the task is expected to take. This value becomes a component of the overall time to complete the execution plan.

</td></tr><tr><td>

Condition

</td><td>

Condition under which the task is performed \(if the condition is not met, the task is skipped\).

</td></tr><tr><td>

Short description

</td><td>

Brief description of the task activity. This information populates the created task short description field.

</td></tr><tr><td>

Instructions

</td><td>

Details of the activities to be performed for the task. This information populates the created task description field.

</td></tr><tr><td>

Work notes

</td><td>

A journal field for entering comments about the task template. Note: this information is separate from the created task work notes field.

</td></tr></tbody>
</table>
## Conditions to run execution plan tasks

Administrators and catalog administrators can define conditions under which a particular execution plan task runs, or is skipped, when the relevant item is requested.

For example, an execution plan can contain the following tasks:

1.  Order hardware
2.  Receive hardware
3.  Configure hardware
4.  Deliver hardware

If the hardware requested is already on-site, it does not need to be ordered. The first task in the list can be skipped.

**Note:** Skipped task records are still created, but are marked as skipped, and are not processed within the execution plan.

### Conditional Tasks

To make an execution plan task conditional, defining the conditions under which the task runs.

1.  Navigate to **Service Catalog** &gt; **Execution Plans**.
2.  Open an execution plan, and then open a task within that plan.
3.  Use the **condition** field to select the condition under which the task runs.

If no conditions are set, the task runs every time a user orders an item associated with this execution plan.

Here is an example of conditional task for an IT lab based in Atlanta:

![](../image/ApplyConditionToTasks.png "Applying Conditions to Execution Plan Tasks")

In this example, the **Deliver to IT Labs** step does not run if the request itself is in Atlanta. There is no need to deliver something to the IT lab if it is already there.

## Condition scripts to run tasks

Administrators can use a condition script in addition to or instead of any condition to determine whether a task runs.

**Note:** If you are using both a condition \(via the condition field\) and a condition script, both must be true before the task runs.

To use a script, you must configure the Execution Plan Task form to add the "Condition script" field. If the script returns true, the task runs. If the script returns false, the task does not run.

Ensure that you add the variable used in the script to the execution plan task.

![Use Condition Scripts](../image/UseConditionScriptsToRunTasks.png "Use Condition Scripts")

