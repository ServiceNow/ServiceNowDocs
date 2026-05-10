---
title: Generate insights for a goal
description: Review AI-generated insights to identify at-risk goals, assess forecasted statuses, and act on recommendations before goals fall off track.
locale: en-US
release: australia
product: Strategic Planning
classification: strategic-planning
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Manage enterprise goals, Strategy and Goals, Strategic Planning, Strategic Portfolio Management]
---

# Generate insights for a goal

Review AI-generated insights to identify at-risk goals, assess forecasted statuses, and act on recommendations before goals fall off track.

## Before you begin

**Important:** This Now Assist skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills/now-assist-skills-on-by-default.md).

Role required: sn\_apw\_advanced.spw\_goal\_user

## About this task

The Goal insights skill analyzes the goal, its targets, subgoals, and aligned work, then delivers concise, data‑driven insights—including AI forecasted status, confidence of achieving the goal, targets at risk, delayed or stalled aligned work and recommendations.

**Note:** When you generate insights for a goal, insights are also generated individually for each of its targets.

The skill analyzes the real-time data — including check-in patterns, comments, and planned versus actual progress — to forecast goal status and surface proactive recommendations.

**Tip:** For better reviews and recommendations, use the Goal insights skill with the AWS Claude model.

**Note:** Only the owner or contributors of the goal can generate insights for the goal.

![Generate goal insights in Strategic Planning Workspace using Goal insights skill.](../../now-assist-spm/images/generate-goal-insights.gif)

**Note:** If the Goal insights generation job is enabled, it automatically generates insights for each goal based on the job's run frequency. Before manually regenerating, check the timestamp on the goal insights summary card to confirm when insights were last generated — regenerating unnecessarily increases token consumption. You can also view the last generated insights in the **AI rationale** column of the goal list. If goal or target data has changed since the last run, select the refresh icon on the goal insights summary card to regenerate the insights.

## Procedure

1.  Navigate to **Workspaces** &gt; **Strategic Planning Workspace** &gt; **Strategy and Goals**.

2.  Select **Favorites**, **Shared with me**, **Created by me**, or **Public**, depending on where the board is located.

3.  Select the board that contains the goal for which you want to generate insights.

4.  From the list of goals, select the Goal insights icon next to the goal.

    Alternatively, you can select **Show insights** on the goal's full details page.

    The Goal insights side pane appears to process the insights for the goal. After a while, the Insights by Now Assist pane shows the insights for the goal including AI forecasted status, confidence of achieving the goal, targets at risk, delayed or stalled aligned work and recommendations.

5.  Review AI-generated insights to identify risk, assess forecasted statuses, and act on recommendations before goals fall off track.


**Related topics**  


[Create a goal](create-goal-strategy.md)

[Add a target for goal](set-target-for-goal-strategy.md)

[Duplicate a goal or target](duplicate-goal-target-strategy.md)

[Align work with a goal or target](associate-work-with-goals-strategy.md)

[Send a reminder for target actuals check in](send-reminder-target-checkin-strategy.md)

