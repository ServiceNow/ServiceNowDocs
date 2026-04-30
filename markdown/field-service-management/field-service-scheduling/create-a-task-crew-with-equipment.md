---
title: Assign equipment to a task crew
description: Assign equipment to an ad hoc task crew to ensure they have the necessary tools to complete the work order task.
locale: en-US
release: yokohama
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Scheduling and assigning equipment to tasks and crews, Scheduling and dispatching work order tasks to agents, Using Field Service Management, Field Service Management]
---

# Assign equipment to a task crew

Assign equipment to an ad hoc task crew to ensure they have the necessary tools to complete the work order task.

## Before you begin

Note the following requirements to assign the equipment:

-   The work order task must already have a task crew assigned. See [Create ad hoc crews in Dispatcher Workspace](create-adhoc-crews-disp-wrkspc.md) for more information.
-   The work order task must already have resource requirements. See [Add resource requirement for a work order task in Dispatcher Workspace](add-resource-requirement-disp-wrkspc.md) for more information.

Role required: wm\_admin, wm\_dispatcher

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Manager** &gt; **Work Order Tasks**.

2.  Select the work order task.

3.  In the **Task Assignees** tab, select **Add**.

4.  On the form, fill in the fields.

    |Fields|Description|
    |------|-----------|
    |Requirement|Name of the resource requirement that this assignment addresses.|
    |Resource Type|Should be set to **Equipment**.|
    |Equipment|The equipment instance to be assigned.|

5.  Select **Submit**.


## Result

On the task crew page, the equipment appears in the **Task Assignees** tab.

**Parent Topic:**[Scheduling and assigning equipment to tasks and crews](../concept/assign-equipment-to-wot.md)

**Related topics**  


[Assign equipment to a planned crew](add-equipment-to-a-planned-crew.md#)

[Assign an equipment instance to groups](assign-eq-instance-to-groups.md)

[Create a maintenance schedule for an equipment instance](create-maint-sched-for-eq-instance.md)

