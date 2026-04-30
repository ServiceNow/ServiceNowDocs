---
title: Configure Now Assist for HR Service Delivery \(HRSD\)
description: If you have the admin role, you can configure the Now Assist for HR Service Delivery \(HRSD\) application so that your agents can use the generative AI capabilities in Agent Workspace for HR Case Management and Core UI.
locale: en-US
release: xanadu
product: Now Assist for HRSD
classification: now-assist-for-hrsd
topic_type: task
last_updated: "2024-08-22"
reading_time_minutes: 4
breadcrumb: [Now Assist for HR Service Delivery \(HRSD\), HR Service Delivery, Employee Service Management]
---

# Configure Now Assist for HR Service Delivery \(HRSD\)

If you have the admin role, you can configure the Now Assist for HR Service Delivery \(HRSD\) application so that your agents can use the generative AI capabilities in Agent Workspace for HR Case Management and Core UI.

## Before you begin

Role required: admin

## About this task

Use the Now Assist Admin console to configure Now Assist for HR Service Delivery \(HRSD\). This console contains everything that you need to install the plugins and configure the generative AI skills. For additional information, see [Now Assist Admin console](https://www.servicenow.com/docs/access?context=configuring-now-assist&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).

The following list contains skills that you can access from the Now Assist Admin console.

-   Chat reply recommendation
-   Chat summarization
-   Sidebar discussion summarization
-   Case summarization
-   Resolution notes generation
-   KB generations
-   Email recommendation
-   Sensitivity detection
-   Journey generation for managers
-   Journey summarization for managers
-   Persona assistant

Now LLM Service is currently the only provider for this Now Assist application's skills.

## Procedure

1.  Install the Now Assist for HR Service Delivery \(HRSD\) plugin \(sn\_hr\_gen\_ai\).

    -   For information about the plugin dependencies and plugin activation order, see [Supporting information for Now Assist for HR Service Delivery \(HRSD\)](../concept/support-info-hr-assist.md).
    -   For information about the installation process, see [Install Now Assist plugins](https://www.servicenow.com/docs/access?context=install-now-assist-feature-plugins&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).
2.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Skills** to access the **Now Assist Skills** tab of the Now Assist Admin console.

3.  Activate and configure the skills for the Now Assist for HR Service Delivery \(HRSD\) features.

    These features are grouped under the **Employee** workflow group. Each feature has its associated skills.

4.  On the skill that you would like to activate, select **Activate Skill**.

5.  Select the inputs or triggers for the selected skill.

    For information about the inputs and triggers for each skill, see [Skill inputs and triggers for Now Assist for HR Service Delivery \(HRSD\)](../concept/now-assist-hrsd-skill-inputs.md).

6.  After you configure the inputs or triggers for the selected skill, select **Save and continue** to go to the next step.

    You can return to a previous step by using the **Back** button.

7.  Define the availability of skill.

    **Note:** This step applies to the case summarization and resolution notes generation skills. It doesn't apply to the chat summarization skill. If you’re configuring the chat summarization skill, go to Step 10.

8.  After you configure the skill availability, select **Save and continue** to go to the next step.

9.  Select where you would like to display the skill.

    -   **In-product**: When selected, the Now Assist skills are displayed on forms and workspaces.

        For the skills that appear in **In-product**, select the down arrow to identify the roles that can use the skill. The sn\_hr\_core.basic role is available by default.

    -   **Now Assist panel**: When selected, the Now Assist skills are available in the Now Assist panel. If you don't see this option, you must activate the Now Assist panel. For more information, see [Turn on the Now Assist panel](https://www.servicenow.com/docs/access?context=activate-now-assist-panel&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).

        For the skills that appear in the Now Assist panel, select the down arrow to identify the roles that can use the skill.

10. After you configure the display for the selected skill, select **Save and continue** to go to the next step.

11. Review your choices and select **Activate** to complete the configuration.

    Your skill is configured.


-   **[Skill inputs and triggers for Now Assist for HR Service Delivery \(HRSD\)](../concept/now-assist-hrsd-skill-inputs.md)**  
Get a quick overview of the skill inputs and triggers for Now Assist for HR Service Delivery \(HRSD\). By configuring the inputs or triggers for a skill, you can determine how and when a skill is used.
-   **[RCA approvals for Now Assist for HR Service Delivery \(HRSD\)](run-rca-now-assist-hrsd.md)**  
After you install Now Assist for HR Service Delivery \(HRSD\), you might encounter Restricted Caller Access \(RCA\) approval messages requesting for an update in the access request.
-   **[Restrict Now Assist capabilities for employee relations cases](restrict-now-assist-skills-er-cases.md)**  
Restrict the Now Assist capabilities for your employee relations cases and define the availability.
-   **[Configure Gen AI Virtual Agent for HRSD](use-genai-ec.md)**  
Enable your requesters to have a streamlined, conversational experience that is based on generative AI as they submit a catalog item request in Virtual Agent. By offering this generative AI experience, your organization can increase self-service and reduce operating costs.
-   **[Configure the Now Assist for HRSD Virtual Agent topics](config-va-topics.md)**  
Complete the configuration steps to enable your employees place requests to the Human Capital Management \(HCM\) system using the Now Assist for HRSD Virtual Agent topics in Employee Center.
-   **[Configure HCM AI agents from the HR Service Delivery AI Agent Collection](configure-hcm-agents.md)**  
Enable your employees to place requests to the Human Capital Management \(HCM\) system using the Now Assist for HR Service Delivery \(HRSD\) agent collection.
-   **[Configure sensitivity detection in Now Assist for HR Service Delivery \(HRSD\)](config-na-sd-filters.md)**  
Configure sensitivity detection in the Now Assist for HR Service Delivery \(HRSD\) application.

**Parent Topic:**[Now Assist for HR Service Delivery \(HRSD\)](../concept/now-assist-hrsd.md)

**Related topics**  


[Now Assist Admin console](https://www.servicenow.com/docs/access?context=configuring-now-assist&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)

[Configuring Now Assist settings and features](https://www.servicenow.com/docs/access?context=configuring-na-landing&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)

[Record summarization](https://www.servicenow.com/docs/access?context=now-assist-case-summary&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)

[Chat summarization](https://www.servicenow.com/docs/access?context=now-assist-chat-summary&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)

