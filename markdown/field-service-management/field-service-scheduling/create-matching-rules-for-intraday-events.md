---
title: Create matching rules for intraday events
description: Create matching rules to specify which tasks and technicians to include in prioritized intraday optimization runs.
locale: en-US
release: australia
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Optimization for prioritized events, Intraday optimization, Schedule Optimization, Setting up a Field Service scheduling method, Configure, Field Service Management]
---

# Create matching rules for intraday events

Create matching rules to specify which tasks and technicians to include in prioritized intraday optimization runs.

## Before you begin

[Set up prioritized intraday optimization with matching rules](set-up-prioritized-intraday-optimization-with-matching-rules.md)

Role required: wm\_admin

## About this task

Create matching rules within a specific intraday optimization configuration. Matching rules execute in order based on the **Execution Order** field, with lower numbers processing first.

## Procedure

1.  Navigate to **All** &gt; **Schedule Optimization** &gt; **Intraday Optimization** &gt; **Configurations**.

2.  Select the configuration where you want to add the matching rule.

3.  In the **Matching Rules** tab, select **New**.

    A new window opens with the Matching Rule form.

4.  Complete the form.

<table id="table_om2_rvx_g3c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Execution Order

</td><td>

Order in which the rule processes:Rules with lower numbers process first. All rules execute from the lowest to the highest order numbers, regardless of order in the list.

For example, matching rule with order 100 includes technicians with specific skills who are available within a defined time frame.

When technicians match the criteria, they’re included in optimization. When no technicians meet the criteria, the second rule \(order 200\) runs with broader criteria.

</td></tr><tr><td>

Active

</td><td>

Select the check box to enable the rule.

</td></tr><tr><td>

Table

</td><td>

Table with the records that the matching rule applies to. Select **Intraday Event** or an extension of that table.

</td></tr><tr><td>

Conditions

</td><td>

Conditions in which the matching rule applies. Define conditions that classify which types of events the rule executes for.

</td></tr><tr><td>

Matching

</td><td>

Indicates the option to match the rules. Select **Selection Criteria** to use the supported criteria for radius and skills. Other options require custom configuration.

</td></tr></tbody>
</table>5.  Select **Submit**.

6.  If you selected **Selection Criteria** in the **Matching** field, add matching criteria in the **Matching Criteria** related list.

7.  Choose which event types use matching rules.

    1.  Navigate to **All** &gt; **Schedule Optimization** &gt; **Intraday Optimization** &gt; **Event Types**.

    2.  For each event type you want to optimize with matching rules, set the **Prioritized** field to **True**.


## Result

The matching rule is added to the configuration and executes when the specified conditions are met during prioritized intraday optimization.

**Related topics**  


[Optimizing technician schedules at set intervals throughout the day](optimize-your-schedules-intraday.md)

[Optimizing technician schedules in response to urgent events](triggering-optimization-on-task-or-agent-availability-change.md)

