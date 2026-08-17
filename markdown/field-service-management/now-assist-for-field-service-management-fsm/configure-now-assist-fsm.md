---
title: Configure ServiceNow Otto for Field Service Management \(FSM\)
description: If you have the admin role, you can configure ServiceNow Otto for Field Service Management \(FSM\) application so that users can generate work order summaries and knowledge articles, or summarize Sidebar discussions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/field-service-management/now-assist-for-field-service-management-fsm/configure-now-assist-fsm.html
release: australia
product: Now Assist for Field Service Management \(FSM\)
classification: now-assist-for-field-service-management-fsm
topic_type: task
last_updated: "2026-05-13"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [ServiceNow Otto for FSM]
---

# Configure ServiceNow Otto for Field Service Management \(FSM\)

If you have the admin role, you can configure ServiceNow Otto for Field Service Management \(FSM\) application so that users can generate work order summaries and knowledge articles, or summarize Sidebar discussions.

## Before you begin

Role required: wm\_admin

## About this task

Use the AI Admin Hub console to configure ServiceNow Otto for FSM. This console contains everything that you need to install the plugins and configure the generative AI skills. For more information, [Overview tab in AI Admin Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configuring-now-assist.md).

The following table lists the features and skills that you can access from the AI Admin Hub console.

|FSM feature|Skills|
|-----------|------|
|Work Order Task|Work Order Task Summarization|
|Knowledge|KB generation|
|Chat|Sidebar summarization|

The ServiceNow large language model \(Now LLM Service\) is currently the only provider for ServiceNow Otto skills.

## Procedure

1.  If necessary, install the ServiceNow Otto for FSM plugin \(sn\_fsm\_gen\_ai\).

    For information about the installation process, see [Install plugins for ServiceNow Otto](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/install-now-assist-feature-plugins.md).

2.  Navigate to **All** &gt; **AI Admin Hub** &gt; **AI Skills**.

3.  In the product panel, select **FSM** under **Customer**.

    All the skills available for FSM are displayed.

4.  On the feature card that is associated with the skill that you would like to activate, select **View details**.

5.  After reviewing the skill details, select **Activate skill** on the skill card.

6.  Select the inputs or triggers for the selected skill.

    For more information about the inputs and triggers for each skill, see [Skill inputs for ServiceNow Otto for Field Service Management \(FSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/now-assist-for-field-service-management-fsm/now-assist-fsm-skill-inputs.md).

7.  After configuring the required fields under the **General details** and **Choose input** tabs, select **Save and continue**.

8.  Select the **Define availability** tab.

    -   Select **Skill is always available** to enable the skill everywhere it is available.
    -   Select **Customize skill availability** to manually set the conditions for when the skill is available.
9.  After configuring skill availability, select **Save and continue**.

10. Select the **Select display** tab.

    -   Select **In-product** to display the skill on the Mobile Agent app.
    -   Select **ServiceNow Otto panel** to display the skill in the ServiceNow Otto panel.
11. After configuring the display for the selected skill, select **Save and continue**.

12. In the **Review and activate** tab, review your choices and select **Done** to complete the configuration.

    Your skill is configured.

13. Configure the Generate closure notes UI actions.

    To complete activation for the work order task summarization skill, you must enable the Generate closure notes UI actions for the Close complete and Close incomplete states. For more information, see [Configure the Generate closure notes UI action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/now-assist-for-field-service-management-fsm/configure-close-ui-actions.md).


**Related topics**  


[Overview tab in AI Admin Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configuring-now-assist.md)

[Configuring AI skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configuring-na-landing.md)

