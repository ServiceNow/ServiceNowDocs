---
title: Customize an FSM KB generation skill in AI Admin Hub
description: As an admin, you can clone the KB generation skill and customize the input fields.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/field-service-management/work-order-management/cust-now-assist-fsm-skill.html
release: brazil
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Customizing a skill, Configure, Set up work orders and tasks, Configure, Field Service Management]
---

# Customize an FSM KB generation skill in AI Admin Hub

As an admin, you can clone the KB generation skill and customize the input fields.

## Before you begin

Role required: wm\_admin

## About this task

The out-of-the-box \(OOB\) KB is generated for the following states: Close Complete, Close Incomplete, and Work In Progress. From the AI Admin Hub console, you can duplicate and customize the availability of the KB generation skill.

## Procedure

1.  Navigate to **All** &gt; **AI Admin Hub** &gt; **Skills**.

2.  In the **Customer** workflow group, select **FSM** to view the skills for the ServiceNow Otto for FSM features.

3.  Create a copy of the ServiceNow Otto for FSM KB generation skill and customize the input fields.

    1.  On the KB generation skill feature card, select the more actions icon \[Omitted image "more\_actions.png"\] Alt text:.

    2.  Select **Make a copy**.

        A guided setup leads you through the configuration of the general details, input, availability, display, review, and activation of the customized skill. When you complete the entire walk-through, the skill is activated.

4.  In the General details step, fill in the fields.

    1.  Enter a name and description for the skill.

    2.  Select **Save and continue** to go to the next step.

5.  View the input data.

    1.  The table record and input fields are read-only.

    2.  Select the **Default Knowledge Base for Servicenow Otto panel**.

    3.  Select **Save and continue**.

6.  Define how the skill is available to your users.

    1.  Configure the skill to be available to users, or select conditions that must be met before the skill is available.

        Selecting **Customize skill availability** displays a condition builder to filter the data further.

    2.  Select **Save and continue** to go to the next step.

7.  Configure where to display the KB generation.

    1.  Select either **In-product**, or **Now Assist panel**.

        -   **In-product**: When selected, the Now Assist KB generation skill is displayed on the forms and workspaces.

            For the skill to appear in the product, select the down arrow to identify the roles that can use the skill. The only supported roles are `wm_manager` and `wm_dispatcher`.

        -   **Servicenow Otto panel**: When selected, the ServiceNow Otto for FSM KB generation skill is available in the ServiceNow Otto® panel.

            For the skill to appear in the AI Admin Hub panel, select the down arrow to identify the roles that can use the skill. The only supported roles are `wm_manager` and `wm_dispatcher`.

    2.  Select **Save and continue** to go to the next step.

8.  Review and activate the skill.

    Review your choices and select **Activate** to complete the skill customization.


