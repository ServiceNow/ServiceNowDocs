---
title: Configure the demand AI skills
description: Configure the generative AI skills for demands by defining their triggers, display locations, and access settings to make it available to users.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-business-management/portfolio-planning/configure-demand-ai-skills-ppw.html
release: zurich
product: Portfolio Planning
classification: portfolio-planning
topic_type: task
last_updated: "2026-07-21"
reading_time_minutes: 2
breadcrumb: [Configure, Next Experience for Demand Management in Portfolio Planning, Portfolio Planning, Strategic Portfolio Management]
---

# Configure the demand AI skills

Configure the generative AI skills for demands by defining their triggers, display locations, and access settings to make it available to users.

## Before you begin

Role required: sn\_generative\_ai.nsa\_admin

## About this task

**Important:** These generative AI skills are turned on by default. The skills will be automatically available to appropriate role users for the application. For more information, see [AI agents, skills, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skills-on-by-default.md).

## Procedure

1.  Navigate to **Admin** &gt; **AI Admin Hub**.

2.  Select **AI Skills**.

3.  In the navigation panel, select **Technology** &gt; **SPM**.

4.  Select **Activate** from a skill card.

5.  Review the input fields for the skill.

    For more information, see [Inputs for AI skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/portfolio-planning/skill-inputs-for-ai-skills-ppw.md).

    A check mark next to each step indicates whether the step is completed, partially completed, or not completed. After configuring a step, select **Save and continue** to go to the next step. Return to a previous step by selecting **Back**.

    **Note:** Some configuration options are read-only.

6.  Define the trigger for the skill.

    -   Automatic: The skill is initiated without user interaction.
    -   User trigger: The skill is initiated when by an user action.
7.  For the demand summarization skill, the triggers behaving in the following ways:
    -   Automatic: The skill is initiated without user interaction. When users navigate to the **AI Overview** page of a demand, the summary of the record is auto-generated. By default, this trigger is set for demands in the Submitted, Screening, Qualified, and Approved states.
    -   User trigger: The skill is initiated when users select the **Summarize** action on a demand record.
8.  Define and review the user accesses.

9.  Choose where to display the skill.

    The display options may vary from skill to skill.

    **In-product desktop**: When selected, the skill is displayed on forms and workspaces.

10. Open the role selection list next to the Display toggle, and select the roles that can use the skill.

    The user roles added in the **Define access** page for each ACL can be selected in this step.

11. Review the configuration and select **Activate**.


**Related topics**  


[Summarize demands with the demand summarization skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/portfolio-planning/summarize-demands-in-ppw.md)

[AI skills for Next Experience for Demand Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/portfolio-planning/ai-skills-in-demands-workspace-ppw.md)

