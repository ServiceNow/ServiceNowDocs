---
title: Configure ServiceNow Otto for Field Service Management \(FSM\)
description: If you have the admin role, you can configure ServiceNow Otto for Field Service Management \(FSM\) application so that users can generate work order summaries and knowledge articles, or summarize Sidebar discussions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/field-service-management/work-order-management/configure-now-assist-fsm.html
release: brazil
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Set up work orders and tasks, Configure, Field Service Management]
---

# Configure ServiceNow Otto for Field Service Management \(FSM\)

If you have the admin role, you can configure ServiceNow Otto for Field Service Management \(FSM\) application so that users can generate work order summaries and knowledge articles, or summarize Sidebar discussions.

## Before you begin

Role required: wm\_admin

## About this task

Use the AI Admin Hub console to configure ServiceNow Otto for FSM. This console contains everything that you need to install the plugins and configure the generative AI skills. For more information, [Overview tab in AI Admin Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/configuring-now-assist.md).

The following table lists the features and skills that you can access from the AI Admin Hub console.

|FSM feature|Skills|
|-----------|------|
|Work Order Task|Work Order Task Summarization|
|Knowledge|KB generation|
|Chat|Sidebar summarization|

The ServiceNow® large language model \(Now LLM Service\) is currently the only provider for ServiceNow Otto for FSM skills.

## Procedure

1.  If necessary, install the ServiceNow Otto for FSM plugin \(sn\_fsm\_gen\_ai\).

    For information about the installation process, see [Install Now Assist plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/install-now-assist-feature-plugins.md).

2.  Navigate to **All** &gt; **AI Admin hub** &gt; **Skills**.

3.  In the Customer dropdown, select **FSM**.

4.  Activate and configure the skills for the ServiceNow Otto for FSM features.

    These features are grouped under the **Customer** workflow group. Each feature has its associated skills.

5.  On the feature card that is associated with the skill that you would like to activate, select **View details**.

6.  In the All available skills section, select **Activate skill**.

7.  Select the inputs or triggers for the selected skill.

    For information about the inputs and triggers for each skill, see [Skill inputs for ServiceNow Otto for Field Service Management \(FSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/field-service-management/work-order-management/now-assist-fsm-skill-inputs.md).

8.  After you've configured the inputs or triggers for the selected skill, select **Save and continue** to go to the next step.

    You can return to a previous step by using the **Back** button.

9.  Define the availability of the skill.

    -   Select **Skill is always available** to enable the skill everywhere it is available.
    -   Select **Customize skill availability** to manually set the conditions for when the skill is available.
10. After you configure skill availability, select **Save and continue** to go to the next step.

11. Select where you would like to display the skill.

    -   Select **In-product** to display the skill on the Mobile Agent app.
    -   Select **ServiceNow Otto panel** to display the skill in the ServiceNow Otto panel.
12. After you configure the display for the selected skill, select **Save and continue** to go to the next step.

13. Review your choices and select **Activate** to complete the configuration.

    Your skill is configured.

14. Configure the Generate closure notes UI actions.

    To complete activation for the work order task summarization skill, you must enable the Generate closure notes UI actions for the Close complete and Close incomplete states. For more information, see [Configure the Generate closure notes UI action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/field-service-management/work-order-management/configure-close-ui-actions.md).


**Related topics**  


[Overview tab in AI Admin Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/configuring-now-assist.md)

[Configuring Now Assist Admin features](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/configuring-na-landing.md)

