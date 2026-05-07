---
title: Activate and configure the Goal insights generation job
description: Activate the Goal insights generation scheduled job to automatically generate AI-driven insights for a predefined set of goals at a scheduled frequency.
locale: en-US
release: australia
product: Strategic Planning
classification: strategic-planning
topic_type: task
last_updated: "2026-04-27"
reading_time_minutes: 1
keywords: [goal insights, scheduled job, AI insights, goals, Strategy and Goals, Now Assist for SPM]
breadcrumb: [Goal insights generation job, Configure, Strategy and Goals, Strategic Planning, Strategic Portfolio Management]
---

# Activate and configure the Goal insights generation job

Activate the Goal insights generation scheduled job to automatically generate AI-driven insights for a predefined set of goals at a scheduled frequency.

## Before you begin

Role required: sn\_gf.goal\_admin

## About this task

The Goal insights generation scheduled job is inactive by default. After activation, the job runs at the configured frequency and generates insights for all goals that match the admin-defined filter criteria. With this, goal users no need to generate insights individually for each goal.

**Tip:** For better reviews and recommendations, use the Goal insights skill with the AWS Claude model.

![Configure goal insights scheduled job.](../image/configure-goal-insights-job.gif)

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

    A list of all scheduled jobs appears.

2.  Search for and select the **Goal insights generation job** scheduled job.

3.  Select the **Active** check box to run the job at a scheduled time.

4.  In the **Run** field, select the frequency at which you want to run the scheduled job.

    For example, you can select **Weekly** to run the job every week.

5.  Select **Update** to save the configuration.

    **Important:** The job runs only on goals that match the defined filter criteria. Goals outside the filter criteria are not processed by the job. To optimize system resources and prevent excessive token consumption, define the filter criteria as specifically as possible. For details, see [Configure the goals set for goal insights generation](configure-goals-set-goal-insights-generation.md).

6.  To run the job immediately outside the scheduled frequency, select **Execute Now**.


## Result

The Goal insights generation job is active and configured. The job automatically generates AI-driven insights for all goals that match the defined filter criteria at the configured frequency. The latest insights and their timestamps are displayed on the Goals page.

## What to do next

To generate insights for goals outside the filter criteria, users can manually select **Goal insights** on the Goals page for the required goal. For details, see [Generate insights for a goal](generate-insights-for-goal-strategy.md).

