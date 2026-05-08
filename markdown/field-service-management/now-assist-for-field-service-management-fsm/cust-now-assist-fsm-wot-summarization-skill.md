---
title: Customize a Now Assist for Field Service Management \(FSM\) work order task summarization skill
description: As an admin you can clone the Work order task summarization skill, then access the skill in the Now Assist skill kit, and update the prompts.
locale: en-US
release: australia
product: Now Assist for Field Service Management \(FSM\)
classification: now-assist-for-field-service-management-fsm
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Customizing a skill, Configure, Now Assist for FSM]
---

# Customize a Now Assist for Field Service Management \(FSM\) work order task summarization skill

As an admin you can clone the Work order task summarization skill, then access the skill in the Now Assist skill kit, and update the prompts.

## Before you begin

Role required: wm\_admin

## About this task

From the Now Assist Admin console, you can select the input tables, related lists, and fields for each input template of the work order task summarization skill.

## Procedure

1.  Navigate to **Admin** &gt; **Now Assist Admin**.

2.  Select the **Now Assist Skills** tab.

3.  In the **Customer** workflow group, select **FSM** to view the skills for the Now Assist for FSM features.

4.  Activate and copy the Now Assist for FSM work order task summarization skill for customization.

    1.  On the work order task summarization feature card, select **View details**.

    2.  In the All available skills section, locate the work order task summarization skill and select **Activate skill**.

        You can choose to make a copy of the skill before activating it.

    3.  Select the more actions icon ![](../image/more_actions.png) for the skill in the Active skills section, and create a copy that you can customize by selecting **Make a copy**.

        The copy that you make is listed in the Active skills section.

        **Note:** You can only duplicate a work order task summarization skill or the KB generation skill. The fields for the skills that you can’t duplicate have read-only values.

    4.  Select the copied skill from the Active skills section to open it.

        A guided setup leads you through the configuration of the general details, input, availability, display, review, and activation of the customized skill. When you complete the entire walk-through, the skill is activated.

5.  In the General details step, fill in the fields.

    For information about the inputs and triggers for each skill, see [Skill inputs for Now Assist for Field Service Management \(FSM\)](../concept/now-assist-fsm-skill-inputs.md).

    1.  Enter a name and description for the skill.

    2.  Select **Save and continue** to go to the next step.

6.  Choose input data.

    Configure the base input table fields and related lists for the different input templates \(New, Work In Progress, and Closed states\) for the skill.

    Each skill relies on a base input table and input fields with descriptions to provide context for the Now LLM Service to generate a response.

    Select only those related tables that are offered with the base system as part of the input data.

    1.  For each input template state \(New, WIP, and Closed\), select **+New base input field field** and configure the base input table fields.

        Add multiple base input fields if more inputs are needed.

        ![Choose input data screen that contains the input tables and fields to define the prompt.](../image/now-assist-wot-summ-skill-view-input.png)

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
</table>    2.  For each input template state \(New, WIP, and Closed\), configure the rule conditions by using the condition builder to filter the data further.

        The rule conditions determine when the input template is used. By default, the record state determines the input template that the Now LLM Service uses.

        You can build the condition out further by selecting **+New condition set** and configuring additional parameters.

        The following table lists the input template states.

        |State|Description|
        |-----|-----------|
        |New|State is New.|
        |WIP|State is Work in Progress.|
        |Closed|State is Closed.|

    3.  For each input template state \(New, WIP, and Closed\), select **+New data source** to configure the additional related table, activity streams, and relationships as needed.

        Adding the input data sources, such as the related tables, activity streams, and relationships provides more context to the Now LLM Service.

        You can also add the rule conditions to these additional related table, activity stream, and relationship data sources.

        ![Choose additional input data screen that contains the input tables and fields to define the prompt.](../image/now-assist-wot-summ-skill-view-input-2.png)

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
</table>    4.  Select **Save and continue** to go to the next step.

7.  Customize the prompt.

    Evaluate the prompt utilized for each input template to confirm it meets your expectations. To review and modify the prompt, you can visit the Now Assist Skill Kit.

    1.  For each input template state \(New, WIP, and Closed\), select a work order task record in the Test response section, and test the prompt response output format by selecting **Run Test**

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
</table>    2.  Select **Edit prompt in Now Assist Skill Kit** to make necessary changes to the prompt in the Now Assist Skill Kit.![Edit prompt screen to modify prompts in the Now Assist Skill Kit.](../image/now-assist-wot-summ-skill-cust-prompt.png)

    3.  Select **Save and continue** to go to the next step.

8.  Define availability.

    Define how the skill will be available to users.

    1.  Configure the skill to be always available to users, or select the conditions that must be met before the skill is available.

        Selecting **Customize skill availability** displays a condition builder to filter the data further.

    2.  Select **Save and continue** to go to the next step.

9.  Select display.

    Configure where to display the work order task summarization.

    1.  Select either **In-product**, or **Now Assist panel**.

        -   **In-product**: When selected, Now Assist skills are displayed in all FSM products \(on forms and in workspaces\).

            For the skills that appear in-product, select the down arrow to identify the roles that can use the skill.

        -   **Now Assist panel**: When selected, Now Assist skills are available in the Now Assist panel.

            If you don't see this option, you must activate the Now Assist panel. For more information, see Activate the Now Assist panel standard chat.

            For the skills that appear in the Now Assist panel, select the down arrow to identify the roles that can use the skill.

    2.  Select **Save and continue** to go to the next step.

10. Review and activate.

    Review your choices and select **Activate** to complete the skill customization.

    You can now select **Summarize** from a work order task record and generate the custom work order task summary.


