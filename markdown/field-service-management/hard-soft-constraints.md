---
title: Objectives and constraints used with Schedule Optimization
description: Objectives and constraints are optimization features that determine how tasks are assigned to agents in Schedule Optimization.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 20
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

</th><th>

Example

</th></tr></thead><tbody><tr><td>

Maximize balance in number of hours agents work

</td><td>

Reward for even distribution of work hours \(i.e., tasks, travel\) between agents.

</td><td>

Shift “A” is assigned to tech A, and Shift “B” is assigned to tech B. Tasks “X”, “Y”, and “Z” have durations of 1 hour, 2 hours, and 3 hours, respectively. Travel between the shift start location, task locations, and the shift end location takes 1 hour for each segment.**Result:** When the objective applies, the assignment prioritizes an even distribution of total work hours \(tasks plus travel\) across agents. Assigning tasks “X” and “Y” to Shift “A” \(3 hours on tasks + 3 hours on travel\) and task “Z” to Shift “B” \(3 hours on tasks + 2 hours on travel\) achieves a more balanced split than other assignments.

</td></tr><tr><td>

Maximize balance in number of tasks agents work

</td><td>

Reward for even distribution of tasks between agents.

</td><td>

Shift “A” is assigned to tech A, and Shift “B” is assigned to tech B. Tasks “X” and “Y” each require one hour to complete.**Result:** When the objective applies, the assignment prioritizes giving one task to each shift so both agents have an equal workload.

</td></tr><tr><td>

Maximize consecutive collocated task assignments

</td><td>

Reward for each pair of collocated tasks that are assigned consecutively to the same agent.

</td><td>

Shift “A” is scheduled from 9:00 AM to 5:00 PM. Tasks “X” and “Y” are located at the same site, and task “Z” is at a different location.**Result:** Applying the objective prioritizes scheduling tasks “X” and “Y” back-to-back on Shift “A” to reduce unnecessary travel and earn the consecutive collocation reward.

</td></tr><tr><td>

Maximize efficient assignments

</td><td>

Incentive to assign tasks to agents based on efficiency, with rewards for quicker completion and penalties for slower completion compared to planned durations.

**Note:** The Field Service Agent Efficiency \(com.snc.fsm\_agent\_efficiency\) plugin must be installed to use this feature.

</td><td>

Shift “A” is assigned to an agent who completes task “X” in 45 minutes and task “Y” in 90 minutes. Shift “B” is assigned to an agent who completes both tasks in 60 minutes. The planned duration of both tasks is 60 minutes.**Result:** Applying the objective prioritizes assigning task “X” to Shift “A” and task “Y” to Shift “B” because these assignments reduce overall completion time compared to planned durations.

</td></tr><tr><td>

Maximize higher priority task assignments

</td><td>

Reward for every high-priority task that is assigned. The reward is higher for tasks with higher priorities.

</td><td>

Shift “A” is 5 hours long. Tasks “X,” “Y,” and “Z” each require 2 hours, and travel time between tasks is 15 minutes. Task “X” has high priority, task “Y” has medium priority, and task “Z” has low priority.

 **Result:** Applying the objective prioritizes assigning tasks “X” and “Y” to shift “A” because they have higher priorities. Don’t assign task “Z” because there isn’t enough time remaining in the shift.

</td></tr><tr><td>

Maximize higher value task assignments

</td><td>

Reward for the value of tasks that are assigned.

</td><td>

Shift “A” is 5 hours long. Task “X” requires 4 hours and has an optimization value of 10. Tasks “Y” and “Z” each require 2 hours and have optimization values of 5 and 4.**Result:** Applying the objective to maximize total optimization value prioritizes assigning task “X” to Shift “A” because it yields the highest total value, even though fewer tasks are completed.

</td></tr><tr><td>

Maximize preferred agent assignments

</td><td>

Reward for each task that is assigned to a preferred agent.

</td><td>

Shift “A” is assigned to an agent who is a high-preference match for task “X” and a low-preference match for task “Y.” Shift “B” is assigned to an agent who is a high-preference match for task “Y.”**Result:** Applying the objective prioritizes assigning task “X” to Shift “A” and task “Y” to Shift “B” to achieve the highest total reward from preference values.

</td></tr><tr><td>

Maximize task assignments

</td><td>

Reward for every task that is assigned.

</td><td>

