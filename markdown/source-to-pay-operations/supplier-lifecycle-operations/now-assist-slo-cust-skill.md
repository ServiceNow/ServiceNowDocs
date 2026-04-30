---
title: Customize a Now Assist for Supplier Lifecycle Operations \(SLO\) skill
description: If you have the admin role, you can customize a Now Assist for Supplier Lifecycle Operations \(SLO\) skill. By customizing a skill, supplier managers can use the generative AI skills in Source-to-Pay Workspace and in Core UI.
locale: en-US
release: xanadu
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2024-11-05"
reading_time_minutes: 4
keywords: [generative AI, gen AI, genai, artificial intelligence]
breadcrumb: [Configure Now Assist for Supplier Lifecycle Operations \(SLO\), Now Assist for Supplier Lifecycle Operations \(SLO\), Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Customize a Now Assist for Supplier Lifecycle Operations \(SLO\) skill

If you have the admin role, you can customize a Now Assist for Supplier Lifecycle Operations \(SLO\) skill. By customizing a skill, supplier managers can use the generative AI skills in Source-to-Pay Workspace and in Core UI.

## Before you begin

Role required: admin

## About this task

From the Now Assist Admin console, you can select the input table, related records, and fields for each input template of the Case summarization skill. You can then configure the prompt headers to include them in the general summary.

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Features** to access the **Now Assist Features** tab of the Now Assist Admin console.

2.  In the **Finance and Supply Chain** workflow group, select **Supplier Lifecycle Operations** to view the skill for the Now Assist for SLO feature.

3.  Create a copy of the skill and customize the input fields.

    1.  On the Case summarization feature card, select **View details**.

    2.  In the Active skills section, locate the skill that you'd like to copy and select the More actions icon \(![More actions icon.](../../sourcing-procurement-operations/image/more_vertical_icon.png)\).

    3.  Select **Make copy**.

        The copy that you make is listed in the Active skills section.

    4.  Select the copied skill from the Active skills section to open it.

        A guided setup leads you through the configuration of the general details, input, prompt, availability, display, review, and activation of the customized skill. If you complete the entire walk-through, the skill is activated.

4.  In the General details step, fill in the fields.

    For information about the inputs for each skill, see [Skill input for Now Assist for Supplier Lifecycle Operations \(SLO\)](../reference/now-assist-slo-skill-input-triggers.md).

    1.  Enter a name and description for the skill.

    2.  Select **Save and continue** to go to the next step.

5.  View the input data for each skill, such as the base input fields and related lists for the different input templates.

    Configure the base input table fields and related lists for the different input templates for the skill.

    Each skill relies on a base input table and input fields with descriptions to provide context for the Now LLM Service to generate a response.

    Select only those related tables that are offered as the base system, as part of the input data.

    1.  For each input template state, select **+New base input field** and configure the base input table fields.

        Add multiple base input fields, as necessary.

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

 For example, `Short description of case, provides quick info about the case.`

</td></tr></tbody>
</table>    2.  For each input template state, configure the rule conditions by using the condition builder to filter the data.

        The rule conditions determine when the input template is used. By default, the record state determines the input template that the Now LLM Service uses.

        You can build the condition out further by selecting **+New condition set** and configuring additional parameters.

    3.  For each input template state, select **+New data source** to configure the additional related table and activity stream data, as needed.

        You can add input data sources like related tables, activity streams, and relationships to provide more context to the Now LLM Service. You can also add rule conditions to these additional data sources.

        The selection of the related table fields can have a direct impact on the quality of the corresponding prompt header. If a prompt header requires a specific field from a related table, but that field isn’t selected as input, the summary for that prompt header contains missing information.

    4.  Select **Save and continue** to go to the next step.

6.  Customize the prompt.

    Review and test the prompt for each input template configuration. You can edit the prompt by adding new predefined sections and reordering them, as needed.

    1.  For each input template state, select the prompt sections from the list of available sections to include in the generated summary.

        To add a section, you must configure the relevant input data prior to this step.

        The available prompt sections that you can select:

        -   **Overview**
        -   **Actions completed**
        -   **Next steps**
        The following table lists the required prompt headers.

<table id="table_av3_xhw_2bc"><thead><tr><th>

Input template state

</th><th>

Required prompt header

</th></tr></thead><tbody><tr><td>

Open

</td><td>

-   Overview
-   Actions completed
-   Next steps


</td></tr><tr><td>

Closed

</td><td>

-   Overview
-   Actions completed


</td></tr></tbody>
</table>    2.  Select **Save** to continue to the test response.

    3.  Select a record in the Test response section, and test the prompt response output format by selecting **Run Test**.

    4.  Select **Save and continue** to go to the next step.

7.  Define how the skill is available to your users.

    1.  Configure the skill to be always available to users, or select conditions that must be met before the skill is available.

        Selecting **Customize skill availability** displays a condition builder to filter the data further.

    2.  Select **Save and continue** to go to the next step.

8.  Configure where to display the supplier case summarization.

    1.  Select **In-product desktop** to display the Now Assist skills on forms and workspaces.

        For the skills that appear in the in-product desktop, select the down arrow to identify the roles that can use the skill.

    2.  Select **Save and continue** to go to the next step.

9.  Review and activate the skill.

    Review your choices and select **Activate** to complete the skill customization.

    You can select **Summarize** in a record to generate the summary for the supplier case.


