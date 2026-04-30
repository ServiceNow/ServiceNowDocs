---
title: Configuring Field Service Agent Efficiency
description: Configure Field Service Agent Efficiency to define Agent Efficiency criteria and values for agents and more accurately calculate the work duration for a work order task or combination of tasks.
locale: en-US
release: zurich
product: Workforce Optimization for Field Service
classification: workforce-optimization-for-field-service
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Set up workforce, Configure, Field Service Management]
---

# Configuring Field Service Agent Efficiency

Configure Field Service Agent Efficiency to define Agent Efficiency criteria and values for agents and more accurately calculate the work duration for a work order task or combination of tasks.

Field Service agent efficiency is the pace at which an agent can complete a type of work order task. The values for Agent Efficiency for efficiency criteria range from 0 to 2, where a value of 1 signifies that the agent completes these tasks within the standard time frame. A value above 1 suggests the agent finishes these tasks faster than the average, while a value below 1 indicates the agent takes longer than the typical time needed to complete the task. Field Service Agent Efficiency for an agent can be defined for multiple criteria.

Field Service Agent Efficiency uses the following formula to calculate the estimated work duration based on the planned work duration and agent efficiency:

`Estimated work duration = Planned work duration/Agent Efficiency`

**Goal**: Ensure the best-suited agent is assigned the task by considering the efficiency of the agents for these particular tasks and accurately estimate the work duration.

Assume there are two qualified work order tasks that are ready to be dispatched, one for laptop repair and another for MRI machine installation.

**Agent Efficiency table**:

|Technician|Agent Efficiency criterion|Agent Efficiency|Planned work duration|Estimated work duration|
|----------|--------------------------|----------------|---------------------|-----------------------|
|Anthony Roy|MRI machine installation|0.5|60 minutes|120 minutes|
|Cindy Lisa|Laptop repair|0.6|60 minutes|100 minutes|
|Cindy Lisa|MRI machine installation|0.8|60 minutes|75 minutes|
|Alisa Chinoy|Laptop repair|0.8|60 minutes|75 minutes|
|Ray William|Laptop repair|1.2|60 minutes|50 minutes|
|Alex Ray|Laptop repair|1|60 minutes|60 minutes|

**Explanation**: For the laptop repair work order task, the best-suited technician is Ray William because this technician completes this type of task 10 minutes earlier than the planned work duration.

For the MRI machine installation task, the best-suited technician is Cindy Lisa.

## Configuration overview

The steps for configuring Field Service Agent Efficiency are:

1.  [Activate Field Service Agent Efficiency](../task/activate-field-service-agent-efficiency.md)

    Activating the Field Service Agent Efficiency \(com.snc.fsm\_agent\_efficiency\) plugin requires the admin role.

2.  [Create or modify Agent Efficiency criteria](../task/create-or-modify-agent-efficiency-criteria.md)
3.  [Assign an Agent Efficiency value to agents](../task/assign-efficiency-value-to-agents.md)
4.  \(Optional\) [Create or modify an Agent Efficiency determination rule](../task/create-or-modify-agent-efficiency-determination-rule.md)
5.  \(Optional\) Configure Field Service Agent Efficiency with Dynamic Scheduling to auto-assign tasks to the agents. For more information, see [Configuring Dynamic Scheduling](Configure-dynamic-scheduling.md).
6.  \(Optional\) Configure Field Service Agent Efficiency with Intelligent Task Recommendations to recommend the best suited task for an agent based on the efficiency. For more information, see [Configuring Intelligent Task Recommendations](administer-task-recommendations.md).
7.  \(Optional\) Configure Field Service Agent Efficiency with Schedule Optimization to identify, schedule, and assign tasks to the most appropriate agent based on the agent efficiency and an accurate estimated duration. For more information see, [Configuring Schedule Optimization](schedule-optimization-engine.md).

**Related topics**  


[Field Service Agent Efficiency](agent-efficiency.md)