Shift “A” is 5 hours long. Task “X” requires 2 hours, task “Y” requires 2 hours, and task “Z” requires 4 hours.**Result:** Applying the objective to maximize the number of scheduled tasks prioritizes assigning tasks “X” and “Y” to Shift “A” because they fit within the available time. Task “Z” isn’t assigned because there isn’t enough time remaining in the shift.

</td></tr><tr><td>

Maximize tasks in earlier shifts

</td><td>

Reward for each task that is assigned to an earlier shift. The reward is higher for shifts that start earlier in the optimization horizon.

</td><td>

Shift "A" runs from 9:00 AM to 2:00 PM, and Shift "B" runs from 2:00 PM to 6:00 PM. Tasks "X" and "Y" each require two hours.**Result:** Applying the objective prioritizes assigning both tasks to Shift A because it starts earlier in the optimization horizon and yields a higher reward.

</td></tr><tr><td>

Maximize work hours

</td><td>

Reward for every hour of work that is assigned

</td><td>

Shift “A” is 6 hours long. Task “X” requires 5 hours, and tasks “Y” and “Z” each require 2 hours.**Result:** When the objective applies, the assignment prioritizes maximizing time spent on tasks \(excluding travel\). Assigning task “X” to Shift “A” results in 5 hours of task work, which is greater than alternatives such as assigning tasks “Y” and “Z” \(4 hours total\).

</td></tr><tr><td>

Minimize work hours \(agent level\)

</td><td>

Penalty for each hour of work assigned. The penalty is higher for agents with higher Work Penalty Per Hour values.

</td><td>

Shift “A” is assigned to an agent with a work penalty of 1 per hour, and shift “B” is assigned to an agent with a work penalty of 3 per hour. Tasks “X” and “Y” each require 2 hours.**Result:** Assigning the objective prioritizes assigning tasks “X” and “Y” to shift “A” because the agent has a lower work penalty per hour.

</td></tr><tr><td>

Minimize higher priority task start times

</td><td>

Penalty for each hour that a task starts later than its earliest window start. The penalty is higher for tasks with higher priorities.

</td><td>

Task “X” has high priority and task “Y” has medium priority. Both have an earliest start time of 9:00 AM.**Result:** Applying the objective prioritizes assigning task “X” before task “Y” because “X” has a higher priority. Scheduling tasks later than their earliest start time incurs penalties, with higher penalties for higher-priority tasks. For example, if both tasks start at 10:00 AM, task “X” incurs a larger penalty than task “Y.”

</td></tr><tr><td>

Minimize number of shifts with tasks

</td><td>

Penalty for every shift that is assigned one or more tasks.

</td><td>

Shift “A” and Shift “B” are each 8 hours long. Tasks “X” and “Y” each require 2 hours.**Result:** Applying the objective prioritizes assigning both tasks “X” and “Y” to the same shift \(either “A” or “B”\) instead of splitting them across shifts. This approach reduces the total number of active shifts.

</td></tr><tr><td>

Minimize overtime

</td><td>

Penalty for every hour of overtime.

</td><td>

Shift “A” is scheduled from 9:00 AM to 5:00 PM, and Shift “B” is scheduled from 1:00 PM to 9:00 PM. Task “X” has a duration of 2 hours and must start between 3:30 PM and 7:00 PM.**Result:** Applying the objective prioritizes assigning task “X” to Shift “B” because it avoids any overtime penalty. Assigning task “X” to Shift “A” would result in a half-hour of overtime, as the task would run from 4:30 PM to 6:30 PM.

</td></tr><tr><td>

Minimize overtime \(agent level\)

</td><td>

Penalty for each hour of overtime work. The penalty is higher for agents with higher overtime penalty per-hour values.

</td><td>

Shift “A” is assigned to an agent with an overtime penalty of 1 per hour, and shift “B” is assigned to an agent with an overtime penalty of 3 per hour. Task “X” requires 2 hours and can only be completed as overtime.

 **Result:** Applying the objective prioritizes assigning task “X” to shift “A” because the agent’s overtime penalty is lower.

</td></tr><tr><td>

Maximize SLA compliance buffers

</td><td>

Reward for each hour that a task finishes earlier than its window end. The reward is smaller for tasks with longer SLA windows.

</td><td>

