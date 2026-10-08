---
title: Generate targets for a goal in Strategic Planning Workspace using ServiceNow Otto for SPM
description: Generate measurable targets for your goals in Strategic Planning Workspace using ServiceNow Otto for SPM.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/scenario-planning-in-spw/generate-targets-for-goal.html
release: brazil
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: task
last_updated: "2026-10-08"
reading_time_minutes: 3
keywords: [Target generation, Now Assist skill, Now Assist, Gen AI, Generative AI, Email project summary, Strategic Portfolio Management, SPM]
breadcrumb: [Manage portfolio plan goals, Portfolio Planning in Strategic Planning Workspace, Strategic Planning, Strategic Portfolio Management]
---

# Generate targets for a goal in Strategic Planning Workspace using ServiceNow Otto for SPM

Generate measurable targets for your goals in Strategic Planning Workspace using ServiceNow Otto for SPM.

## Before you begin

**Important:** This generative AI skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [AI agents, skills, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-skills-on-by-default.md).

Role required: sn\_apw\_advanced.spw\_goal\_user and \(sn\_align\_core.apw\_user or sn\_gf.goal\_admin\)

## About this task

The Target generation skill leverages the goal’s details and provided context to create a precise target for the goal. The more specific the input, the stronger the recommendations.

The skill automatically populates key fields in the Target form, ensuring accuracy and alignment with the goal. This helps teams define clear, measurable outcomes and speeds up the target-setting process.

The skill suggests the target type based on the goal’s details and the context that you enter in the Provide context to generate a target window. Depending on that context, the type can be **Maximize**, **Minimize**, **Milestone**, **Maintain above**, **Maintain below**, or **Maintain constant**. For goals about sustaining a level rather than changing one, such as keeping service uptime at or above a threshold, staying within a cost ceiling, or holding headcount steady, the skill suggests one of the Maintain types. For a description of each target type, see [Target types and achievement strategies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/scenario-planning-in-spw/target-types-overview.md).

**Note:** Only the owner or contributors of the goal can create targets for the goal.

\[Omitted video\] Description: Generate targets for a goal in Strategic Planning Workspace using ServiceNow Otto for SPM

## Procedure

1.  Navigate to **Workspaces** &gt; **Strategic Planning Workspace** &gt; **Portfolio Planning**.

2.  From the list of portfolio plans, select the required portfolio plan that the goal belongs to.

3.  In the Goals view, select the **Goals and targets** tab.

4.  Next to the goal that you want to create a target for, select the row context menu icon \(\[Omitted image "action-menu-icon.png"\] Alt text: Row context menu icon.\) and select **Generate target**.

5.  On the Provide context to generate a target window, enter a context to generate a desired target and then select **Generate**.

    **Tip:** The more specific the input, the stronger the recommendations.

6.  On the form, verify the field values and update them as needed.

    For a description of the field values, see [Target form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/scenario-planning-in-spw/target-form-egm.md).

    The **Type** field is set based on the goal and the context that you provide. The skill can suggest **Maximize**, **Minimize**, **Milestone**, **Maintain above**, **Maintain below**, or **Maintain constant**. If the suggested type doesn’t fit your goal, select a different type before you save. For a Maintain type, the **Final target value** is the threshold to maintain. For example, 99.5 for an uptime target that must stay at or above 99.5%.

7.  Select **Save**.


## Result

A target is created based on the goal’s details and any context that you provide.

The target progress records are automatically created when you save the target post populating the **Actuals to date** field. The target progress records specify the progress of each target for the goal.

**Note:** When you delete a goal, its associated targets \(if any\) and their progress records are also deleted even though the **Allow the deletion of targets** property is set to **No**.

## What to do next

[Update the progress of the target](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/scenario-planning-in-spw/update-progress-of-target-egm.md) manually if the target isn’t enabled for target automation.

**Related topics**  


[Add targets for a goal in Strategic Planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/scenario-planning-in-spw/set-targets-for-goal-egm.md)

[Target types and achievement strategies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/scenario-planning-in-spw/target-types-overview.md)

