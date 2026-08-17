---
title: Customize a KB generation skill in ServiceNow Otto for Field Service Management \(FSM\)
description: As an admin, you can clone the KB generation skill and customize the input fields.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/field-service-management/now-assist-for-field-service-management-fsm/cust-now-assist-fsm-skill.html
release: australia
product: Now Assist for Field Service Management \(FSM\)
classification: now-assist-for-field-service-management-fsm
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Customizing a skill, Configure, ServiceNow Otto for FSM]
---

# Customize a KB generation skill in ServiceNow Otto for Field Service Management \(FSM\)

As an admin, you can clone the KB generation skill and customize the input fields.

## Before you begin

Role required: wm\_admin

## About this task

The out-of-the-box \(OOB\) KB is generated for the following states: Close Complete, Close Incomplete, and Work In Progress. From the AI Admin Hub console, you can duplicate and customize the availability of the KB generation skill.

## Procedure

1.  Navigate to **All** &gt; **AI Admin Hub** &gt; **AI Skills**.

2.  In the product panel, select **FSM** under **Customer**.

    All the skills available for FSM are displayed.

3.  Create a copy of the ServiceNow Otto for FSM KB generation skill and customize the input fields.

    1.  On the KB generation skill feature card, select the more actions icon \[Omitted image "more\_actions.png"\] Alt text:.

    2.  Select **Make a copy**.

        A guided setup leads you through the configuration of the general details, input, availability, display, review, and activation of the customized skill. When you complete the entire walk-through, the skill is activated.

4.  On the **General details** page, fill in the fields.

    1.  Enter a name and description for the skill.

    2.  Select **Save and continue**.

5.  Select the **Choose input** tab to choose the table record and input fields.

    1.  Select the **Default Knowledge Base for ServiceNow Otto panel**.

    2.  Select **Save and continue**.

6.  Select the **Define availability** tab to configure how the skill must available to users.

    1.  Select if the skill must be always available or customize its availability.

        Selecting **Customize skill availability** displays a condition builder to filter the data further.

    2.  Select **Save and continue**.

7.  Select the **Select display** tab.

    1.  Select either **In-product**, or **Servicenow Otto panel**.

        -   **In-product**: When selected, the ServiceNow Otto KB generation skill is displayed on the forms and workspaces.

            For the skill to appear in the product, select the down arrow to identify the roles that can use the skill. The only supported roles are `wm_manager` and `wm_dispatcher`.

        -   **ServiceNow Otto panel**: When selected, the ServiceNow Otto KB generation skill is available in the ServiceNow Otto panel.

            For the skill to appear in the ServiceNow Otto panel, select the down arrow to identify the roles that can use the skill. The only supported roles are `wm_manager` and `wm_dispatcher`.

    2.  Select **Save and continue**.

8.  In the **Review and activate** page, review your choices and select **Done** to complete the skill customization.


