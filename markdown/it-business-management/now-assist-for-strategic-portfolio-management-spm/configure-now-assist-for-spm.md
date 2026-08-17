---
title: Configure ServiceNow Otto for Strategic Portfolio Management
description: If you have the admin role, you can configure the ServiceNow Otto for Strategic Portfolio Management application to enable generative AI skills in Strategic Planning, Project Workspace, Demand Management, or Enterprise Agile Planning.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/it-business-management/now-assist-for-strategic-portfolio-management-spm/configure-now-assist-for-spm.html
release: yokohama
product: Now Assist for Strategic Portfolio Management \(SPM\)
classification: now-assist-for-strategic-portfolio-management-spm
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
keywords: [Now Assist for SPM configuration, Now Assist for SPM features and skills, Choose inputs, Activate and configure the skills, Project Gen AI Docs, Multi feedback summarization, Conversational experiences for demand creation]
breadcrumb: [ServiceNow Otto for Strategic Portfolio Management, Strategic Portfolio Management]
---

# Configure ServiceNow Otto for Strategic Portfolio Management

If you have the admin role, you can configure the ServiceNow Otto for Strategic Portfolio Management application to enable generative AI skills in Strategic Planning, Project Workspace, Demand Management, or Enterprise Agile Planning.

## Before you begin

**Important:** This Now Assist skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/now-assist-skills-on-by-default.md).

To enable the Agile story generation skill and project insights generation skill, ensure that Now assist panel is enabled. For more information, see [Activate Now Assist panel standard chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/activate-now-assist-panel.md). For Agile story generation skill, ensure AI Search is activated and ready to use by navigating to **All** &gt; **AI Search** &gt; **AI Search Status**

Role required: admin

## About this task

The following table lists the features and skills that you can access from the AI Admin Hub console.

<table id="table_u5z_gfb_fbc"><thead><tr><th>

SPM feature

</th><th>

Skill

</th></tr></thead><tbody><tr><td>

Feedback

</td><td>

-   Feedback summarization
-   Multi feedback summarization

</td></tr><tr><td>

Demand

</td><td>

-   Conversational experiences for demand creation
-   Identify similar records

</td></tr><tr><td>

Docs

</td><td>

-   Project doc summarization \(Project Workspace\)
-   Planning item doc summarization \(Strategic Planning\)
-   EAP doc summarization \(Enterprise Agile Planning\)

</td></tr><tr><td>

Project

</td><td>

Project insights generation

</td></tr><tr><td>

Stories

</td><td>

Story generation

</td></tr><tr><td>

Product idea, Demand, Epic, Project, Capability, Feature, or Story

</td><td>

Refine records

</td></tr></tbody>
</table>The ServiceNow Otto for SPM application and conversational experiences for demand creation system requirements are as follows:

-   Now Assist for Platform
-   Strategic Planning
-   Project Workspace
-   Demand workbench
-   SPM Pro Plus license

## Procedure

1.  Install the ServiceNow Otto for Strategic Portfolio Management plugin \(sn\_spm\_gen\_ai\).

    -   For information about the application dependencies, see [Supporting information for ServiceNow Otto for Strategic Portfolio Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-business-management/now-assist-for-strategic-portfolio-management-spm/supporting-info-now-assist-spm.md).
    -   For information about the installation process, see [Install Now Assist plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/install-now-assist-feature-plugins.md).
2.  Navigate to **Now Assist Admin** &gt; **Now Assist Skills**.

3.  Select the **Technology** category and then select **SPM**.

4.  Choose your Now Assist skill and activate it.

<table id="choicetable_vkp_mtx_mhc"><thead><tr><th align="left" id="d229821e326">

Option

</th><th align="left" id="d229821e329">

Steps

</th></tr></thead><tbody><tr><td id="d229821e335">

**Skill tiles with Turn on option**

</td><td>

1.  Select **Turn on**.
2.  In Add users access section, specify the user or roles.

\[Omitted image "edit-access-project-insights-generation.png"\] Alt text: Edit access screen for Project insights generation skill.

3.  Review the role restrictions to skill.
4.  Select **Turn on** to activate the skill.


</td></tr><tr><td id="d229821e371">

**Skill tiles with Activate skill option**

</td><td>

1.  Select **Activate skill**
2.  **Choose inputs**:
    -   Review the data source, such as the tables and fields. The inputs for most skills are selected by default and can't be modified. For information about the inputs for each skill, see [Skill inputs for ServiceNow Otto for Strategic Portfolio Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-business-management/now-assist-for-strategic-portfolio-management-spm/skill-inputs-for-now-assist-for-spm.md).

\[Omitted image "inputs-feedback.png"\] Alt text: Choose inputs for the multi feedback summarization skill in the Choose Input screen.

    -   Select **Save and continue**.
3.  **Define access**: Review who has access to skills.
    -   Configure ACLs or role-based permissions to ensure who can view or edit the skills.
    -   Review role restrictions to skill.
4.  **Select display**: Review where the skill appears.
    -   **In-product desktop**: Enabling this option shows the skill within the Strategic Planning workspace.
    -   **Now Assist panel**: Enabling this option shows the skill within the Now Assist panel when launched from the Strategic Planning workspace.

**Note:** The display options are available based on the skill.

    -   Select **Save and continue**.
5.  **Review and activate**: Review the summary of your choices and activate the skill by selecting **Activate**.


</td></tr></tbody>
</table>5.  Repeat the process to activate any other available skills for SPM.

    **Important:** The Acceptance criteria generation skill also requires activating Refine Records skill.


## Result

The skill is configured and activated.

**Related topics**  


[Using ServiceNow Otto for Strategic Portfolio Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-business-management/now-assist-for-strategic-portfolio-management-spm/using-now-assist-for-spm.md)

[AI Admin Hub console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/configuring-now-assist.md)

[Configuring Now Assist settings and features](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/configuring-na-landing.md)

