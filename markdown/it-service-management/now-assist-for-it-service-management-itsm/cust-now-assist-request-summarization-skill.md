---
title: Customize Now Assist for IT Service Management \(ITSM\) Request Management skills
description: If you have the admin role, you can customize a Now Assist for IT Service Management \(ITSM\) skill so that agents can use the generative AI skills in Service Operations Workspace for ITSM and in Core UI.
locale: en-US
release: australia
product: Now Assist for IT Service Management \(ITSM\)
classification: now-assist-for-it-service-management-itsm
topic_type: task
last_updated: "2026-04-03"
reading_time_minutes: 4
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configure, Now Assist for IT Service Management \(ITSM\), IT Service Management]
---

# Customize Now Assist for IT Service Management \(ITSM\) Request Management skills

If you have the admin role, you can customize a Now Assist for IT Service Management \(ITSM\) skill so that agents can use the generative AI skills in Service Operations Workspace for ITSM and in Core UI.

## Before you begin

Role required: sn\_nowassist\_admin.nsa\_admin

## About this task

**Important:** Request Management skills include the following:

-   Request summarization
-   Requested item summarization
-   Catalog task summarization
-   Request activity response generation
-   Requested item activity response generation
-   Catalog task activity response generation

The following procedure contains examples that are specific to the request summarization skill. The steps are broadly applicable to other Request Management skills.

## Procedure

1.  Navigate to **Admin** &gt; **Now Assist Admin**.

2.  Select the **Now Assist Skills** tab.

3.  In the **Technology** feature group, select **ITSM** from the product list.

4.  Copy the Request Management skill you want to customize.

    **Note:** Activity response generation skills cannot be copied at this time, and their input table and input fields are read-only.

    1.  Select the more actions icon ![More actions icon.](../../itsm-workspace/image/more-actions-icon.png) for the skill, and select **Make a copy** to create a copy to customize.

    2.  Select the copied skill and select **Activate** to activate the skill.

        A guided setup leads you through the configuration of the general details, input, availability, display, review, and activation of the customized skill.

5.  In the General details step, fill in the fields.

    1.  Enter a name and description for the skill.

    2.  Select **Save and continue** to go to the next step.

6.  Choose input data.

    For information about the inputs and triggers for each skill, see [Skill inputs and triggers for Now Assist for IT Service Management \(ITSM\)](../reference/now-assist-itsm-skills.md).

    Each skill relies on a base input table and input fields with descriptions to provide context for the Now LLM Service to generate a response.

    Select only those related tables that are offered with the base system as part of the input data.

    1.  Add multiple base input tables and fields if more inputs are needed.

        ![Choose input data screen that contains the input tables and fields to define the prompt.](../image/now-assist-itsm-request-summarization-skill.png)

        The following table lists the base input table fields and descriptions, including a relevant example.

<table id="table_c53_vp5_dbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Base input field

</td><td>

Field in the Incident table whose value this skill uses in its response.

 For example, `Short description`.

</td></tr><tr><td>

Field description

</td><td>

Description of the base input field value.

 For example, `Short description of the request provides quick info about the issue.`

</td></tr></tbody>
</table>    2.  Add additional related tables and fields as needed.

        Adding the input data sources, such as more related tables and fields provide more context to the Now LLM Service in a related list.

        Configuring the related table fields follows the same format as the base input table fields in the Choose input step.

        ![Choose additional input data screen that contains the input tables and fields to define the prompt.](../image/now-assist-itsm-request-management-sla.png)

    3.  Select **Save and continue** to go to the next step.

7.  Customize the prompt.

    1.  Select the Request Management record in the Test response section, and test the prompt response output format by selecting **Run Test**.

    2.  Select **Edit prompt in Now Assist Skill Kit** to make necessary changes to the prompt in the Now Assist Skill Kit.

        ![Edit prompt screen to modify prompts in the Now Assist Skill Kit.](../image/now-assist-itsm-request-edit-prompt.png)

    3.  Select **Save and continue** to go to the next step.

8.  Define availability.

    Define how the skill will be available to users.

    1.  Configure the skill to be always available to users, or select the conditions that must be met before the skill is available.

        Selecting **Customize skill availability** displays a condition builder to filter the data further.

    2.  Select **Save and continue** to go to the next step.

9.  Define access.

    Define which roles can access the selected Request Management skill. By default, the itil role can access it.

10. Select display.

    Configure where to display the summarization for the selected Request Management skill.

    1.  Select either **In-product desktop** or **Now Assist panel**.

        -   **In-product desktop**: When selected, Now Assist skills are displayed in all ITSM products \(on forms and in workspaces\).

            For the skills that appear in-product, select the down arrow to identify the roles that can use the skill.

        -   **Now Assist panel**: When selected, Now Assist skills are available in the Now Assist panel.

            If you don't see this option, you must activate the Now Assist panel. For more information, see Activate the Now Assist panel standard chat.

            For the skills that appear in the Now Assist panel, select the down arrow to identify the roles that can use the skill.

    2.  Select **Save and continue** to go to the next step.

11. Review and activate.

    Review your choices and select **Activate** to complete the skill customization. A popup displays to show that activation was successful.


