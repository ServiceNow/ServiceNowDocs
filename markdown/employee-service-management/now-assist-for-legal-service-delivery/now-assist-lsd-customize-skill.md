---
title: Customize a summarization skill in Now Assist for Legal Service Delivery \(LSD\)
description: If you have the admin role, you can customize a Now Assist for Legal Service Delivery \(LSD\) skill so that you can use the generative AI skills in Legal Counsel Center and in Core UI.
locale: en-US
release: australia
product: Now Assist for Legal Service Delivery
classification: now-assist-for-legal-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 7
keywords: [Now Assist, generative AI]
breadcrumb: [Configure, Now Assist for Legal Service Delivery \(LSD\), Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Customize a summarization skill in Now Assist for Legal Service Delivery \(LSD\)

If you have the admin role, you can customize a Now Assist for Legal Service Delivery \(LSD\) skill so that you can use the generative AI skills in Legal Counsel Center and in Core UI.

## Before you begin

Role required: admin

## About this task

The legal request summarization and legal matter summarization skills are available in the base system with the required configurations. To customized the skill, you must create a copy of the skill that is in the base system before you modify the configuration. Activating a customized skill with the same base input table as the original skill automatically deactivates the original skill.

From the Now Assist Admin console, you can select the input table, related records, and fields for each input template of the request summarization skill, and then configure the prompt headers to include in the general summary.

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Skills** to access the **Now Assist Skills** tab of the Now Assist Admin console.

2.  Navigate to **Employee** &gt; **LSD**.

3.  Create a copy of the Now Assist for LSD feature summarization skill for customization.

    1.  On the feature card that is associated with the skill that you would like to activate, select the More actions icon ![More actions icon](../image/more-actions-icon.png) and create a copy that you can customize by selecting **Make a copy**.

    2.  On the confirmation pop-up, select **Make a copy**.

        A guided setup leads you through the configuration of the general details, input, prompt, availability, display, review, and activation of the customized skill. If you complete the entire walk-through, the summarization skill is activated.

4.  In the General details step, fill in the fields.

    For information about the inputs for each skill, see [Skill inputs for Now Assist for Legal Service Delivery \(LSD\)](../concept/now-assist-lsd-skill-inputs.md).

    1.  Enter a name and description for the skill.

    2.  Select **Save and continue** to go to the next step.

5.  Customize the Now Assist context menu configuration.

    Customize the Now Assist context menu configuration to control which options should appear and how they are displayed in the Now Assist summarization.

    **Note:** Selecting the Enable Extended Tables check box applies the Now Assist context menu configuration to all the extended tables of the legal request and legal matter.

    For more information about the Now Assist context menu summarization, see Summarize records with the Now Assist context menu.

6.  View the input data for each skill, such as the base input fields and related lists for the different input templates \(New, Work in progress, or Closed states\).

    Each skill relies on a base input table and input fields with descriptions to provide context for the Now LLM Service to generate a response.

    Select only those related tables that are offered as the base system, as part of the input data.

    1.  For each input template state \(New, Work in progress, or Closed\), select **+New base input field** and configure the base input table fields.

        Add multiple base input fields, as necessary.

        ![View of all the input tables and fields that are used to define the prompt that determines where to pull the data from](../image/lsd-na-skill-input-customize.png)

        The following table lists the base input table fields and descriptions, including a relevant example.

<table id="table_c53_vp5_dbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Base input field

</td><td>

Field in the table whose value this skill uses in its response.

 For example, `Short description`.

</td></tr><tr><td>

Field description

</td><td>

Description of the base input field value.

 For example, `Short description of legal request, provides quick info about the request.`

</td></tr></tbody>
</table>    2.  For each input template state \(New, Work in progress, or Closed\), configure the rule conditions by using the condition builder to filter the data.

        The rule conditions determine when the input template is used. By default, the record state determines the input template that the Now LLM Service uses.

        You can build the condition out further by selecting **+New condition set** and configuring additional parameters.

        The following table lists the input template states.

        |State|Description|
        |-----|-----------|
        |New|State is New.|
        |Work in progress|State is Work in Progress.|
        |Closed|State is Closed.|

    3.  For each input template state \(New, Work in progress, or Closed\), select **+New data source** to configure the additional related table and activity stream data, as needed.

        Adding input data sources, like the related tables and activity streams, provide more context to the Now LLM Service in a related list.

        You can also add the rule conditions to these additional data sources.

        The selection of the related table fields may have a direct impact on the quality of the corresponding prompt header. For example, if a prompt header requires a specific field from the related table, but that field isn’t selected as input, the summary for that prompt header will contain missing information. For example, for a legal request, you see one related table, such as Service level agreement \(SLA\), that includes all the required fields and filtering conditions for the prompt header. The SLA prompt header is preselected to help you understand how the related table, its fields, and the prompt header work together to produce a summary. You can use the SLA as a reference to configure the other related tables to determine which fields to select and which description adds the requirements of their respective prompt headers. Apply any additional conditions to filter the data further.

    4.  Select **Save and continue** to go to the next step.

7.  Customize the prompt.

    Review and test the prompt for each input template configuration. You can edit the prompt by selecting **Edit prompt in Now Assist Skill Kit**

    1.  Select a record in the Test response section, and test the prompt response output format by selecting **Run Test**.

        ![Selection of new sections that can be included in the summary for each input template.](../image/lsd-na-skill-prompt-customize.png)

    2.  Select **Edit prompt in Now Assist Skill Kit** to edit the prompt.

    3.  After editing and publishing the prompt in the Now Assist Skill kit, return and test the prompt.

    4.  On finalizing the prompt, select **Save and continue** to go to the next step.

8.  Define how the skill is available to your users.

    1.  Configure the skill to be always available to users or select conditions that must be met before the skill is available.

        Selecting **Customize skill availability** displays a condition builder to filter the data further.

    2.  Select **Save and continue** to go to the next step.

9.  Enable Legal Practice Area tables to be considered for summarization.

    1.  Select the check box **Enable extended table selection**.

    2.  Select **Save and continue** to go to the next step.

10. Define who can access the skilland the data.

    1.  Select **Define access** to determine who can access the skill.

        By selecting specific roles, you're controlling who can use it. The roles you choose will also be available in the next step **Select display**.

        Default and Custom Roles:

        -   If custom roles were added before the upgrade, they’ll be updated automatically by a script.
        -   If new roles are created after the upgrade, you’ll need to manually add them in both the **Define Access** and **Select Display**.

            **Note:** In the **Select Display** step, you can only choose roles that were added in the **Define Access** step. If you add a role in **Define Access**, you still need to manually select it in **Select Display** to make it active.

    2.  In the **Role restrictions to skill** section, grant data access to additional roles.

        For more information, see role masking.

    3.  Select **Save and continue** to go to the next step.

11. After you define access, select **Save and continue** to go to the next step.

12. Configure where to display the summarization.

    1.  Select either **In-product**, or **Now Assist panel**.

        -   **In-product**: When selected, the Now Assist skills are displayed on the forms and workspaces.

            For the skills that appear in-product, select the down arrow to identify the roles that can use the skill.

        -   **Now Assist panel**: When selected, the Now Assist skills are available in the Now Assist panel.

            If you don't see this option, you must activate the Now Assist panel. For more information, see Activate the Now Assist panel standard chat.

            For the skills that appear in the Now Assist panel, select the down arrow to identify the roles that can use the skill.

    2.  Select **Save and continue** to go to the next step.

13. Review and activate the skill.

    Review your choices and select **Activate** to complete the skill customization.

    You can now select **Summarize** to generate the summary.

14. Configure the variables of the practice areas that you want to be considered as inputs for the legal request or matter summarization.

    For more information, see [Configure variables for Now Assist summarization](configure-variables-for-now-assist-summarization.md).


