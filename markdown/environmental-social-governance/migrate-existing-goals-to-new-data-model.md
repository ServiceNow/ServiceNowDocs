---
title: Migrate existing goals data to Goal Framework
description: With the admin role, you can migrate the existing goals data to the Goal Framework tables by running the scheduled job.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Create an Operational Sustainability Management \(formerly ESG Management\) goal, Configure, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Migrate existing goals data to Goal Framework

With the admin role, you can migrate the existing goals data to the Goal Framework tables by running the scheduled job.

## Before you begin

Role required: sys\_admin

## About this task

If you are an existing user of IT Business Management, then you must migrate your existing goals to the Goal Framework. New customers automatically have the new framework and they do not need to run the job mentioned in this procedure.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

2.  Search and click the **Migrating Goal, Strategy, and related Work Item data to the new tables** scheduled job.

3.  On the Scheduled Script Execution form, perform the following steps:

    1.  Ensure that the frequency is selected as **On Demand** in the **Run** field.

    2.  Set the value to **true** for the required parameters in the **Run this script** field.

<table id="table_fmv_jrg_wqb"><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

migrateGoalData

</td><td>

-   Migrates all existing goal records from the Goal \[goal\] table to the Goal \[sn\_gf\_goal\] table. The sys\_ID remains the same. The corresponding target records will be created in the Target \[sn\_gf\_goal\_target\] table.
-   Creates the existing relationship between the goal and work items \(Project, Demand, Program\) in the Goal Relationship \[sn\_gf\_goal\_m2m\_relationship\] table with the first goal as the primary goal.
 **Note:** Only existing goal records that have the **Direction** field populated on the Goal \[goal\] table are migrated to the Goal \[sn\_gf\_goal\] table.

</td></tr><tr><td>

migrateStrategyData

</td><td>

Migrates all existing strategy records from the Enterprise Strategy \[enterprise\_strategy\], Business Unit Strategy \[business\_unit\_strategy\], and Strategic Objective \[strategic\_objective\] tables to the Strategic Priority \[sn\_gf\_strategy\] table. The sys\_ID remains the same.

</td></tr><tr><td>

migratingGoalStrategyM2Mdata

</td><td>

In Goal Framework, a goal can be mapped to only one strategy. If an existing goal has two strategies mapped to it, a clone of the goal will be created \(one as a generic goal and another as a sub-goal\) with the same strategy populated for both. And, for the sub-goal, the first goal will be set as the parent goal.For example, consider a scenario where an existing goal \(G1\) is mapped to five strategies \(S1, S2, S3, S4, and S5\). Then, four clones of G1 will be created as sub-goals \(G2, G3, G4, and G5\) and the parent goal is populated as G1. For the sub-goals \(G2, G3, G4, and G5\), the **Strategy** field is populated respectively \(S1, S2, S3, S4, and S5\).

 **Note:** The name of the cloned sub-goal will be prefixed with `Cloned SubGoal:`, followed by the parent goal name.

</td></tr><tr><td>

migrateStrategyWorkItemRelData

</td><td>

-   Migrates the existing relationship of strategy and work items \(Project, Demand, Program\) to the Goal Relationship \[sn\_gf\_goal\_m2m\_relationship\] table.
-   If a goal does not have an association between the strategy \(as current strategy\) and the work item in the Goal Relationship \[sn\_gf\_goal\_m2m\_relationship\] table, a dummy goal will be created with a strategy value of current strategy. And, a goal relationship is created with the dummy goal and the work item in the Goal Relationship \[sn\_gf\_goal\_m2m\_relationship\] table.

**Note:** The name of the dummy goal will be prefixed with `Goal:`, followed by the strategy name.

</td></tr></tbody>
</table>4.  Click **Execute Now**.


**Parent Topic:**[Create an Operational Sustainability Management \(formerly ESG Management\) goal](create-esg-goal.md)