Shift “A” is scheduled from 9:00 AM to 5:00 PM. Tasks “X” and “Y” each have a 1-hour duration and SLA due times of 12:00 PM and 5:00 PM.**Result:** Applying the objective prioritizes finishing tasks before their SLA due times, with smaller rewards for tasks that have longer SLA windows. Scheduling task “X” to finish at 10:00 AM earns a larger reward than scheduling task “Y” at the same time because task “X” has a shorter SLA window.

</td></tr><tr><td>

Minimize SLA violation \(fixed\)

</td><td>

Penalty for each task that finishes later than its SLA due date.

</td><td>

Shift “A” is scheduled from 9:00 AM to 5:00 PM. Tasks “X”, “Y”, and “Z” each have a 2-hour duration and SLA due times of 8:00 AM, 1:00 PM, and 2:00 PM. Assume zero travel time between locations.**Result:** When the objective applies, the assignment prioritizes scheduling tasks before their SLA due times. Tasks “Y” and “Z” can be scheduled to finish at 11:00 AM and 1:00 PM, meeting their SLAs and incurring no penalties. Task “X” can’t meet its SLA because its due time \(8:00 AM\) is before Shift “A” begins \(9:00 AM\), so it incurs a penalty regardless of when it’s scheduled.

</td></tr><tr><td>

Minimize SLA violation \(hourly\)

</td><td>

Penalty for each hour that a task finishes later than in its SLA due date.

</td><td>

Shift “A” is scheduled from 9:00 AM to 5:00 PM. Tasks “X”, “Y”, and “Z” each have a 2-hour duration and SLA due times of 8:00 AM, 1:00 PM, and 2:00 PM. Assume zero travel time between locations.**Result:** When the objective applies, the assignment minimizes the total number of hours tasks exceed their SLA due times. Scheduling tasks “X,” “Y,” and “Z” to finish at 11:00 AM \(3-hour violation\), 1:00 PM \(0-hour violation\), and 3:00 PM \(1-hour violation\) results in a total SLA violation of 4 hours, which is the minimum possible when assigning all tasks. Any other task order would lead to more total hours of SLA violation.

</td></tr><tr><td>

Minimize task start times

</td><td>

Penalty for each hour that a task starts later than its earliest window start.

</td><td>

Shift “A” is scheduled from 9:00 AM to 5:00 PM. Tasks “X” and “Y” each have a 1-hour duration and earliest start times of 9:00 AM and 11:00 AM.**Result:** Applying the objective prioritizes scheduling task “X” as close to 9:00 AM as possible and task “Y” as close to 11:00 AM as possible to reduce total penalties.

</td></tr><tr><td>

Minimize task time penalties \(fixed\)

</td><td>

Penalty for each task that finishes later than its penalty time.

</td><td>

Shift “A” is scheduled from 9:00 AM to 5:00 PM. Tasks “X,” “Y,” and “Z” each have a 1-hour duration and penalty times of 8:00 AM, 1:00 PM, and 2:00 PM, respectively. Travel between the shift start location, task locations, and shift end location takes 1 hour.**Result:** Applying the objective penalizes tasks that finish after their penalty times. Tasks “Y” and “Z” can be scheduled to finish at 11:00 AM and 1:00 PM, meeting their penalty times and avoiding penalties. Task “X” incurs a penalty regardless of when it’s scheduled because its penalty time occurs before Shift “A” begins.

</td></tr><tr><td>

Minimize task time penalties \(hourly\)

</td><td>

Penalty for each hour that a task finishes later than its penalty time.

</td><td>

Shift “A” is scheduled from 9:00 AM to 5:00 PM. Tasks “X,” “Y,” and “Z” each have a 1-hour duration and penalty times of 8:00 AM, 1:00 PM, and 2:00 PM, respectively. Travel between the shift start location, task locations, and shift end location takes 1 hour.**Result:** Applying the objective prioritizes scheduling tasks “X,” “Y,” and “Z” to finish at 11:00 AM \(3-hour violation\), 1:00 PM \(0-hour violation\), and 3:00 PM \(1-hour violation\), respectively. This sequence results in a total penalty of 4 hours, which is the minimum possible when assigning all tasks. Any other task order would lead to more total hours of time penalties.

</td></tr><tr><td>

Minimize travel time

</td><td>

Penalty for every hour of travel.

</td><td>

