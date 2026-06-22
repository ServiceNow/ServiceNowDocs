---
title: Configuring the KB generation skill
description: Configure the KB generation skill that agents can use to draft a knowledge article with Now Assist.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/servicenow-platform/now-assist-in-knowledge-management/Now-Assist-configuring-km-skills.html
release: xanadu
product: Now Assist in Knowledge Management
classification: now-assist-in-knowledge-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configure Now Assist in Knowledge Management, Now Assist in Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configuring the KB generation skill

Configure the KB generation skill that agents can use to draft a knowledge article with Now Assist.

## Before you begin

Before configuring the KB generation skill, the following applications and their respective plugins must be installed.

-   The latest Now Assist in Knowledge Management and Knowledge Capabilities in UI Builder store apps must be installed prior to the following configuration steps.

-   For ServiceNow Store installation steps, see [Install a ServiceNow Store application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/platform-administration/t_InstallApplications.md).


Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Features**.

2.  Select the application that you want to configure the KB generation skills for.

3.  On the **Knowledge** feature card, select **View details**.

4.  In the Activate Skills section, select the more actions icon \(\[Omitted image "more-options-icon.png"\] Alt text: More actions icon.\), then select **Edit** to open the skill configuration window for KB generation.

5.  Review the values in the Choose input window, then select **Save and Continue**.

    Review the read-only fields for more information.

    -   **Input Table**: The record type used for KB generation. For example, the value is **case** for Now Assist for CSM.
    -   **Input Fields**: The fields from which information is gathered to draft the Knowledge article. Based on the Input Table, the Input Fields can be configured. Together, they serve as an input to Now LLM Service from the case or incident where the article is created.
    -   **Default Knowledge Base for Now Assist panel**: The Knowledge Base in which the Now Assist panel generates the article.
    \[Omitted image "NAConfig\_Chooseinput.png"\] Alt text: Choose the table records and input fields to generate a knowledge article.

6.  Configure whether the KB generation skill should always be available or available based on a set of conditions. \[Omitted image "NAConfig\_DefineAvailability.png"\] Alt text: Customize the skill availability for the KB generation skill.

7.  Select where you want to display the KB generation skill.

    You can select In-product, Now Assist panel, or both.

    -   **In-product**: When selected, Now Assist skills are displayed on forms and workspaces. Select the arrow next to the toggle switch to define the roles that can use this skill in-product.
    -   **Now Assist panel**: When selected, Now Assist skills are available in the Now Assist panel. Select the arrow next to the toggle switch to define roles that can use this skill in the Now Assist panel.
    \[Omitted image "NAConfig\_Selectdisplay.png"\] Alt text: Select where the KB generation skill is displayed.

8.  Select **Save and continue** to go to the next step.

9.  Review your choices and select **Activate** to complete the configuration. \[Omitted image "NAConfig\_Review.png"\] Alt text: Review your configuration choices to activate the KB generation skill.


## Result

Your skill is configured.

-   **[Configure skill for Now Assist context menu](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/servicenow-platform/now-assist-in-knowledge-management/Now-Assist-configuring-context-menu-skill.md)**  
Configure the knowledge content management skill to enable agents to utilize the Now Assist context menu to elaborate or shorten a Knowledge article.

**Parent Topic:**[Configuring Now Assist in Knowledge Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/servicenow-platform/now-assist-in-knowledge-management/configuring-now-assist-km.md)

**Related topics**  


[Skill inputs and triggers for Now Assist for Customer Service Management \(CSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/customer-service-management/now-assist-for-csm/now-assist-csm-skill-inputs.md)

[Skill inputs and triggers for Now Assist for IT Service Management \(ITSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/it-service-management/now-assist-for-it-service-management-itsm/now-assist-itsm-skills.md)

[Skill inputs and triggers for Now Assist for HR Service Delivery \(HRSD\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/employee-service-management/now-assist-for-hrsd/now-assist-hrsd-skill-inputs.md)

[Skill inputs for Now Assist for Field Service Management \(FSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/field-service-management/now-assist-for-field-service-management-fsm/now-assist-fsm-skill-inputs.md)

