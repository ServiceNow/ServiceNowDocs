---
title: Assign multi-day tasks to agents
description: Assign a work order task that requires multiple schedules or days to complete the job to a field service agent. This capability avoids having to create more than one task for the same job.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/field-service-management/field-service-scheduling/assign-multi-day-task.html
release: zurich
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Assigning multi-day tasks to agents, Scheduling and dispatching, Use, Field Service Management]
---

# Assign multi-day tasks to agents

Assign a work order task that requires multiple schedules or days to complete the job to a field service agent. This capability avoids having to create more than one task for the same job.

## Before you begin

If you are scheduling a task across multiple schedule entries or days, a work schedule must have been assigned to the agent. For more information, see [Create a work schedule for agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/field-service-management/field-service-manager-workforce/create-agent-work-schedule.md).

**Note:** If the agent schedule has not been defined and you are auto-assigning a task, the system uses the default schedule.

Role required: wm\_admin

## About this task

For information about how to assign a multi-day task to a crew, see [Assign work order tasks to crews](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/field-service-management/field-service-manager-workforce/assign-wot-crew-operations.md).

This procedure explains how you can assign a multi-day task to an agent using ServiceNow AI Platform. For information about how to assign a multi-day task using Dispatcher Workspace, see [Assign work order tasks to agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/field-service-management/field-service-scheduling/manage-work-order-tasks-dw.md).

## Procedure

1.  Navigate to **All** &gt; **Field Service Management** &gt; **Work Order** &gt; **Work Order Tasks**.

2.  Select the desired task for assignment.

3.  Select the **Assign across the schedule entries** check box if it is not already selected.

4.  Assign the task.

<table id="choicetable_jln_msm_dsb"><thead><tr><th align="left" id="d111155e139">

Option

</th><th align="left" id="d111155e142">

Description

</th></tr></thead><tbody><tr><td id="d111155e148">

**To assign a task manually**

</td><td>

1.  In the **Assigned to** field, select the agent available to work on the task.
2.  Click **Update**.


</td></tr><tr><td id="d111155e172">

**To auto-assign a task**

</td><td>

1.  Click **Auto Assign** to automatically assign the task to an available agent.

2.  In the Confirm Assignment dialog box, select **Confirm**.


</td></tr></tbody>
</table>    The system calculates the estimated end date of the task based on the schedule of the selected agent.


## Result

The task schedule spanning multiple schedule entries, days, or weeks is assigned to an agent.

