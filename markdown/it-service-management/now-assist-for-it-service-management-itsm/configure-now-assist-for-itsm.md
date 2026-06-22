---
title: Configure Now Assist for IT Service Management \(ITSM\)
description: If you have the admin role, you can configure the Now Assist for IT Service Management \(ITSM\) application so that agents can use the generative AI capabilities in Service Operations Workspace for ITSM and in Core UI.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-service-management/now-assist-for-it-service-management-itsm/configure-now-assist-for-itsm.html
release: zurich
product: Now Assist for IT Service Management \(ITSM\)
classification: now-assist-for-it-service-management-itsm
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
keywords: [Now Assist, Agentic AI, generative AI, Gen AI]
breadcrumb: [Now Assist for IT Service Management \(ITSM\), IT Service Management]
---

# Configure Now Assist for IT Service Management \(ITSM\)

If you have the admin role, you can configure the Now Assist for IT Service Management \(ITSM\) application so that agents can use the generative AI capabilities in Service Operations Workspace for ITSM and in Core UI.

## Before you begin

Role required: admin

## About this task

Use the Now Assist Admin console to configure Now Assist for IT Service Management \(ITSM\). This console contains everything that you need to install the plugins and configure the generative AI skills. For additional information, see [Overview tab in Now Assist Admin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/enable-ai-experiences/configuring-now-assist.md).

Domain separation is supported in Now Assist for IT Service Management \(ITSM\). For details, see [Domain separation in the Now Assist Admin console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/enable-ai-experiences/domain-separation-in-the-now-assist-admin-console.md). For information on Domain separation for the generative AI skills, see [Using Now Assist for IT Service Management \(ITSM\) Generative AI skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/now-assist-for-it-service-management-itsm/using-now-assist-for-itsm.md).

Here's a list of all skills supported in Now Assist for IT Service Management \(ITSM\):

-   Chat summarization
-   Sidebar discussion summarization
-   Chat reply recommendation
-   Incident assist
-   Incident summarization

    **Note:** The incident summarization is applicable only for incidents in the New, In progress, On-hold, and Resolved states as long as the incident state mappings that are provided in the base system aren’t customized.

-   Resolution notes generation
-   Email reply recommendation
-   Knowledge article generation
-   Change request risk explanation
-   Change request summarization

    **Note:** The change request summarization is applicable only for change requests in the Assess, Authorize, Scheduled, Implement, Review, and Closed states as long as the change request state mappings that are provided in the base system aren’t customized.

-   Major Incident email content recommendation

## Procedure

1.  Install the Now Assist for IT Service Management plugin \(sn\_itsm\_gen\_ai\).

    -   For information about the application dependencies, see [Supporting information for Now Assist for IT Service Management \(ITSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/now-assist-for-it-service-management-itsm/supporting-information-now-assist-itsm.md).
    -   For information about the installation process, see [Install Now Assist plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/enable-ai-experiences/install-now-assist-feature-plugins.md).
2.  Navigate to **Admin** &gt; **Now Assist Admin**.

3.  Select the **Now Assist Skills** tab.

4.  Activate and configure the skills for the Now Assist for ITSM features.

    These features are grouped under the **Technology** workflow group. Each feature has its associated skills.

5.  On the tile for your skill, select **Activate skill**.

6.  Select the inputs or triggers for the selected skill.

    For information about the inputs and triggers for each skill, see [Skill inputs and triggers for Now Assist for IT Service Management \(ITSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/now-assist-for-it-service-management-itsm/now-assist-itsm-skills.md).

    \[Omitted image "now-assist-itsm-triggers.png"\] Alt text: Example Define trigger screen for the Chat summarization skill.

7.  After you've configured the inputs or triggers for the selected skill, select **Save and continue** to go to the next step.

    You can return to a previous step by using the **Back** button.

8.  Select where you'd like to display the skill.

    \[Omitted image "now-assist-itsm-select-roles.png"\] Alt text: Now Assist for ITSM select roles

    -   **In-product**: When selected, the Now Assist skills are displayed on forms and workspaces. For the skills that appear in-product, select the down arrow to identify the roles that can use the skill.
    -   **Now Assist panel**: When selected, the Now Assist skills are available in the Now Assist panel. If you don't see this option, you must activate the Now Assist panel. For more information, see [Activate the Now Assist panel standard chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/enable-ai-experiences/activate-now-assist-panel.md).

        For the skills that appear in the Now Assist panel, select the down arrow to identify the roles that can use the skill.

9.  After you've configured the display for the selected skill, select **Save and continue** to go to the next step.

10. Review your choices and select **Activate** to complete the configuration.

    Your skill is configured.


**Related topics**  


[Overview tab in Now Assist Admin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/enable-ai-experiences/configuring-now-assist.md)

[Configuring Now Assist Admin features](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/enable-ai-experiences/configuring-na-landing.md)

