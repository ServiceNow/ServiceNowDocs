---
title: Schedule Optimization components
description: Components installed with Schedule Optimization include tables, roles, constraints, objectives, and properties.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Reference, Field Service Management]
---

# Schedule Optimization components

Components installed with Schedule Optimization include tables, roles, constraints, objectives, and properties.

## Tables

Field Service Schedule Optimization adds the tables listed in the following table.

<table id="table_gbn_dgk_21c"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Optimization Scope snc\_schedule\_optim\_optimization\_scope

</td><td>

Defines the qualifiers \(groups or territories\), tasks, and policies to be used during optimization.

</td></tr><tr><td>

Optimization Batch snc\_schedule\_optim\_batch

</td><td>

Defines the optimization schedule for one, or more scopes.

</td></tr><tr><td>

Optimization Feature snc\_schedule\_optim\_optimization\_constraints

</td><td>

Defines the objectives and constraints to be used in optimization policies.-   Objective = soft target, optimizer tries to build a schedule that honors these goals
-   Constraint = hard rule, optimizer must build a schedule that honors these restrictions

 **Note:** This table is read only

</td></tr><tr><td>

Policies snc\_schedule\_optim\_policy

</td><td>

Container record for objectives and constraints that are used for optimization.

</td></tr><tr><td>

Policy Configurations snc\_schedule\_optim\_policy\_configuration

</td><td>

Related list table used to add objectives and constraints to a policy and to associate weights with objectives.-   Optimizer prioritizes adhering to the objectives with the highest weight.
-   Lower weight objectives are considered but might have less impact on the schedule

</td></tr><tr><td>

Scheduling Attribute Configuration snc\_schedule\_optim\_sched\_attr\_config

</td><td>

Defines global and qualifier-level settings for intraday optimization, including policy and travel estimate providers.-   "If Global is set to false, groups or territories can be added to a configuration to override optimization settings for a particular qualifier.
-   If Global is set to true, the settings apply to all other groups that don’t have an override.
-   A Global record also includes additional settings that cannot be overwritten at the qualifier level, such as the intraday processing window and flow.
-   Determines the travel estimate vendor for batch optimization.

</td></tr><tr><td>

Group Scheduling Attributes snc\_schedule\_optim\_group\_m2m\_sched\_attr\_config

</td><td>

Links a group to a scheduling attribute configuration.

</td></tr><tr><td>

Territory Scheduling Attributes snc\_schedule\_optim\_territory\_m2m\_sched\_attr\_config

</td><td>

Links a territory to a scheduling attribute configuration.**Note:** This table is installed only if the FSM Territory plugin is active

</td></tr></tbody>
</table>## Roles

Field Service Schedule Optimization adds the following roles.

|Role|Description|
|----|-----------|
|schedule\_optimization\_user|User role for accessing the Schedule Optimization application. This role allows users to trigger on-demand schedule optimization executions.|
|schedule\_optimization\_planner|Planner role for the Schedule Optimization application. This role allows administrators to perform administration configurations for the Schedule Optimization application and perform schedule planning activities.|

-   **[Tables installed with FSM for Schedule Optimization](tables-installed-with-fsm-for-schedule-optimization.md)**  
The following tables are installed with the Field Service Management plugin, but are only used bySchedule Optimization.
-   **[Objectives and constraints used with Schedule Optimization](hard-soft-constraints.md)**  
Objectives and constraints are optimization features that determine how tasks are assigned to agents in Schedule Optimization.
-   **[Schedule Optimization properties](schedule-optimization-properties.md)**  
You can set parameters that control how optimization runs.
-   **[Schedule Optimization integration user access requirements](schedule-optimization-integration-user-access-requirements.md)**  
Describes the access requirements for the shared integration user account used by Schedule Optimization.

**Parent Topic:**[Field Service Management reference](../../planning-and-policy/reference/fsm-reference.md)

