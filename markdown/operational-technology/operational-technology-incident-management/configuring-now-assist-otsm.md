---
title: Configure ServiceNow Otto for Operational Technology \(OT\) Service Management
description: If you have the admin role, you can configure the ServiceNow Otto for Operational Technology \(OT\) Service Management application so that teams can use the generative AI capabilities in the Industrial Workspace for their Operational Technology \(OT\) incidents.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/operational-technology/operational-technology-incident-management/configuring-now-assist-otsm.html
release: zurich
product: Operational Technology Incident Management
classification: operational-technology-incident-management
topic_type: task
last_updated: "2026-07-23"
reading_time_minutes: 3
breadcrumb: [Configure, Operational Technology Incident Management, Operational Technology]
---

# Configure ServiceNow Otto for Operational Technology \(OT\) Service Management

If you have the admin role, you can configure the ServiceNow Otto for Operational Technology \(OT\) Service Management application so that teams can use the generative AI capabilities in the Industrial Workspace for their Operational Technology \(OT\) incidents.

## Before you begin

Role required: admin

## About this task

Use the AI Admin Hub console to configure ServiceNow Otto for OT Service Management. The console helps you install plugins and configure generative AI skills. For more information, see [Overview tab in AI Admin Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/configuring-now-assist.md).

You can also set up AI Enhanced Recommended Actions for OTSM to use with ServiceNow Otto for OT Service Management. For more information, see [Set up AI Enhanced Recommended Actions for Operational Technology Service Management \(OTSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/operational-technology/set-up-ai-enhanced-ra-otsm.md).

**Important:** Some generative AI skills, AI agents, and agentic workflows are turned on by default. For more information, see [AI agents, skills, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skills-on-by-default.md).

The following table lists the features and skills that you can access from the AI Admin Hub console.

<table id="table_nbg_fzk_fdc"><thead><tr><th>

OTSM features

</th><th>

Skills

</th></tr></thead><tbody><tr><td>

Gen AI skills for OT incident

</td><td>

-   OT resolution notes generation
-   OT incident summarization

**Note:** The incident summarization is applicable only for incidents in the New, In progress, On-hold, Resolved, or Closed states as long as the incident state mappings that are provided in the base system aren't customized.


</td></tr></tbody>
</table>## Procedure

1.  Activate the ServiceNow Otto for OT Service Management plugin \(sn\_otsm\_gen\_ai\).

    -   For information about the application dependencies, see [Supporting information for ServiceNow Otto for Operational Technology \(OT\) Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/operational-technology/operational-technology-incident-management/supporting-information-for-now-assist-otsm.md).
    -   For information about the installation process, see [Install plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/install-now-assist-feature-plugins.md).
2.  Navigate to **All** &gt; **AI Admin Hub**.

3.  Select the **AI Skills** tab.

4.  Activate and configure the skills for the ServiceNow Otto for OT Service Management features.

    These features are grouped under the **Technology** workflow group. Each feature has its associated skills.

5.  On the tile for your skill, select **Activate skill**.

6.  Select the inputs or triggers for the selected skill.

    For information about the inputs and triggers for each skill, see [Skill inputs and triggers for ServiceNow Otto for Operational Technology \(OT\) Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/operational-technology/operational-technology-incident-management/skill-inputs-and-triggers-for-now-assist-for-operational-technology-service-management-otsm.md).

7.  After you configure the inputs or triggers, select **Save and continue**.

    You can return to a previous step by using the **Back** button.

8.  Define access as needed to determine who can access the selected skill.

    **Note:** For both the OT incident summarization skill and the OT incident resolution notes generation skill, a user must have the sn\_ot\_incident\_write role.

9.  After you configure the access controls, select **Save and continue**.

10. Select where to display the skill.

    -   **In-product**: When selected, the AI skills are displayed on forms and workspaces.
    -   **ServiceNow Otto panel**: When selected, the AI skills are available in the ServiceNowOtto panel. If you don't see this option, you must activate the panel. For more information, see [Activate the panel in standard chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/activate-now-assist-panel.md).
11. After you configure the display for the selected skill, select **Save and continue** to go to the next step.

12. Review your choices and select **Activate** to complete the configuration.


-   **[Supporting information for ServiceNow Otto for Operational Technology \(OT\) Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/operational-technology/operational-technology-incident-management/supporting-information-for-now-assist-otsm.md)**  
Review the supported language models, supported interfaces, and application dependencies for ServiceNow Otto for Operational Technology \(OT\) Service Management.
-   **[Skill inputs and triggers for ServiceNow Otto for Operational Technology \(OT\) Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/operational-technology/operational-technology-incident-management/skill-inputs-and-triggers-for-now-assist-for-operational-technology-service-management-otsm.md)**  
Skill inputs and triggers for ServiceNow Otto for Operational Technology \(OT\) Service Management determine how and when each skill is used. Configure inputs to identify the data a skill uses, or configure triggers to initiate skill actions.

**Parent Topic:**[Configuring Operational Technology Incident Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/operational-technology/operational-technology-incident-management/configuring-operational-technology-incident-mgt.md)

