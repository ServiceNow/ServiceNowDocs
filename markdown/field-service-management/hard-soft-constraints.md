---
title: Objectives and constraints used with Schedule Optimization
description: Objectives and constraints are optimization features that determine how tasks are assigned to agents in Schedule Optimization.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Schedule Optimization components, Reference, Field Service Management]
---

# Objectives and constraints used with Schedule Optimization

Objectives and constraints are optimization features that determine how tasks are assigned to agents in Schedule Optimization.

## Objectives

Objectives prioritize agent task assignments, and each objective is weighted. Schedule Optimization prioritizes higher-numbered weights. For default settings, apply a weight of 1, and for more important factors, such as maximizing high-priority task assignments, apply a weight of 2.

<table id="table_p1j_q3h_fyb"><thead><tr><th>

Objective

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Maximize balance in number of hours agents work

</td><td>

Reward for even distribution of work hours \(i.e., tasks, travel\) between agents.

</td></tr><tr><td>

Maximize balance in number of tasks agents work

</td><td>

Reward for even distribution of tasks between agents.

</td></tr><tr><td>

Maximize consecutive collocated task assignments

</td><td>

Reward for each pair of collocated tasks that are assigned consecutively to the same agent.

</td></tr><tr><td>

Maximize higher priority task assignments

</td><td>

Reward for every high-priority task that is assigned. The reward is higher for tasks with higher priorities.

</td></tr><tr><td>

Maximize higher value task assignments

</td><td>

Reward for the value of tasks that are assigned.

</td></tr><tr><td>

Maximize preferred agent assignments

</td><td>

Reward for each task that is assigned to a preferred agent.

</td></tr><tr><td>

Maximize SLA compliance buffers

</td><td>

Reward for each hour that a task finishes earlier than its window end. The reward is smaller for tasks with longer SLA windows.

</td></tr><tr><td>

Maximize task assignments

</td><td>

Reward for every task that is assigned.

</td></tr><tr><td>

Maximize tasks in earlier shifts

</td><td>

Reward for each task that is assigned to an earlier shift. The reward is higher for shifts that start earlier in the optimization horizon.

</td></tr><tr><td>

Maximize work hours

</td><td>

Reward for every hour of work that is assigned

</td></tr><tr><td>

Minimize higher priority task start times

</td><td>

Penalty for each hour that a task starts later than its earliest window start. The penalty is higher for tasks with higher priorities.

</td></tr><tr><td>

Minimize number of shifts with tasks

</td><td>

Penalty for every shift that is assigned one or more tasks.

</td></tr><tr><td>

Minimize over-skilled agent assignments

</td><td>

Penalty for skill level deviation between agents with a higher skill level than their assigned tasks.

</td></tr><tr><td>

Minimize overtime

</td><td>

Penalty for every hour of overtime.

</td></tr><tr><td>

Minimize SLA violation \(fixed\)

</td><td>

Penalty for each task that finishes later than its SLA due date.

</td></tr><tr><td>

Minimize SLA violation \(hourly\)

</td><td>

Penalty for each hour that a task finishes later than in its SLA due date.

</td></tr><tr><td>

Minimize task start times

</td><td>

Penalty for each hour that a task starts later than its earliest window start.

</td></tr><tr><td>

Minimize task time penalties \(fixed\)

</td><td>

Penalty for each task that finishes later than its penalty time.

</td></tr><tr><td>

Minimize task time penalties \(hourly\)

</td><td>

Penalty for each hour that a task finishes later than its penalty time.

</td></tr><tr><td>

Minimize travel time

</td><td>

Penalty for every hour of travel.

</td></tr><tr><td>

Minimize under-skilled agent assignments

</td><td>

Penalty for skill level deviation between agents with a lower skill level than their assigned tasks.

</td></tr><tr><td>

Maximize efficient assignments

</td><td>

Incentive to assign tasks to agents based on efficiency, with rewards for quicker completion and penalties for slower completion compared to planned durations.

**Note:** The Field Service Agent Efficiency \(com.snc.fsm\_agent\_efficiency\) plugin must be installed to use this feature.

</td></tr><tr><td>

Minimize travel time \(agent level\)

</td><td>

Penalty for each hour of travel. The penalty is higher for agents with higher Travel Penalty Per Hour values.

</td></tr><tr><td>

Minimize work hours \(agent level\)

</td><td>

Penalty for each hour of work assigned. The penalty is higher for agents with higher Work Penalty Per Hour values.

</td></tr><tr><td>

Minimize overtime \(agent level\)

</td><td>

Penalty for each hour of overtime work. The penalty is higher for agents with higher Overtime Penalty Per Hour values.

</td></tr></tbody>
</table>|Objective|Description|
|---------|-----------|
|Maximize existing assignments|Reward for every agent/task assignment that remains in the schedule.|
|Minimize delayed tasks \(fixed\)|Penalty for every task that starts after it was originally scheduled.|
|Minimize delayed tasks \(hourly\)|Penalty for every hour that tasks start later than originally scheduled.|
|Minimize unassigned tasks|Penalty for every task that is removed from the schedule.|

## Constraints

Constraints are required and tasks won't be assigned unless the assignment group meets the constraint. Policies created in Schedule Optimization can be assigned to the following constraints.

<table id="table_mbs_bjl_3rb"><thead><tr><th>

Constraint

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Block excluded agents from assignment

</td><td>

Tasks with excluded agents can’t be assigned to those agents.

</td></tr><tr><td>

Enable access hours

</td><td>

Task time windows are restricted based on their access hours.**Note:** The Field Service \(com.snc.fsm\_access\_hours\) Access Hours plugin must be installed to use this feature.

</td></tr><tr><td>

Enable agent travel radius

</td><td>

Agents can only be assigned tasks that are within the travel radius of their home location.

</td></tr><tr><td>

Enable assignments only with preferred/secondary agents

</td><td>

Tasks with preferred/secondary agents can only be assigned to those agents.

</td></tr><tr><td>

Enable excluded agent restrictions

</td><td>

Tasks with excluded agents can’t be assigned to those agents.

</td></tr><tr><td>

Enable flexible breaks

</td><td>

Agents can be assigned flexible breaks.**Note:** The Shift Scheduling for Field Service \(com.snc.sn\_fsm\_shift\_schdl\) plugin must be installed and Workforce Optimization for Field Service must be activated to use the flexible breaks feature. For more information, see [Activate Workforce Optimization for Field Service](../task/activate-wfo-fsm.md).

</td></tr><tr><td>

Enable mandatory parts

</td><td>

Tasks can only be assigned agents who have a sufficient inventory of parts.

</td></tr><tr><td>

Enable mandatory skills

</td><td>

Tasks can only be assigned to agents with necessary skills.

</td></tr><tr><td>

Enable overtime

</td><td>

Agents can work overtime.

</td></tr><tr><td>

Enable travel outside work hours

</td><td>

Agents can travel outside work hours.

</td></tr><tr><td>

Enable task dependencies

</td><td>

Tasks can only be assigned when their dependencies are met.

</td></tr><tr><td>

Enable travel time limits between locations

</td><td>

Agents must travel between locations within their travel time limit.

</td></tr><tr><td>

Enable agent dependent task durations

</td><td>

The estimated duration for completing a task is determined by considering the primary skills required for the task and agent efficiency.**Note:** The Field Service Agent Efficiency \(com.snc.fsm\_agent\_efficiency\) plugin must be installed to use this feature.

</td></tr></tbody>
</table>**Parent Topic:**[Schedule Optimization components](schedule-optimization-components.md)