Shift “A” is 5 hours long and starts and ends at the same location. Task “X” is 10 minutes away, and task “Y” is 30 minutes away. Both tasks are 3 hours long, so there’s only enough time to schedule one of them.**Result:** Applying the objective prioritizes assigning task “X” to Shift “A” because the round trip takes 20 minutes compared to 60 minutes for task “Y.”

</td></tr><tr><td>

Minimize travel time \(agent level\)

</td><td>

Penalty for each hour of travel. The penalty is higher for agents with higher Travel Penalty Per Hour values.

</td><td>

Shift “A” is assigned to an agent with a travel penalty of 1 per hour, and shift “B” is assigned to an agent with a travel penalty of 3 per hour. Task “X” is 1 hour away from the shift start location, and task “Y” is 30 minutes away. Both shifts are 5 hours long, and each task is 3 hours long, so there’s only enough time for each shift to complete one task.

 **Result:** Applying the objective prioritizes assigning shift “A” to task “X” and shift “B” to task “Y” because this pairing minimizes the total weighted travel penalty across all assignments.

</td></tr><tr><td>

Minimize over-skilled agent assignments

</td><td>

Penalty for skill level deviation between agents with a higher skill level than their assigned tasks.

</td><td>

Shift “A” is assigned to an agent with skill level 5. Task “X” requires skill level 5, and task “Y” requires skill level 2.**Result:** Applying the objective prioritizes assigning task “X” to Shift “A” because the skill levels match. Assigning task “Y” incurs a penalty because the agent’s skill level exceeds the requirement. If Shift “A” only has space for one task, task “X” is more likely to be scheduled than task “Y.”

</td></tr><tr><td>

Minimize under-skilled agent assignments

</td><td>

Penalty for skill level deviation between agents with a lower skill level than their assigned tasks.

</td><td>

Shift “A” is assigned to an agent with skill level 2. Task “X” requires an optional skill level 2, and task “Y” requires an optional skill level 5.**Result:** Applying the objective prioritizes assigning task “X” to Shift “A” because the skill levels match. Assigning task “Y” incurs a penalty because the agent’s skill level is lower than required. In general, task “X” is more likely to be scheduled on Shift “A” than task “Y.”

</td></tr></tbody>
</table><table id="table_yvh_ffd_kbc"><thead><tr><th>

Objective

</th><th>

Description

</th><th>

Example

</th></tr></thead><tbody><tr><td>

Maximize existing assignments

</td><td>

Reward for every agent/task assignment that remains in the schedule.

</td><td>

Shift “A” is currently assigned task “X” from 9:00 AM to 10:00 AM, and Shift “B” currently has no assignments but is 5 minutes closer to task “X”.**Result:** Applying the objective prioritizes keeping Shift “A” assigned to task “X” rather than reassigning it to Shift “B” to achieve slightly less travel time.

</td></tr><tr><td>

Minimize delayed tasks \(fixed\)

</td><td>

Penalty for every task that starts after it was originally scheduled.

</td><td>

Task “X” was originally scheduled to start at 10:00 AM. Task “X” has a delay penalty cost of 10.**Result:** When the objective applies, the assignment penalizes rescheduling task “X” to any time later than 10:00 AM. The penalty is the same whether the task moves to 10:01 AM or 1:00 PM and is based on the task’s delay penalty cost field. No penalty applies if the task is scheduled earlier than 10:00 AM.

</td></tr><tr><td>

Minimize delayed tasks \(hourly\)

</td><td>

Penalty for every hour that tasks start later than originally scheduled.

</td><td>

Task “X” was originally scheduled to start at 10:00 AM. Task “X” has a delay penalty cost of 10.**Result:** When the objective applies, the assignment penalizes task “X” based on how many hours it’s delayed. For example, rescheduling task “X” to 10:01 AM incurs a small penalty, while moving it to 1:00 PM incurs a larger penalty. The penalty is calculated using the task’s delay penalty cost field. No penalty applies if the task is scheduled earlier than 10:00 AM.

</td></tr><tr><td>

Minimize unassigned tasks

</td><td>

Penalty for every task that is removed from the schedule.

</td><td>

Shift “A” and Shift “B” are each 5 hours long. Tasks “X” and “Y” were included in the original schedule, and task “Z” wasn’t scheduled. All tasks require 3 hours.**Result:** Applying the objective prioritizes keeping tasks “X” and “Y” assigned, even if they move to different shifts, rather than unassigning them to make room for task “Z.”

