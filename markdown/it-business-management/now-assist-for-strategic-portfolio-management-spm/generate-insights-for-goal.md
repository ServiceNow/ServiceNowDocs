---
title: Generate insights for a goal in Strategic Planning Workspace using Now Assist for SPM
description: Review AI-generated insights to identify at-risk goals, assess forecasted statuses, and act on recommendations before goals fall off track.
locale: en-US
release: australia
product: Now Assist for Strategic Portfolio Management \(SPM\)
classification: now-assist-for-strategic-portfolio-management-spm
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using Now Assist for Strategic Portfolio Management \(SPM\), Now Assist for Strategic Portfolio Management \(SPM\), Strategic Portfolio Management]
---

# Generate insights for a goal in Strategic Planning Workspace using Now Assist for SPM

Review AI-generated insights to identify at-risk goals, assess forecasted statuses, and act on recommendations before goals fall off track.

## Before you begin

**Important:** This Now Assist skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

Role required: sn\_apw\_advanced.spw\_goal\_user and \(sn\_align\_core.apw\_user or sn\_gf.goal\_admin\)

## About this task

The Goal insights skill analyzes the goal, its targets, subgoals, and aligned work, then delivers concise, data‑driven insights—including AI forecasted status, confidence of achieving the goal, targets at risk, delayed or stalled aligned work and recommendations.

**Note:** When you generate insights for a goal, insights are also generated individually for each of its targets.

The skill analyzes the real-time data — including check-in patterns, comments, and planned versus actual progress — to forecast goal status and surface proactive recommendations.

**Tip:** For better reviews and recommendations, use the Goal insights skill with the AWS Claude model.

**Note:** Only the owner or contributors of the goal can generate insights for the goal.

![Generate goal insights in Strategic Planning Workspace using Goal insights skill.](../images/generate-goal-insights.gif)

**Note:** If the Goal insights generation job is enabled, it automatically generates insights for each goal based on the job's run frequency. Before manually regenerating, check the timestamp on the goal insights summary card to confirm when insights were last generated — regenerating unnecessarily increases token consumption. You can also view the last generated insights in the **AI rationale** column of the goal list. If goal or target data has changed since the last run, select the refresh icon on the goal insights summary card to regenerate the insights.

## Procedure

1.  Navigate to **Workspaces** &gt; **Strategic Planning Workspace** &gt; **Strategy and Goals**.

2.  Select **Favorites**, **Shared with me**, **Created by me**, or **Public**, depending on where the board is located.

3.  Select the board that contains the goal for which you want to generate insights.

4.  From the list of goals, select Goal insights icon next to the goal.

    Alternatively, you can select **Show insights** on the goal's full details page.

    The Goal insights side pane appears processing the insights for the goal. After a while, the Insights by Now Assist pane shows the insights for the goal including AI forecasted status, confidence of achieving the goal, targets at risk, delayed or stalled aligned work and recommendations.

5.  Review AI-generated insights to identify risk, assess forecasted statuses, and act on recommendations before goals fall off track.


**Parent Topic:**[Using Now Assist for Strategic Portfolio Management \(SPM\)](../concept/using-now-assist-for-spm.md)

**Related topics**  


[Update the progress of an automated target](../../spw-goals/task/update-progress-of-target-agf-apw.md)

[Update the progress of a manual target](../../spw-goals/task/update-progress-of-target-egm.md)

