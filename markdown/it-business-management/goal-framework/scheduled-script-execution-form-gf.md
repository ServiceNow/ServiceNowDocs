---
title: Scheduled Script Execution form
description: Scheduled Jobs are automated pieces of work that can be performed at a specific time or on a recurring schedule.
locale: en-US
release: xanadu
product: Goal Framework
classification: goal-framework
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Reference, Goal Framework and Goal Framework for SPM, Strategic Portfolio Management]
---

# Scheduled Script Execution form

Scheduled Jobs are automated pieces of work that can be performed at a specific time or on a recurring schedule.

## Migrate Goal, Strategy, and Work item data to the Goal Framework and related Planning item tables

Use the **Migrate Goal, Strategy, and Work item data to the Goal Framework and related Planning item tables** job to migrate the existing goals data to the Goal Framework tables.

<table id="scheduled-job-to-migrate-goals-data-parameters-form"><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

migrateGoalData

</td><td>

-   Migrates all existing goal records from the Goal \[goal\] table to the Goal \[sn\_gf\_goal\] table. The sys\_id remains the same. The corresponding target records will be created in the Target \[sn\_gf\_goal\_target\] table.
-   Creates the existing relationship between the goal and work items \(Project, Demand, Program\) in the Goal Relationship \[sn\_gf\_goal\_m2m\_relationship\] table with the first goal \(from the order in the glide list\) as the primary goal.

</td></tr><tr><td>

migrateStrategyData

</td><td>

Migrates all existing strategy records from the Enterprise Strategy \[enterprise\_strategy\], Business Unit Strategy \[business\_unit\_strategy\], and Strategic Objective \[strategic\_objective\] tables to the Strategic Priority \[sn\_gf\_strategy\] table. The sys\_id remains the same.

</td></tr><tr><td>

migratingGoalStrategyM2Mdata

</td><td>

In Goal Framework, a goal can be mapped to only one strategy. If an existing goal has two strategies mapped to it, a clone of the goal will be created \(one as a generic goal and another as a sub-goal\) with the same strategy populated for both. And, for the sub-goal, the first goal will be set as the parent goal.For example, consider a scenario where an existing goal \(G1\) is mapped to five strategies \(S1, S2, S3, S4, and S5\). Then, four clones of G1 will be created as sub-goals \(G2, G3, G4, and G5\) and the parent goal is populated as G1. For the parent goal \(G1\) and the sub-goals \(G2, G3, G4, and G5\), the **Strategy** field is populated respectively \(S1, S2, S3, S4, and S5\).

 **Note:** The name of the cloned sub-goal will be prefixed with `Cloned SubGoal:`, followed by the parent goal name.

</td></tr><tr><td>

migrateStrategyWorkItemRelData

</td><td>

-   Migrates the existing relationship of strategy and work items \(Project, Demand, Program\) to the Goal Relationship \[sn\_gf\_goal\_m2m\_relationship\] table.
-   If a goal doesn't have an association between the strategy \(as current strategy\) and the work item in the Goal Relationship \[sn\_gf\_goal\_m2m\_relationship\] table, a dummy goal will be created with a strategy value of current strategy. And, a goal relationship is created with the dummy goal and the work item in the Goal Relationship \[sn\_gf\_goal\_m2m\_relationship\] table.

**Note:** The name of the dummy goal will be prefixed with `Goal:`, followed by the strategy name.


</td></tr></tbody>
</table>## Migrate goal relationships for assigned entities

Use the **Migrate goal relationships for assigned entities** job to populate the fields, **Assigned entity type** and **Assigned entity** on the [Goal form](goal-form-1.md) based on the existing values in the legacy fields, **Business Unit**, **Department**, **Company**, **Portfolio**, and any customized entity field.

<table id="table_smd_b5p_fwb"><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Migrate goal relationships for assigned entities

</td><td>

\(For Strategic Planning users\) Populates the fields, **Assigned entity type** and **Assigned entity** on the [Goal form](../../spw-goals/reference/goal-form-egm.md) based on the data in the Goal Relationship \[sn\_gf\_goal\_m2m\_relationship\] table if you've created an m2m relationship with lens entities other than **Company**, **Business Unit**, **Department**, and **Portfolio**.If users had already created m2m relationship, they may use this script to move those relationships from the m2m table to the goals table to access and manage those goals in the respective portfolio plans.

 If the goal has only one relationship with an assign entity table type, the **Assign entity type** and **Assign entity** fields are populated on the Goal \[sn\_gf\_goal\] table based on the Goal Relationship \[sn\_gf\_goal\_m2m\_relationship\] table.

 If the goal has multiple relationships with an assign entity table type, number of relationships \(n\) cloned sub-goals will be created and the **Assign entity type** and **Assign entity** fields are populated on the Goal \[sn\_gf\_goal\] table based on the data in the Goal Relationship \[sn\_gf\_goal\_m2m\_relationship\] table for each cloned sub-goal.

</td></tr></tbody>
</table>