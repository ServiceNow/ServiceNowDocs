---
title: Configure Now Assist for Operational Technology Service Management \(OTSM\)
description: If you have the admin role, you can configure the Now Assist for Operational Technology Service Management \(OTSM\) application so that teams can use the generative AI capabilities in the Industrial Workspace for their Operational Technology \(OT\) incidents.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Now Assist for OTSM, Operational Technology]
---

# Configure Now Assist for Operational Technology Service Management \(OTSM\)

If you have the admin role, you can configure the Now Assist for Operational Technology Service Management \(OTSM\) application so that teams can use the generative AI capabilities in the Industrial Workspace for their Operational Technology \(OT\) incidents.

## Before you begin

Role required: admin

## About this task

Use the Now Assist Admin console to configure Now Assist for OTSM. This console contains everything that you need to install the plugins and configure the generative AI skills. For additional information, see [Overview tab in Now Assist Admin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configuring-now-assist.md).

**Note:** You can also set up AI Enhanced Recommended Actions for OTSM to use with Now Assist for OTSM. For more information, see [Set up AI Enhanced Recommended Actions for Operational Technology Service Management \(OTSM\)](../../ot-ai-enhanced-recommended-actions/task/set-up-ai-enhanced-ra-otsm.md).

**Important:** Some Now Assist skills, agents, and agentic workflows are turned on by default. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills/now-assist-skills-on-by-default.md).

The following table lists the features and skills that you can access from the Now Assist Admin console.

<table id="table_nbg_fzk_fdc"><thead><tr><th>

OTSM features

</th><th>

Skills

</th></tr></thead><tbody><tr><td>

Gen AI skills for OT incident

</td><td>

-   OT resolution notes generation
-   OT incident summarization

**Note:** The incident summarization is applicable only for incidents in the New, In progress, On-hold, Resolved, or Closed states as long as the incident state mappings that are provided in the base system aren’t customized.


</td></tr></tbody>
</table>## Procedure

1.  Install the Now Assist for OTSM plugin \(sn\_otsm\_gen\_ai\).

    -   For information about the application dependencies, see [Supporting information for Now Assist for Operational Technology Service Management \(OTSM\)](supporting-information-for-now-assist-otsm.md).
    -   For information about the installation process, see [Install Now Assist plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/install-now-assist-feature-plugins.md).
2.  Navigate to **All** &gt; **Now Assist Admin**.

3.  Select the **Now Assist Skills** tab.

4.  Activate and configure the skills for the Now Assist for OTSM features.

    These features are grouped under the **Technology** workflow group. Each feature has its associated skills.

5.  On the tile for your skill, select **Activate skill**.

6.  Select the inputs or triggers for the selected skill.

    For information about the inputs and triggers for each skill, see [Skill inputs and triggers for Now Assist for Operational Technology Service Management \(OTSM\)](skill-inputs-and-triggers-for-now-assist-for-operational-technology-service-management-otsm.md).

7.  After you configure the inputs or triggers for the selected skill, select **Save and continue** to go to the next step.

    You can return to a previous step by using the **Back** button.

8.  Define access as needed to determine who can access the selected skill.

    **Note:** For both the OT incident summarization skill and the OT incident resolution notes generation skill, a user must have the **sn\_ot\_incident\_write** role.

9.  After you configure the access controls, select **Save and continue** to go to the next step.

10. Select where you'd like to display the skill.

    -   **In-product**: When selected, the Now Assist skills are displayed on forms and workspaces.
    -   **Now Assist panel**: When selected, the Now Assist skills are available in the Now Assist panel. If you don't see this option, you must activate the Now Assist panel. For more information, see [Activate the Now Assist panel standard chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/activate-now-assist-panel.md).
11. After you configure the display for the selected skill, select **Save and continue** to go to the next step.

12. Review your choices and select **Activate** to complete the configuration.

    Your skill is configured.


-   **[Supporting information for Now Assist for Operational Technology Service Management \(OTSM\)](supporting-information-for-now-assist-otsm.md)**  
Get a quick overview of the important information that is related to the Now Assist for Operational Technology Service Management \(OTSM\) application.
-   **[Skill inputs and triggers for Now Assist for Operational Technology Service Management \(OTSM\)](skill-inputs-and-triggers-for-now-assist-for-operational-technology-service-management-otsm.md)**  
Get a quick overview of the skill inputs and triggers for Now Assist for Operational Technology Service Management \(OTSM\). By configuring the inputs or triggers for a skill, you can determine how and when a skill is used.

**Parent Topic:**[Now Assist for Operational Technology Service Management \(OTSM\)](now-assist-for-operational-technology-service-management.md)

**Related topics**  


[Overview tab in Now Assist Admin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configuring-now-assist.md)

[Configuring Now Assist Admin features](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configuring-na-landing.md)

