---
title: Configure the KB generation skill
description: Configure the KB generation skill that agents can use to draft a knowledge article with ServiceNow Otto.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/field-service-management/now-assist-for-field-service-management-fsm/configure-the-kb-generation-skill.html
release: australia
product: Now Assist for Field Service Management \(FSM\)
classification: now-assist-for-field-service-management-fsm
topic_type: task
last_updated: "2026-08-17"
reading_time_minutes: 1
breadcrumb: [Configure, ServiceNow Otto for FSM]
---

# Configure the KB generation skill

Configure the KB generation skill that agents can use to draft a knowledge article with ServiceNow Otto.

## Before you begin

Role required: wm\_admin

## About this task

Agents can generate knowledge articles for work orders in a closed complete or closed incomplete state, by configuring the KB generation skill. To enable the configuration, activate the ServiceNow Otto panel, FSM knowledge skill, and ServiceNow Otto for Platform knowledge skills.

## Procedure

1.  Navigate to **All** &gt; **AI Admin Hub** &gt; **AI Experiences** to access the **ServiceNow Otto panel** tab of the AI Admin Hub console.

2.  In the summary section, select **Turn on**.

3.  Navigate to **AI Admin Hub** &gt; **AI Skills** tab.

4.  Select **FSM** under the **Customer** tab.

5.  On the **KB generation** skill card, select **View details**.

6.  On the **KB generation** skill card, select **Activate skill**.

7.  After configuring the required fields under the **General details** and **Choose input** tabs, select **Save and continue**.

8.  Select the **Define availability** tab.

    -   Select **Skill is always available** to enable the skill everywhere it is available.
    -   Select **Customize skill availability** to manually set the conditions for when the skill is available.
9.  After configuring skill availability, select **Save and continue**.

10. Select the **Select display** tab.

    You can select In-product, ServiceNow Otto panel, or both.

    -   **In-product**: When selected, ServiceNow Otto skills are displayed on forms and Workspaces. Select the arrow next to the toggle switch to define the roles that can use this skill in-product.
    -   **Servicenow Otto panel**: When selected, the ServiceNow Otto skills are available in the ServiceNow Otto panel. Select the arrow next to the toggle switch to define roles that can use this skill in the ServiceNow Otto panel.

        **Note:** If you don't see the ServiceNow Otto panel toggle, go back to step 1 to enable it.\[Omitted image "KBskill.png"\] Alt text: Configuring display option for the KB generation skill

11. Select **Save and continue**.

12. Review your choices and select **Activate**.

13. Return to the **AI Skills** page.

14. Select **Knowledge** under the **Platform** tab.

15. On the required Knowledge skill card, select **View details**.\[Omitted image "KBPlatform.png"\] Alt text: Turn on the KB generation skill

16. On the required Knowledge skill card, select **Turn on**.

    The **Activate skill** option is displayed on a skill card when it's details aren't configured.

17. In the selected Knowledge skill page, review and modify its access permissions.

18. Select **Turn on**.


