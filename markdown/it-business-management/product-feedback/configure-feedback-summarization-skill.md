---
title: Configure the feedback AI skills
description: Configure the generative AI skills for feedback by defining their triggers, display locations, and access settings to make them available to users.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/product-feedback/configure-feedback-summarization-skill.html
release: brazil
product: Product Feedback
classification: product-feedback
topic_type: task
last_updated: "2026-11-04"
reading_time_minutes: 1
breadcrumb: [Configure, Feedback in Strategic Planning, Strategic Planning, Strategic Portfolio Management]
---

# Configure the feedback AI skills

Configure the generative AI skills for feedback by defining their triggers, display locations, and access settings to make them available to users.

## Before you begin

Role required: sn\_nowassist\_admin.nsa\_admin

## About this task

**Important:** These generative AI skills are turned on by default. The skills will be automatically available to appropriate role users for the application. For more information, see [AI agents, skills, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-skills-on-by-default.md).

## Procedure

1.  Navigate to **Admin** &gt; **AI Admin Hub**.

2.  Select **AI Skills**.

3.  In the navigation panel, select **Technology** &gt; **SPM**.

4.  Select **Activate** from a skill card.

5.  Review the input fields for the skill.

    A check mark next to each step indicates whether the step is completed, partially completed, or not completed. After configuring a step, select **Save and continue** to go to the next step. Return to a previous step by selecting **Back**.

    **Note:** Some configuration options are read-only.

6.  Define the trigger for the skill.

    -   Automatic: The skill is initiated without user interaction.
    -   User trigger: The skill is initiated when by an user action.
7.  Define and review the user accesses.

8.  Choose where to display the skill.

    The display options may vary from skill to skill.

    **In-product desktop**: When selected, the skill is displayed on forms and workspaces.

9.  Open the role selection list next to the Display toggle, and select the roles that can use the skill.

    The user roles added in the **Define access** page for each ACL can be selected in this step.

10. Review the configuration and select **Activate**.


**Parent Topic:**[Configuring Feedback application in Strategic Planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/product-feedback/configuring-product-feedback-in-sp.md)

**Related topics**  


[Summarize the feedback by using ServiceNow Otto for Strategic Portfolio Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/product-feedback/feedback-summary-sentiment-topics-pf.md)

[AI Skills in Feedback application in Strategic Planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/product-feedback/ai-skills-in-feedback-spw.md)

