---
title: Configure Now Assist for Field Service Management \(FSM\)
description: If you have the admin role, you can configure Now Assist for Field Service Management \(FSM\) application so that users can generate work order summaries and knowledge articles, or summarize Sidebar discussions.
locale: en-US
release: xanadu
product: Now Assist for Field Service Management \(FSM\)
classification: now-assist-for-field-service-management-fsm
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Now Assist for Field Service Management \(FSM\)]
---

# Configure Now Assist for Field Service Management \(FSM\)

If you have the admin role, you can configure Now Assist for Field Service Management \(FSM\) application so that users can generate work order summaries and knowledge articles, or summarize Sidebar discussions.

## Before you begin

Role required: wm\_admin

## About this task

Use the Now Assist Admin console to configure Now Assist for FSM. This console contains everything that you need to install the plugins and configure the generative AI skills. For more information, [Now Assist Admin console](https://www.servicenow.com/docs/access?context=configuring-now-assist&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).

The following table lists the features and skills that you can access from the Now Assist Admin console.

|FSM feature|Skills|
|-----------|------|
|Work Order Task|Work Order Task Summarization|
|Knowledge|KB generation|
|Chat|Sidebar summarization|

The ServiceNow® large language model \(Now LLM Service\) is currently the only provider for this Now Assist application's skills.

## Procedure

1.  If necessary, install the Now Assist for FSM plugin \(sn\_fsm\_gen\_ai\).

    For information about the installation process, see [Install Now Assist plugins](https://www.servicenow.com/docs/access?context=install-now-assist-feature-plugins&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).

2.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Features** to access the **Features** tab of the Now Assist Admin console.

3.  In the Select product field, select **FSM**.

4.  Activate and configure the skills for the Now Assist for FSM features.

    These features are grouped under the **Customer** workflow group. Each feature has its associated skills.

5.  On the feature card that is associated with the skill that you would like to activate, select **View details**.

6.  In the All available skills section, select **Activate skill**.

7.  Select the inputs or triggers for the selected skill.

    For information about the inputs and triggers for each skill, see [Skill inputs for Now Assist for Field Service Management \(FSM\)](../concept/now-assist-fsm-skill-inputs.md).

8.  After you've configured the inputs or triggers for the selected skill, select **Save and continue** to go to the next step.

    You can return to a previous step by using the **Back** button.

9.  Define the availability of the skill.

    -   Select **Skill is always available** to enable the skill everywhere it is available.
    -   Select **Customize skill availability** to manually set the conditions for when the skill is available.
10. After you configure skill availability, select **Save and continue** to go to the next step.

11. Select where you would like to display the skill.

    -   Select **In-product** to display the skill on the Mobile Agent app.
    -   Select **Now Assist panel** to display the skill in the Now Assist panel.
12. After you configure the display for the selected skill, select **Save and continue** to go to the next step.

13. Review your choices and select **Activate** to complete the configuration.

    Your skill is configured.

14. Configure the Generate closure notes UI actions.

    To complete activation for the work order task summarization skill, you must enable the Generate closure notes UI actions for the Close complete and Close incomplete states. For more information, see [Configure the Generate closure notes UI action](configure-close-ui-actions.md).


**Related topics**  


[Now Assist Admin console](https://www.servicenow.com/docs/access?context=configuring-now-assist&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)

[Configuring Now Assist settings and features](https://www.servicenow.com/docs/access?context=configuring-na-landing&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)

