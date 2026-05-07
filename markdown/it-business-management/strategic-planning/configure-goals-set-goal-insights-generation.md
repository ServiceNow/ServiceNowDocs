---
title: Configure the goals set for goal insights generation
description: Configure the filter criteria for the Goal insights generation scheduled job to define the set of goals for which insights are automatically generated.
locale: en-US
release: australia
product: Strategic Planning
classification: strategic-planning
topic_type: task
last_updated: "2026-04-27"
reading_time_minutes: 1
keywords: [goal insights, scheduled job, filter criteria, goals, Strategy and Goals, Now Assist for SPM]
breadcrumb: [Goal insights generation job, Configure, Strategy and Goals, Strategic Planning, Strategic Portfolio Management]
---

# Configure the goals set for goal insights generation

Configure the filter criteria for the Goal insights generation scheduled job to define the set of goals for which insights are automatically generated.

## Before you begin

Role required: sn\_gf.goal\_admin

## About this task

By default, the Goal insights generation job runs on the predefined set of goals using the goals filter criteria \(**Goal insights generation filter**\) in the system. If the predefined filter criteria doesn’t match goals set that you want to run the job, administrators must edit the predefined filter criteria to run the goal insights generation job on the specific set of goals as required.

![Default goals set for goal insights generation.](../image/default-goals-set-for-goal-insights-generation.png "Goal insights generation filter")

**Tip:** Defining a precise goals set helps optimize AI resource usage and prevents excessive token consumption.

If a goal does not match the configured filter criteria, users can still generate insights for it manually by selecting the **Goal insights** button on the Goals page.

## Procedure

1.  Navigate to **All** &gt; **Enterprise Goal Management** &gt; **Goals**.

    A list of all goals appears.

2.  Select the predefined goals list view by navigating to **List controls** &gt; **Filters** &gt; **Goal insights generation filter**

    ![Goal insights generation filter.](../image/goal-insights-generation-filter.png)

3.  Select the Show / hide filter icon \(![Show or hide filter icon.](../image/goal-insights-filter-icon.png)\).

4.  Add or edit the filter conditions as needed per your set of goals on which you want to the scheduled job.

5.  Select **Save Filters** to save the filter criteria.


## Result

The filter criteria is saved. The Goal insights generation job processes the goals that match the defined filter criteria and automatically generates insights for them at the configured frequency. Goals outside the filter criteria are not processed by the job.

## What to do next

Activate the Goal insights generation scheduled job to automatically generate AI-driven insights for a predefined set of goals at a scheduled frequency. For details, see [Activate and configure the Goal insights generation job](activate-goal-insights-generation-job.md).

