---
title: Configuring the KB generation skill
description: Configure the KB generation skill that agents can use to draft a knowledge article with Now Assist.
locale: en-US
release: australia
product: Now Assist in Knowledge Management
classification: now-assist-in-knowledge-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure Now Assist in Knowledge Management, Now Assist in Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configuring the KB generation skill

Configure the KB generation skill that agents can use to draft a knowledge article with Now Assist.

## Before you begin

Before configuring the KB generation skill, the following applications and their respective plugins must be installed.

-   The latest Now Assist in Knowledge Management and Knowledge Capabilities in UI Builder store apps must be installed prior to the following configuration steps.

-   For ServiceNow Store installation steps, see [Install a ServiceNow Store application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/application-manager/installing-applications-in-application-manager.md).

    **Note:** You can access knowledge articles created with TinyMCE by enabling KB generation skill, see [Configuring the KB generation skill](Now-Assist-configuring-km-skills.md). To use articles created with custom instructions, please activate the knowledge content recommendation skill, see [Edit an article using the Now Assist context menu](Now-Assist-generate-article-using-context-menu.md#).


Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Now Assist Skills**.

2.  Select the application that you want to configure the KB generation skills for.

3.  Select the Knowledge feature from the features drop-down.

4.  Select **Activate skill** on the feature card.

5.  Review the values in the Choose input window, then select **Save and Continue**.

    Review the read-only fields for more information.

    -   **Input Table**: The record type used for KB generation. For example, the value is **case** for Now Assist for CSM.
    -   **Input Fields**: The fields from which information is gathered to draft the Knowledge article. Based on the Input Table, the Input Fields can be configured. Together, they serve as an input to Now LLM Service from the case or incident where the article is created.
    -   **Default Knowledge Base for NAP**: The Knowledge Base in which the Now Assist panel generates the article.
    ![Choose the table records and input fields to generate a knowledge article.](../image/NAConfig_Chooseinput.png)

6.  Configure whether the KB generation skill should always be available or available based on a set of conditions. ![Customize the skill availability for the KB generation skill.](../image/NAConfig_DefineAvailability.png)

7.  Select where you want to display the KB generation skill.

    You can select In-product, Now Assist panel, or both.

    -   **In-product**: When selected, Now Assist skills are displayed on forms and workspaces. Select the arrow next to the toggle switch to define the roles that can use this skill in-product.
    -   **Now Assist panel**: When selected, Now Assist skills are available in the Now Assist panel. Select the arrow next to the toggle switch to define roles that can use this skill in the Now Assist panel.
    ![Select where the KB generation skill is displayed.](../image/NAConfig_Selectdisplay.png)

8.  Select **Save and continue** to go to the next step.

9.  Review your choices and select **Activate** to complete the configuration.


## Result

Your skill is configured.

**Parent Topic:**[Configuring Now Assist in Knowledge Management](../concept/configuring-now-assist-km.md)

**Related topics**  


[Additional skill input and trigger information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/now-assist-for-csm/additional-skill-input-and-trigger-information-for-now-assist_0.md)

[Skill inputs and triggers for Now Assist for IT Service Management \(ITSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/now-assist-for-it-service-management-itsm/now-assist-itsm-skills.md)

[Skill inputs and triggers for Now Assist for HRSD](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/now-assist-for-hrsd/now-assist-hrsd-skill-inputs.md)

[Skill inputs for Now Assist for Field Service Management \(FSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/now-assist-for-field-service-management-fsm/now-assist-fsm-skill-inputs.md)