</td></tr></tbody>
</table>## Constraints

Constraints are required and tasks aren't assigned unless the assignment group meets the constraint. Policies created in Schedule Optimization can be assigned to the following constraints.

<table id="table_mbs_bjl_3rb"><thead><tr><th>

Constraint

</th><th>

Description

</th><th>

Example

</th></tr></thead><tbody><tr><td>

Block excluded agents from assignment

</td><td>

Tasks with excluded agents can’t be assigned to those agents.

</td><td>

Shift “A” is assigned to an agent who is excluded from task “Y” but not from task “X.”**Result:** Applying the constraint allows task “X” to be assigned to Shift “A” while preventing task “Y” from being assigned because the agent is listed as excluded for that task. When this constraint is inactive, both tasks can be assigned to Shift “A.”

</td></tr><tr><td>

Enable access hours

</td><td>

Task time windows are restricted based on their access hours.**Note:** The Field Service \(com.snc.fsm\_access\_hours\) Access Hours plugin must be installed to use this feature.

</td><td>

Shift “A” is scheduled from 9:00 AM to 5:00 PM. Task “X” has a 1-hour duration and access hours from 9:00 AM to 11:00 AM and from 3:00 PM to 5:00 PM.**Result:** Applying the constraint allows task “X” to be scheduled only within its access windows. When the constraint is active, task “X” can only be scheduled between 9:00–11:00 AM or 3:00–5:00 PM. When the constraint is inactive, task “X” can be scheduled at any time between 9:00 AM and 5:00 PM.

</td></tr><tr><td>

Enable agent travel radius

</td><td>

Agents can only be assigned tasks that are within the travel radius of their home location.

</td><td>

Shift “A” starts at a defined location. Tasks “X”, “Y”, and “Z” are 10 miles, 20 miles, and 60 miles from that point. The constraint is active and the agent for Shift “A” has a 50-mile travel radius limit.**Result:** Shift “A” includes tasks “X” and “Y” and excludes task “Z”. When the constraint doesn’t apply, Shift “A” includes all three tasks.

</td></tr><tr><td>

Enable assignments only with preferred/secondary agents

</td><td>

Tasks with preferred/secondary agents can only be assigned to those agents.

</td><td>

Shift “A” is assigned to an agent. Task “X” has no preferred agents, task “Y” has preferred agents including that of Shift “A,” and task “Z” has preferred agents that don’t include the agent of Shift “A.”**Result:** Applying the constraint allows each task to be assigned only to its preferred or secondary agents when defined. Shift “A” can be assigned to task “X” because it has no preferred agents and to task “Y” because the shift belongs to a preferred agent. Task “Z” can’t be assigned to Shift “A” because it doesn’t belong to a preferred agent. When this constraint is inactive, all tasks can be assigned to Shift “A.”

</td></tr><tr><td>

Enable excluded agent restrictions

</td><td>

Tasks with excluded agents can’t be assigned to those agents.

</td><td>

Task “X” includes agents marked as excluded.

 **Result:** Applying this constraint prevents assigning Task “X” to any excluded agent.

</td></tr><tr><td>

Enable flexible breaks

</td><td>

Task assignments consider flexible breaks and can move them within their allowable windows for efficient scheduling.**Note:** The Shift Scheduling for Field Service \(com.snc.sn\_fsm\_shift\_schdl\) plugin must be installed and Workforce Optimization for Field Service must be activated to use the flexible breaks feature. For more information, see [Activate Workforce Optimization for Field Service](../task/activate-wfo-fsm.md).

</td><td>

Shift “A” is scheduled from 9:00 AM to 5:00 PM and includes a required 1-hour break that can be taken anytime between 11:00 AM and 2:00 PM. When the constraint is active, the break must occur within this allowable window.**Result:** Shift “A” honors the flexible break within the specified time range. When the constraint doesn’t apply, the break is ignored and may not be scheduled.

</td></tr><tr><td>

Enable mandatory parts

</td><td>

Tasks can only be assigned agents who have a sufficient inventory of parts.

</td><td>

An agent has 3 parts. Task “X” requires 3 optional parts, task “Y” requires 1 mandatory part, and task “Z” requires 3 mandatory parts.**Result:**Task “X” can be assigned to the agent because it requires no mandatory parts. Only one of tasks “Y” or “Z” can be assigned because the agent has enough parts for only one. Assigning both tasks would require 4 mandatory parts, which exceeds the available inventory. When the constraint doesn’t apply, all tasks can be assigned to the agent.

