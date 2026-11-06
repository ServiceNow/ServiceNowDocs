---
title: Generate insights for a goal in Strategic Planning Workspace using ServiceNow Otto for SPM
description: Review AI-generated insights to identify at-risk goals, assess forecasted statuses, and act on recommendations before goals fall off track.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-business-management/scenario-planning-in-spw/generate-insights-for-goal-spw.html
release: australia
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: task
last_updated: "2026-11-06"
reading_time_minutes: 2
breadcrumb: [Manage portfolio plan goals, Portfolio Planning in Strategic Planning Workspace, Strategic Planning, Strategic Portfolio Management]
---

# Generate insights for a goal in Strategic Planning Workspace using ServiceNow Otto for SPM

Review AI-generated insights to identify at-risk goals, assess forecasted statuses, and act on recommendations before goals fall off track.

## Before you begin

**Important:** This generative AI skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [AI agents, skills, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills-on-by-default.md).

Role required: sn\_apw\_advanced.spw\_goal\_user and \(sn\_align\_core.apw\_user or sn\_gf.goal\_admin\)

## About this task

The Goal insights skill analyzes the goal, its targets, subgoals, and aligned work, then delivers concise, data‑driven insights—including AI forecasted status, confidence of achieving the goal, targets at risk, delayed or stalled aligned work and recommendations.

**Note:** When you generate insights for a goal, insights are also generated individually for each of its targets.

The skill analyzes the real-time data — including check-in patterns, comments, and planned versus actual progress — to forecast goal status and surface proactive recommendations.

**Tip:** For better reviews and recommendations, use the Goal insights skill with the AWS Claude model.

The skill supports all target types, including **Maintain above**, **Maintain below**, and **Maintain constant**. For example, the insights can point out a Maintain above target whose latest actual value is below its threshold. For a description of each target type, see [Target types and achievement strategies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/scenario-planning-in-spw/target-types-overview.md).

Insights are based on the latest check-ins at each target's check-in frequency, up to five periods. Periods are referred to by their labels, for example FY27: P03 for a fiscal period.

For Maintain targets, the insights judge whether the target is within its threshold now, not progress toward a finish line. A breached Maintain target is flagged at risk, and a target that is holding within its threshold is not treated as finished.

A goal's forecasted status is the worst status among its targets and sub-goals. Aligned work doesn't change the goal's status.

**Note:** Only the owner or contributors of the goal can generate insights for the goal.

## Procedure

1.  Navigate to **Workspaces** &gt; **Strategic Planning Workspace** &gt; **Portfolio Planning**.

2.  From the list of portfolio plans, select the portfolio plan that the goal belongs to.

3.  From the Goals page, select **Goals and targets**.

4.  From the list of goals, select the name of the goal for which you want to generate insights.

    The goal side pane opens with the **Details** tab.

5.  From the side pane, select **Full Details** to open the goal form.

    The goal’s full details page opens.

6.  Select **Show insights**.

    The Goal insights side pane appears processing the insights for the goal. After a while, the Insights by AI pane shows the insights for the goal including AI forecasted status, confidence of achieving the goal, targets at risk, delayed or stalled aligned work and recommendations.

7.  Review AI-generated insights to identify risk, assess forecasted statuses, and act on recommendations before goals fall off track.


