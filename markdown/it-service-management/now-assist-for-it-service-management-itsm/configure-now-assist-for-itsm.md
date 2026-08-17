---
title: Configure ServiceNow Otto for IT Service Management \(ITSM\)
description: If you have the admin role, you can configure the ServiceNow Otto for IT Service Management \(ITSM\) application so that agents can use the generative AI capabilities in Service Operations Workspace for ITSM and in Core UI.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/now-assist-for-it-service-management-itsm/configure-now-assist-for-itsm.html
release: australia
product: Now Assist for IT Service Management \(ITSM\)
classification: now-assist-for-it-service-management-itsm
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [Now Assist, Agentic AI, generative AI, Gen AI]
breadcrumb: [ServiceNow Otto for IT Service Management \(ITSM\), IT Service Management]
---

# Configure ServiceNow Otto for IT Service Management \(ITSM\)

If you have the admin role, you can configure the ServiceNow Otto for IT Service Management \(ITSM\) application so that agents can use the generative AI capabilities in Service Operations Workspace for ITSM and in Core UI.

## Before you begin

Role required: admin

## About this task

Use the ServiceNow Otto Admin console to configure ServiceNow Otto for IT Service Management \(ITSM\). This console contains everything that you need to install the plugins and configure the generative AI skills. For additional information, see [Overview tab in AI Admin Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configuring-now-assist.md). For the list of all skills supported in ServiceNow Otto for IT Service Management \(ITSM\), see [Using ServiceNow Otto for IT Service Management \(ITSM\) Generative AI skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/now-assist-for-it-service-management-itsm/using-now-assist-for-itsm.md).

Domain separation is supported in ServiceNow Otto for IT Service Management \(ITSM\). For details, see [Domain separation in the AI Admin Hub console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/domain-separation-in-the-now-assist-admin-console.md).

**Note:** Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents. For more information, see [ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-native-sku-overview.md).

## Procedure

1.  Install the ServiceNow Otto for IT Service Management \(ITSM\) \(sn\_itsm\_gen\_ai\).

    -   For information about the application dependencies, see [Supporting information for ServiceNow Otto for IT Service Management \(ITSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/now-assist-for-it-service-management-itsm/supporting-information-now-assist-itsm.md).
    -   For information about the installation process, see [Install plugins for ServiceNow Otto](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/install-now-assist-feature-plugins.md).
2.  Navigate to **Admin** &gt; **AI Admin Hub**.

3.  Select the **AI Skills** tab.

4.  Activate and configure the skills for the ServiceNow Otto for ITSM features.

    These features are grouped under the **Technology** workflow group. Each feature has its associated skills.

5.  On the tile for your skill, select **Activate skill**.

6.  Select the inputs or triggers for the selected skill.

    For information about the inputs and triggers for each skill, see [Skill inputs and triggers for ServiceNow Otto for IT Service Management \(ITSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/now-assist-for-it-service-management-itsm/now-assist-itsm-skills.md).

    \[Omitted image "now-assist-itsm-triggers.png"\] Alt text: Example Define trigger screen for the Chat summarization skill.

7.  After you've configured the inputs or triggers for the selected skill, select **Save and continue** to go to the next step.

    You can return to a previous step by using the **Back** button.

8.  Select where you'd like to display the skill.

9.  After you've configured the display for the selected skill, select **Save and continue** to go to the next step.

10. Review your choices and select **Activate** to complete the configuration.

    Your skill is configured.


**Related topics**  


[Overview tab in AI Admin Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configuring-now-assist.md)

[Configuring AI skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configuring-na-landing.md)