</td></tr><tr><td>

Enable mandatory skills

</td><td>

Tasks can only be assigned to agents with necessary skills.

</td><td>

Shift “A” is assigned to an agent with skill level 2. Task “X” requires skill level 2, and task “Y” requires skill level 4. When the constraint is active, assignments must meet or exceed the required skill level. Higher skill levels represent greater expertise \(level 4 is more advanced than level 2\).**Result:** Shift “A” includes task “X” because the agent meets the required skill level. Task “Y” can’t be assigned because the agent’s skill level is insufficient. When the constraint doesn’t apply, both tasks can be assigned to Shift “A”.

</td></tr><tr><td>

Enable overtime

</td><td>

Agents can work overtime.

</td><td>

Shift “A” is scheduled from 9:00 AM to 5:00 PM. Task “X” has a duration of 2 hours and must be completed between 4:00 PM and 10:00 PM. The task location is 15 minutes away from the shift end location.**Result:** When the constraint applies, the agent working Shift “A” can work up to 3 hours of overtime. Task “X” can be scheduled from 4:00 PM to 6:00 PM, extending one hour beyond regular shift hours. An additional 15 minutes is used for travel, so the shift effectively ends at 6:15 PM. When the constraint doesn’t apply, task “X” can’t be assigned to Shift “A”.

</td></tr><tr><td>

Enable travel outside work hours

</td><td>

Agents can travel outside work hours.

</td><td>

Shift “A” is scheduled from 9:00 AM to 5:00 PM. Task “X” is 1 hour away from the shift start location and is scheduled to begin at 9:00 AM.**Result:** When the constraint applies, the agent can travel before the start of Shift “A” to reach task “X” on time. When the constraint doesn’t apply, travel must occur during the shift or overtime hours.

</td></tr><tr><td>

Enable task dependencies

</td><td>

Tasks can only be assigned when their dependencies are met.

</td><td>

Shift “A” is scheduled from 9:00 AM to 5:00 PM. Task “Y” depends on the completion of task “X,” and each task has a 1-hour duration.**Result:** When the **Enable Task Dependencies** constraint applies, task “Y” can only be scheduled after task “X” is completed. When the constraint doesn’t apply, task dependencies may not be respected.

</td></tr><tr><td>

Enable travel time limits between locations

</td><td>

Agents must travel between locations within their travel time limit.

</td><td>

Shift “A” is assigned to an agent with a maximum travel time limit of 45 minutes between locations. Task “X” is 30 minutes away from the shift location, and task “Y” is 60 minutes away from both Task “X” and the shift location.**Result:** When the constraint applies, each segment of a route must meet the travel time limit. The route from Shift “A” start to Task “X” and back to the shift end is feasible because all travel segments are within the 45-minute limit. However, the route from Shift “A” start to Task “X” to Task “Y” and then to the shift end is infeasible because the segments between Task “X” and Task “Y” and between Task “Y” and the shift end each take 60 minutes, exceeding the limit. When the constraint doesn’t apply, both routes are feasible.

</td></tr><tr><td>

Enable agent-dependent task durations

</td><td>

The estimated duration for completing a task is determined by considering the primary skills required for the task and agent efficiency.**Note:** The Field Service Agent Efficiency \(com.snc.fsm\_agent\_efficiency\) plugin must be installed to use this feature.

</td><td>

Shift “A” and Shift “B” are assigned to different agents who complete task “X” in 45 and 90 minutes. Shift “C” is assigned to an agent who has no agent-dependent task duration. The planned duration of task “X” is 60 minutes.**Result:** When the constraint applies, task durations adjust based on the assigned agent. Task “X” takes 45 minutes when assigned to Shift “A” and 90 minutes when assigned to Shift “B.” When assigned to Shift “C,” task “X” takes 60 minutes \(the planned duration\) because there’s no agent-dependent adjustment. When the constraint doesn’t apply, all three shifts require 60 minutes to complete the task.

**Note:** This constraint works with the **Maximize Efficient Assignments** objective to reward faster completions.

</td></tr></tbody>
</table>**Parent Topic:**[Schedule Optimization components](schedule-optimization-components.md)

