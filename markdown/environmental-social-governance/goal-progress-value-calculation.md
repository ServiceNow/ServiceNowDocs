---
title: Goal progress value calculation
description: The progress or percentage complete value of goals is auto-calculated using different formulas. The formula depends on whether the goal has only targets, a combination of sub-goals and targets, and if it has weighted average calculation enabled.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Create an Operational Sustainability Management \(formerly ESG Management\) goal, Configure, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Goal progress value calculation

The progress or percentage complete value of goals is auto-calculated using different formulas. The formula depends on whether the goal has only targets, a combination of sub-goals and targets, and if it has weighted average calculation enabled.

<table id="table_sb2_g2y_gpb"><thead><tr><th>

Scenario

</th><th>

Formula used to calculate the progress value of the goal

</th></tr></thead><tbody><tr><td>

-   The goal has targets.
-   The goal doesn’t have sub-goals.
-   No weight scale defined for targets.

</td><td>

`Progress value of the goal = Sum of progress values of its associated targets / number of targets`

</td></tr><tr><td>

-   The goal has sub-goals and targets.
-   No weight scale defined for sub-goals and targets.

</td><td>

`Progress value of the goal = Sum of progress values of its sub-goals and associated targets / number of sub-goals and targets`

</td></tr><tr><td>

-   The goal has two targets \(target 1 and target 2\).
-   The goal doesn’t have sub-goals.
-   Weight scale defined for targets and the sn\_gf.weighted\_average\_enabled system property is set to **Yes**.

</td><td>

`Progress value of the goal = [(Progress of target 1 * Weight scale of target 1) + (Progress of target 2 * Weight scale of target 2)] / (Weight scale of target 1 + Weight scale of target 2)`

</td></tr><tr><td>

-   The goal has two targets \(target 1 and target 2\).
-   The goal has two sub-goals \(sub-goal 1 and sub-goal 2\).
-   Weight scale defined for sub-goals and targets and the sn\_gf.weighted\_average\_enabled system property is set to **Yes**.

</td><td>

`Progress value of the goal = [(Progress of sub-goal 1 * Weight scale of sub-goal 1) + (Progress of sub-goal 2 * Weight scale of sub-goal 2) + (Progress of target 1 * Weight scale of target 1) + (Progress of target 2 * Weight scale of target 2)] / (Weight scale of sub-goal 1 + Weight scale of sub-goal 2 + Weight scale of target 1 + Weight scale of target 2)`

</td></tr></tbody>
</table>**Parent Topic:**[Create an Operational Sustainability Management \(formerly ESG Management\) goal](../task/create-esg-goal.md)

