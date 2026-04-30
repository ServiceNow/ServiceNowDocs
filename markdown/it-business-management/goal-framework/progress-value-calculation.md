---
title: Progress value calculation
description: The progress or percentage complete value of goals is auto-calculated using different formulas. The formula depends on whether the goal has only targets, a combination of sub-goals and targets, and if it has weighted average calculation enabled.
locale: en-US
release: zurich
product: Goal Framework
classification: goal-framework
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Reference, Goal Framework and Goal Framework for SPM, Strategic Portfolio Management]
---

# Progress value calculation

The progress or percentage complete value of goals is auto-calculated using different formulas. The formula depends on whether the goal has only targets, a combination of sub-goals and targets, and if it has weighted average calculation enabled.

<table id="table_sb2_g2y_gpb"><thead><tr><th>

Scenario

</th><th>

Formula used to calculate the progress value of the goal

</th></tr></thead><tbody><tr><td>

-   The goal has targets.
-   The goal doesn’t have sub-goals.
-   The **Impact on goal** field is defined for targets.

</td><td>

`Progress value of the goal = Sum of progress values of its associated targets / number of targets`

</td></tr><tr><td>

-   The goal has sub-goals and targets.
-   The **Impact on parent goal** and **Impact on goal** fields are defined for sub-goals and targets respectively.

</td><td>

`Progress value of the goal = Sum of progress values of its sub-goals and associated targets / number of sub-goals and targets`

</td></tr><tr><td>

-   The goal has two targets \(target 1 and target 2\).
-   The goal doesn’t have sub-goals.
-   The **Impact on goal** field is defined for targets and the **sn\_gf.weighted\_average\_enabled** system property is set to **Yes**.

</td><td>

`Progress value of the goal = [(Progress of target 1 * Weight scale of target 1) + (Progress of target 2 * Weight scale of target 2)] / (Weight scale of target 1 + Weight scale of target 2)`

</td></tr><tr><td>

-   The goal has two targets \(target 1 and target 2\).
-   The goal has two sub-goals \(sub-goal 1 and sub-goal 2\).
-   The **Impact on parent goal** and **Impact on goal** fields are defined for sub-goals and targets respectively and the **sn\_gf.weighted\_average\_enabled** system property is set to **Yes**.

</td><td>

`Progress value of the goal = [(Progress of sub-goal 1 * Weight scale of sub-goal 1) + (Progress of sub-goal 2 * Weight scale of sub-goal 2) + (Progress of target 1 * Weight scale of target 1) + (Progress of target 2 * Weight scale of target 2)] / (Weight scale of sub-goal 1 + Weight scale of sub-goal 2 + Weight scale of target 1 + Weight scale of target 2)`

</td></tr></tbody>
</table>Consider a scenario where a goal \(G1\) has two targets \(T1 and T2\) and the **Impact on goal** field for T1 and T2 is set to 2 and 3 respectively. The current Progress values of T1 and T2 are 40% and 20% respectively. In this case, the progress value for G1 is calculated as follows:

-   Contribution of T1 towards G1 progress = 2/\(2+3\)\*40 = 16%
-   Contribution of T2 towards G1 progress = 3/\(2+3\)\*20 = 12%
-   Therefore, Progress of G1 = 16% +12% = 28%

**Parent Topic:**[Goal Framework and Goal Framework for SPM reference](../reference/goal-framework-reference.md)

