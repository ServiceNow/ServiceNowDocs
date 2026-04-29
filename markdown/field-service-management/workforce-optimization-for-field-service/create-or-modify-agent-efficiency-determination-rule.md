---
title: Create or modify an Agent Efficiency determination rule
description: Create or modify an Agent Efficiency determination rule for work order tasks.
locale: en-US
release: australia
product: Workforce Optimization for Field Service
classification: workforce-optimization-for-field-service
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Agent Efficiency, Set up workforce, Configure, Field Service Management]
---

# Create or modify an Agent Efficiency determination rule

Create or modify an Agent Efficiency determination rule for work order tasks.

## Before you begin

Role required: wm\_admin, wm\_dispatcher

## About this task

An Agent Efficiency determination rule automatically assigns Agent Efficiency criteria to a qualified work order task. Intelligent Task Recommendation uses Agent Efficiency determination rules to recommend the best-suited tasks for an agent.

## Procedure

1.  Navigate to **All** &gt; **Agent Efficiency** &gt; **Agent Efficiency Determination Rules**.

2.  Create or modify a determination rule.

    -   To create a new rule, select **New**.
    -   To modify a rule, select its name.
3.  On the form, fill in or modify the fields.

<table id="table_ic4_cbb_fdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the rule.

</td></tr><tr><td>

Application

</td><td>

Application to which the rule applies. This field is automatically set to **Global** and cannot be modified.

</td></tr><tr><td>

Type

</td><td>

The type of the determination rule.-   **Simple**: A simple determination rule using one or more filter conditions.
-   **Advanced**: A determination rule that uses a script.


</td></tr><tr><td>

Active

</td><td>

Activates the determination rule.

</td></tr><tr><td>

Source table

</td><td>

The table to which this determination rule applies.

</td></tr><tr><td>

Order

</td><td>

The priority for the determination rule. Determination rules with lower order values are applied first.

</td></tr><tr><td>

Condition

</td><td>

One or more conditions to determine the work order tasks to which this determination rule applies.**Note:** This field appears only when **Type** is selected from **Simple**.

</td></tr><tr><td>

Agent efficiency criteria

</td><td>

The Agent Efficiency criterion to which the determination rule applies.**Note:** This field appears only when **Type** is selected from **Simple**.

</td></tr><tr><td>

Script

</td><td>

A script to define the determination rule details.**Note:** This field appears only when **Type** is selected from **Advanced**.

</td></tr></tbody>
</table>4.  Select **Submit**.


## Result

The determination rule is created.

## What to do next

[Assign an Agent Efficiency value to agents](assign-efficiency-value-to-agents.md)

