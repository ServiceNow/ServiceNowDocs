---
title: Configure the demand AI skills
description: Configure the generative AI skills for demands by defining their triggers, display locations, and access settings to make it available to users.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/demand-management/configure-the-demand-summarization-skill-ppm.html
release: australia
product: Demand Management
classification: demand-management
topic_type: task
last_updated: "2026-07-21"
reading_time_minutes: 2
breadcrumb: [Configure, Demand Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Configure the demand AI skills

Configure the generative AI skills for demands by defining their triggers, display locations, and access settings to make it available to users.

## Before you begin

Role required: sn\_generative\_ai.nsa\_admin

## About this task

**Important:** These generative AI skills are turned on by default. The skills will be automatically available to appropriate role users for the application. For more information, see [AI agents, skills, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills-on-by-default.md).

## Procedure

1.  Navigate to **Admin** &gt; **AI Admin Hub**.

2.  Select **AI Skills**.

3.  In the navigation panel, select **Technology** &gt; **SPM**.

4.  Select **Activate** from a skill card.

5.  Review the input fields for the skill.

    For more information, see [Inputs for AI skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/demand-management/inputs-for-ai-skills-ppm.md).

    A check mark next to each step indicates whether the step is completed, partially completed, or not completed. After configuring a step, select **Save and continue** to go to the next step. Return to a previous step by selecting **Back**.

    **Note:** Some configuration options are read-only.

6.  Define the trigger for the skill.

    -   Automatic: The skill is initiated without user interaction.
    -   User trigger: The skill is initiated when by an user action.
7.  For the demand summarization skill, the triggers behaving in the following ways:
    -   Automatic: The skill is initiated without user interaction. When users navigate to a demand record page, the summary of the record is auto-generated. By default, this trigger is set for demands in the Submitted, Screening, Qualified, and Approved states.
    -   User trigger: The skill is initiated when users select the **Summarize** action on a demand record.
8.  Define and review the user accesses.

9.  Choose where to display the skill.

    The display options may vary from skill to skill.

    **In-product desktop**: When selected, the skill is displayed on forms and workspaces.

10. Open the role selection list next to the Display toggle, and select the roles that can use the skill.

    The user roles added in the **Define access** page for each ACL can be selected in this step.

11. Review the configuration and select **Activate**.


**Parent Topic:**[Configuring Demand Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/demand-management/configuring-demand-management.md)

**Related topics**  


[Summarize demands with the demand summarization skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/demand-management/demand-summary-demand-classic.md)

[AI skills for Demand Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/demand-management/similar-demand-identification-using-now-assist.md)

