---
title: Customize a ServiceNow Otto for Field Service Management \(FSM\) work order task summarization skill
description: As an admin you can clone the Work order task summarization skill, then access the skill in the Now Assist skill kit, and update the prompts.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/field-service-management/now-assist-for-field-service-management-fsm/cust-now-assist-fsm-wot-summarization-skill.html
release: australia
product: Now Assist for Field Service Management \(FSM\)
classification: now-assist-for-field-service-management-fsm
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Customizing a skill, Configure, ServiceNow Otto for FSM]
---

# Customize a ServiceNow Otto for Field Service Management \(FSM\) work order task summarization skill

As an admin you can clone the Work order task summarization skill, then access the skill in the Now Assist skill kit, and update the prompts.

## Before you begin

Role required: wm\_admin

## About this task

From the AI Admin Hub console, you can select the input tables, related lists, and fields for each input template of the work order task summarization skill.

## Procedure

1.  Navigate to **Admin** &gt; **AI Admin Hub** &gt; **AI Skills**.

2.  In the product panel, select **FSM** under **Customer**.

    All the skills available for FSM are displayed.

3.  Activate and copy the **Work Order Task Summarization** skill for customization.

    1.  On the skill card, select **View details**.

    2.  On the skill card select **Activate skill**.

    3.  To make a copy of the skill before activating it, select the more actions icon \[Omitted image "more\_actions.png"\] Alt text: and select **Make a copy**.

        The copied skill is displayed in the Active skills section.

    4.  Select the copied skill from the Active skills section to open it.

        A guided setup leads you through the configuration of the general details, input, availability, display, review, and activation of the customized skill. When you complete the entire walk-through, the skill is activated.

4.  In the **General details** tab, fill in the fields.

    For information about the inputs and triggers for each skill, see [Skill inputs for ServiceNow Otto for Field Service Management \(FSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/now-assist-for-field-service-management-fsm/now-assist-fsm-skill-inputs.md).

    1.  Enter a name and description for the skill.

    2.  Select **Save and continue**.

5.  Select the **View input** tab to configure the base input table fields and related lists for the different input templates \(New, Work In Progress, and Closed states\) for the skill.

    Each skill relies on a base input table and input fields with descriptions to provide context for the Now LLM Service to generate a response. Select only those related tables that are offered with the base system as part of the input data.

    1.  To customize the input configurations for each template state, select the required state from the **Template selection** drop-down list.

    2.  For each input template state, select **+New base input field** and configure the base input table fields.

        Add multiple base input fields if more inputs are needed.

        The following table lists the base input table fields and descriptions, including a relevant example.

<table id="table_c53_vp5_dbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Base input field

</td><td>

Field in the Work order task table whose value this skill uses in its response.

 For example, `Short description`.

</td></tr><tr><td>

Field description

</td><td>

Description of the base input field value.

 For example, `Short description of work order task, provides quick info about the work order task.`

</td></tr></tbody>
</table>    3.  For each input template state \(New, WIP, and Closed\), configure the rule conditions by using the condition builder to filter the data further.

        The rule conditions determine when the input template is used. By default, the record state determines the input template that the Now LLM Service uses.

        You can build the condition out further by selecting **+New condition set** and configuring additional parameters.

        The following table lists the input template states.

        |State|Description|
        |-----|-----------|
        |New|State is New.|
        |WIP|State is Work in Progress.|
        |Closed|State is Closed.|

    4.  For each input template state \(New, WIP, and Closed\), select **+New data source** to configure the additional related table, activity streams, and relationships as needed.

        Adding the input data sources, such as the related tables, activity streams, and relationships provides more context to the Now LLM Service.

        You can also add the rule conditions to these additional related table, activity stream, and relationship data sources.

        The following table lists the data sources you can add to the input data.

<table id="table_wc1_wt5_dbc"><thead><tr><th>

Data source

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Related Table

</td><td>

Fields for a related list:

-   Select related input table
-   Related table field
-   Field description
 Configuring the related table fields follows the same format as the base input table fields in the Choose input step.

</td></tr><tr><td>

Activity: Email

</td><td>

Email that is attached to the work order task in the work order task summarization.

</td></tr></tbody>
</table>    5.  Select **Save and continue**.

6.  Select the **Customize prompt** tab.

    Evaluate the prompt utilized for each input template to confirm it meets your expectations. To review and modify the prompt, you can visit the ServiceNow Otto Skill Kit.

    1.  Test the prompt response output format by selecting **Run Test**.

        For each input template state \(New, WIP, and Closed\), select a work order task record in the Test response section.

        The following table lists the mandatory prompt headers.

<table id="table_av3_xhw_2bc"><thead><tr><th>

Input template state

</th><th>

Mandatory prompt header

</th></tr></thead><tbody><tr><td>

New

</td><td>

Issue

</td></tr><tr><td>

Work in progress

</td><td>

-   Issue
-   Key Actions Taken


</td></tr><tr><td>

Closed

</td><td>

-   Issue
-   Key Actions Taken
-   Resolution


</td></tr></tbody>
</table>    2.  Select **Edit prompt in ServiceNow Otto Skill Kit** to make necessary changes to the prompt in the ServiceNow Otto Skill Kit.

    3.  Select **Save and continue**.

7.  Select the **Define availability** tab.

    1.  Select if the skill must be always available or customize its availability.

        Selecting **Customize skill availability** displays a condition builder to filter the data further.

    2.  Select **Save and continue**.

8.  Select the **Select display** tab.

    1.  Select either **In-product**, or **Servicenow Otto panel**.

        -   **In-product**: When selected, ServiceNow Otto skills are displayed in all FSM products \(on forms and in workspaces\).

            To identify the roles that can use the skill, select the down arrow.

        -   **ServiceNow Otto panel**: When selected, ServiceNow Otto skills are available in the ServiceNow Otto panel.

            If you don't see this option, you must activate the ServiceNow Otto panel. For more information, see [Activate the ServiceNow Otto panel standard chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/activate-now-assist-panel.md).

            For the skills that appear in the ServiceNow Otto panel, select the down arrow to identify the roles that can use the skill.

    2.  Select **Save and continue**.

9.  In the **Review and activate** page, review your choices and select **Activate** to complete the skill customization.


## Result

You can now select **Summarize** from a work order task record and generate the custom work order task summary.

