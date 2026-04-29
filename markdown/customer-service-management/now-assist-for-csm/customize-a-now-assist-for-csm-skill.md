---
title: Customize a case summarization skill in Now Assist for Customer Service Management \(CSM\)
description: If you have the admin role, you can customize a Now Assist for Customer Service Management \(CSM\) skill so that agents can use the generative AI skills in CSM Configurable Workspace and in Core UI.
locale: en-US
release: australia
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 7
breadcrumb: [Configure, Now Assist for CSM, Customer Service Management]
---

# Customize a case summarization skill in Now Assist for Customer Service Management \(CSM\)

If you have the admin role, you can customize a Now Assist for Customer Service Management \(CSM\) skill so that agents can use the generative AI skills in CSM Configurable Workspace and in Core UI.

## Before you begin

Role required: admin

## About this task

From the Now Assist Admin console, you can select the input table, related records, and fields for each input template of the case summarization skill, and then configure the prompt headers to include them in the general summary.

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Features** to access the **Now Assist Features** tab of the Now Assist Admin console.

2.  In the **Customer** workflow group, view the skills for the Now Assist for CSM features.

3.  Activate and copy the Now Assist for CSM feature case summarization skill for customization.

    1.  On the feature card that is associated with the skill that you would like to activate, select **View details**.

    2.  In the All available skills section, locate the skill that you would like to activate and select **Activate skill**.

        **Note:** Only one version of a skill can be active at a time for each table. If you create and activate a copy of the skill, any previously activated version of the skill is deactivated. The copied skill can be activated with the parent skill.

        You can choose to make a copy of the skill before activating it.

    3.  Select the More actions icon![](../image/more_vertical_icon.png) for the skill in the Active skills section, and create a copy that you can customize by selecting **Make a copy**.

        The copy that you make is listed in the Active skills section.

    4.  Select the copied skill from the Active skills section to open it.

        A guided setup leads you through the configuration of the general details, input, prompt, availability, display, review, and activation of the customized skill. If you complete the entire walk-through, the case summarization skill is activated.

4.  In the General details step, fill in the fields.

    For information about the inputs and triggers for each skill, see [Additional skill input and trigger information](additional-skill-input-and-trigger-information-for-now-assist_0.md).

    1.  Enter a name and description for the skill.

    2.  Select **Save and continue** to go to the next step.

5.  View the input data for each skill, such as the base input fields and related lists for the different input templates \(Case new, Case work in progress, or Case resolved states\).

    You can change the base input table and add case extension tables for the copied skill. To create an extended table, select **New** on the Tables list page, and select the table to extend from the **Extends table** search field. This option is only available when you’re creating a table, because it incorporates all of the fields of the original table and creates system fields for the new table.

    Configure the base input table fields and related lists for the different input templates \(Case new, Case work in progress, or Case resolved states\) for the skill.

    Each skill relies on a base input table and input fields with descriptions to provide context for the Now LLM Service to generate a response.

    Select only those related tables that are offered as the base system as part of the input data.

    1.  For each input template state \(New, Work in progress, or Resolved\), select **+New base input field** and configure the base input table fields.

        Add multiple base input fields, as necessary.

        ![View of all the input tables and fields that are used to define the prompt that will determine where to pull the data from.](../image/now-assist-csm-view-input.png "View input step")

        The following table lists the base input table fields and descriptions, including a relevant example.

<table id="table_c53_vp5_dbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Base input field

</td><td>

Field in the case table whose value this skill uses in its response.

 For example, `Short description`.

</td></tr><tr><td>

Field description

</td><td>

Description of the base input field value.

 For example, `Short description of case, provides quick info about the issue.`

</td></tr></tbody>
</table>    2.  For each input template state \(New, Work in progress, or Resolved\), configure the rule conditions by using the condition builder to filter the data.

        The rule conditions determine when the input template is used. By default, the record state determines the input template that the Now LLM Service uses.

        You can build the condition out further by selecting **+New condition set** and configuring additional parameters.

        The following table lists the input template states.

        |State|Description|
        |-----|-----------|
        |New|State is New.|
        |Work in progress|State is Work in Progress.|
        |Resolved|State is Resolved.|

    3.  For each input template state \(New, Work in progress, or Resolved\), select **+New data source** to configure the additional related table and activity stream data, as needed.

        Adding input data sources, like the related tables and activity streams, provide more context to the Now LLM Service in a related list.

        You can also add the rule conditions to these additional data sources.

        The selection of the related table fields may have a direct impact on the quality of the corresponding prompt header. For example, if a prompt header requires a specific field from the related table, but that field isn’t selected as input, the summary for that prompt header will contain missing information. For example, as a base case, you see one related table, such as a Service level agreement \(SLA\), that includes all the required fields and filtering conditions for the prompt header. The SLA prompt header is preselected to help you understand how the related table, its fields, and the prompt header work together to produce a summary. You can use the SLA as a reference to configure the other related tables to determine which fields to select and which description adds the requirements of their respective prompt headers. Apply any additional conditions to filter the data further.

    4.  Select **Save and continue** to go to the next step.

6.  Customize the prompt.

    Review and test the default prompt provided. The prompt is fixed and cannot be customized directly within this step or from the Now Assist Admin screen.

    To customize or create new prompts, select **Edit prompt in Now Assist Skill Kit**. This will redirect you to the Now Assist Skill Kit, where you can manage prompt configurations for the skill. For more info, see [Now Assist Skill Kit](https://www.servicenow.com/docs/access?context=now-assist-skill-kit-landing&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)

    1.  For each input template state \(New, Work in progress, or Resolved\), select the prompt to include in the generated summary.

    2.  Select **Save** to continue to the test response.

    3.  Select a case record in the Test response section, and test the prompt response output format by selecting **Run Test**.

    4.  Select **Save and continue** to go to the next step.

7.  Define how the skill is available to your users.

    1.  Configure the skill to be always available to users, or select conditions that must be met before the skill is available.

        Selecting **Customize skill availability** displays a condition builder to filter the data further.

    2.  Select **Save and continue** to go to the next step.

8.  Select **Define access** to determine who can access this skill.

    By selecting specific roles, you're controlling who can use it. The roles you choose will also be available in the next step **Select display**.

    Default and Custom Roles:

    -   If no changes are made, the default roles sn\_customerservice\_agent and sn\_customerservice.consumer\_agent will automatically appear in **Define Access** and **Select Display**.
    -   If custom roles were added before the upgrade, they’ll be updated automatically by a script.
    -   If new roles are created after the upgrade, you’ll need to manually add them in both the **Define Access** and **Select Display**.

        **Note:** In the **Select Display** step, you can only choose roles that were added in the **Define Access** step. If you add a role in **Define Access**, you still need to manually select it in **Select Display** to make it active.

9.  Configure where to display the case summarization.

    1.  Select either **In-product** or **Now Assist panel**.

        -   **In-product**: When selected, the Now Assist skills are displayed on the forms and workspaces.

            For the skills that appear in-product, select the down arrow to identify the roles that can use the skill.

        -   **Now Assist panel**: When selected, the Now Assist skills are available in the Now Assist panel.

            If you don't see this option, you must activate the Now Assist panel. For more information, see [Activate the Now Assist panel standard chat](https://www.servicenow.com/docs/access?context=activate-now-assist-panel&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

            For the skills that appear in the Now Assist panel, select the down arrow to identify the roles that can use the skill.

    2.  Select **Save and continue** to go to the next step.

10. Review and activate the skill.

    Review your choices and select **Activate** to complete the skill customization.

    You can now select **Summarize** in a case to generate the case summary.


