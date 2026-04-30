---
title: Configuring Schedule Optimization
description: Use Schedule Optimization to automate task assignment, create efficient schedules, and respond to changing conditions as they occur throughout the day.
locale: en-US
release: zurich
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Setting up a Field Service scheduling method, Configure, Field Service Management]
---

# Configuring Schedule Optimization

Use Schedule Optimization to automate task assignment, create efficient schedules, and respond to changing conditions as they occur throughout the day.

## Configuration overview

The Schedule Optimization configuration comprises four main elements: Properties, Policies, Scheduling attributes, and Batches with their associated Scopes. The workflow involves configuring properties to control system-wide behavior, policies to define the rules and priorities that guide optimization, and scheduling attributes to describe the tasks and technicians included in a run. You then create batches and scopes to define what gets optimized, when, and by which method. Additional configurations support intraday and on-demand optimization, allowing scheduling updates in response to changing conditions throughout the day.

## How Schedule Optimization works

Schedule Optimization evaluates available tasks and technicians against configured policies to produce optimized schedules. Each optimization run is associated with a scope, which specifies the scheduling attribute configuration and qualifiers. Qualifiers, such as assignment groups or territories, determine which technicians are included in the run. Assignment groups organize technicians by skill or role, while territories define geographic service areas. Qualifiers support overlapping technicians only when optimizing by territory, not by assignment groups.

Schedule Optimization can be configured to run in three modes:

-   **Batch optimization** runs on a scheduled basis to create optimized schedules for upcoming work. It evaluates all available tasks and technicians within a specified time window and produces a complete schedule based on your configured objectives and constraints.
-   **Intraday optimization** runs throughout the day in response to schedule disruptions such as canceled tasks, new high-priority tasks, or technicians running late or calling in sick. Prioritized event optimization is a focused mode of intraday optimization that triggers shortly after a critical event occurs.
-   **On-demand optimization** allows dispatchers to trigger optimization manually from Dispatcher Workspace at any time.

## Schedule Optimization workflow diagram

The following figure illustrates the high-level workflow of Schedule Optimization in batch mode.

![Schedule Optimization flow diagram showing how batches, scopes, and policies work together. See the previous text description for more information.](../image/sched-opt-flow.png "Schedule Optimization workflow")

## Steps to setup Schedule Optimization

The steps to set up Schedule Optimization are:

1.  Activate the Schedule Optimization plugin. For more information, see [Activate Schedule Optimization](../task/schedule-optimization-engine-plugin.md).
2.  [Set the properties](../reference/schedule-optimization-properties.md) to control optimization behavior and performance in your instance.
3.  Optionally, you can set up [Territory-Based Optimization](../task/territory-based-optimization.md), [Schedule Optimization with Workforce Optimization for Field Service](schedule-optimization-with-workforce-optimization-for-field-service.md), and [Schedule Optimization for Planned Crews](../task/schedule-optimization-for-planned-crews.md) depending on your specific needs.
4.  Create policies that define optimization goals through objectives and constraints. Objectives prioritize how tasks are assigned, such as minimizing travel time or maximizing task assignments. Constraints set rules that must be met before assigning tasks, such as required skills or availability. For more information, see [Create a policy for Schedule Optimization](../task/create-policies-schedule-optimization.md).
5.  Configure scheduling attributes to define reusable optimization settings, including the default policy, travel estimate provider, and applicable qualifiers. For more information, see [Create a scheduling attribute for Schedule Optimization](../task/configure-scheduling-attributes.md).
6.  Create scopes that define the scheduling attribute configuration and qualifiers for an optimization run. Scopes are required for batches to run. For more information, see [Create a scope for Schedule Optimization](../task/create-an-optimization-job-soe.md)
7.  Create batches that define when optimization runs, including start date, run frequency, and start and end times. For more information, see [Create a batch for Schedule Optimization](../task/create-an-optimization-batch.md#).
8.  Optionally, create intraday configurations to trigger optimization in response to schedule disruptions or enable on-demand optimization for dispatchers. For more information, see [Intraday optimization](../task/optimize-your-schedules-intraday.md).

Schedule Optimization supports a high volume of tasks across all three optimization methods by default. If your scheduling needs require expanded capacity, you can contact support or submit a change control request to adjust the configuration.

**Related topics**  


[Schedule Optimization](schedule-optimization.md)

[Schedule Optimization components](../reference/schedule-optimization-components.md)

