---
title: Configuring the KB generation skill
description: Configure the KB generation skill that agents can use to draft a knowledge article with Now Assist.
locale: en-US
release: yokohama
product: Now Assist in Knowledge Management
classification: now-assist-in-knowledge-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configure Now Assist in Knowledge Management, Now Assist in Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configuring the KB generation skill

Configure the KB generation skill that agents can use to draft a knowledge article with Now Assist.

## Before you begin

Before configuring the KB generation skill, the following applications and their respective plugins must be installed.

-   The latest Now Assist in Knowledge Management and Knowledge Capabilities in UI Builder store apps must be installed prior to the following configuration steps.

-   For ServiceNow Store installation steps, see [Install a ServiceNow Store application](https://www.servicenow.com/docs/access?context=t_InstallApplications&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

    **Note:** You can access knowledge articles created with TinyMCE by enabling KB generation skill, see [Configuring the KB generation skill](Now-Assist-configuring-km-skills.md). To use articles created with custom instructions, please activate the knowledge content recommendation skill, see [Edit an article using the Now Assist context menu](Now-Assist-generate-article-using-context-menu.md#).


Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Features**.

2.  Select the application that you want to configure the KB generation skills for.

3.  On the **Knowledge** feature card, select **View details**.

4.  In the Activate Skills section, select the more actions icon \(![More actions icon.](../../../administer/conversational-interfaces/image/more-options-icon.png)\), then select **Edit** to open the skill configuration window for KB generation.

5.  Review the values in the Choose input window, then select **Save and Continue**.

    Review the read-only fields for more information.

    -   **Input Table**: The record type used for KB generation. For example, the value is **case** for Now Assist for CSM.
    -   **Input Fields**: The fields from which information is gathered to draft the Knowledge article. Based on the Input Table, the Input Fields can be configured. Together, they serve as an input to Now LLM Service from the case or incident where the article is created.
    -   **Default Knowledge Base for Now Assist panel**: The Knowledge Base in which the Now Assist panel generates the article.
    ![Choose the table records and input fields to generate a knowledge article.](../image/NAConfig_Chooseinput.png)

6.  Configure whether the KB generation skill should always be available or available based on a set of conditions. ![Customize the skill availability for the KB generation skill.](../image/NAConfig_DefineAvailability.png)

7.  Select where you want to display the KB generation skill.

    You can select In-product, Now Assist panel, or both.

    -   **In-product**: When selected, Now Assist skills are displayed on forms and workspaces. Select the arrow next to the toggle switch to define the roles that can use this skill in-product.
    -   **Now Assist panel**: When selected, Now Assist skills are available in the Now Assist panel. Select the arrow next to the toggle switch to define roles that can use this skill in the Now Assist panel.
    ![Select where the KB generation skill is displayed.](../image/NAConfig_Selectdisplay.png)

8.  Select **Save and continue** to go to the next step.

9.  Review your choices and select **Activate** to complete the configuration. ![Review your configuration choices to activate the KB generation skill.](../image/NAConfig_Review.png)


## Result

Your skill is configured.

**Parent Topic:**[Configuring Now Assist in Knowledge Management](../concept/configuring-now-assist-km.md)

**Related topics**  


[Skill inputs and triggers for Now Assist for IT Service Management \(ITSM\)](https://www.servicenow.com/docs/access?context=now-assist-itsm-skills&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)

[Skill inputs and triggers for Now Assist for HR Service Delivery \(HRSD\)](https://www.servicenow.com/docs/access?context=now-assist-hrsd-skill-inputs&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)

[Skill inputs for Now Assist for Field Service Management \(FSM\)](https://www.servicenow.com/docs/access?context=now-assist-fsm-skill-inputs&version=yokohama&pubname=yokohama-field-service-management&ft:locale=en-US)

