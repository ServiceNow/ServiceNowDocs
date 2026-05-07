---
title: Generate targets for a goal in Strategic Planning Workspace using Now Assist for SPM
description: Generate measurable targets for your goals in Strategic Planning Workspace using Now Assist for SPM.
locale: en-US
release: australia
product: Now Assist for Strategic Portfolio Management \(SPM\)
classification: now-assist-for-strategic-portfolio-management-spm
topic_type: task
last_updated: "2026-05-06"
reading_time_minutes: 2
keywords: [Target generation, Now Assist skill, Now Assist, Gen AI, Generative AI, Email project summary, Strategic Portfolio Management, SPM]
breadcrumb: [Using Now Assist for Strategic Portfolio Management \(SPM\), Now Assist for Strategic Portfolio Management \(SPM\), Strategic Portfolio Management]
---

# Generate targets for a goal in Strategic Planning Workspace using Now Assist for SPM

Generate measurable targets for your goals in Strategic Planning Workspace using Now Assist for SPM.

## Before you begin

**Important:** This Now Assist skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

Role required: sn\_apw\_advanced.spw\_goal\_user and \(sn\_align\_core.apw\_user or sn\_gf.goal\_admin\)

## About this task

The Target generation skill leverages the goal’s details and provided context to create a precise target for the goal. The more specific the input, the stronger the recommendations.

The skill automatically populates key fields in the Target form, ensuring accuracy and alignment with the goal. This helps teams define clear, measurable outcomes and speeds up the target-setting process.

**Note:** Only the owner or contributors of the goal can create targets for the goal.

![Generate targets in Strategic Planning Workspace using Target generation skill.](../images/target-generation-skill.gif)

## Procedure

1.  Navigate to **Workspaces** &gt; **Strategic Planning Workspace** &gt; **Portfolio Planning**.

2.  From the list of portfolio plans, select the required portfolio plan that the goal belongs to.

3.  In the Goals view, select the **Goals and targets** tab.

4.  Next to the goal that you want to create a target for, select the row context menu icon \(![Row context menu icon.](../../alignment-planner-workspace/images/action-menu-icon.png)\) and select **Generate target**.

5.  On the Provide context to generate a target window, enter a context to generate a desired target and then select **Generate**.

    **Tip:** The more specific the input, the stronger the recommendations.

6.  On the form, verify the filed values and update them as needed.

    For a description of the field values, see [Target form](../../spw-goals/reference/target-form-egm.md).

7.  Select **Save**.


## Result

A target is created based on the goal’s details and any context that you provide.

The target progress records are automatically created when you save the target post populating the **Actuals to date** field. The target progress records specify the progress of each target for the goal.

**Note:** When you delete a goal, its associated targets \(if any\) and their progress records are also deleted even though the **Allow the deletion of targets** property is set to **No**.

## What to do next

[Update the progress of the target](../../spw-goals/task/update-progress-of-target-egm.md) manually if the target isn’t enabled for target automation.

**Parent Topic:**[Using Now Assist for Strategic Portfolio Management \(SPM\)](../concept/using-now-assist-for-spm.md)

**Related topics**  


[Add targets for a goal in Strategic Planning](../../spw-goals/task/set-targets-for-goal-egm.md)

