---
title: Configure the Government case summarization skill in Now Assist for Public Sector Digital Services \(PSDS\)
description: Activate and customize the Government case summarization skill in the Now Assist for Public Sector Digital Services \(PSDS\) application so that government service agents can use the generative AI skills in CSM Configurable Workspace and in Public Sector Digital Services Core UI.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Activate Now Assist skills, Configure, Now Assist for PSDS, Public Sector Digital Services \(PSDS\)]
---

# Configure the Government case summarization skill in Now Assist for Public Sector Digital Services \(PSDS\)

Activate and customize the Government case summarization skill in the Now Assist for Public Sector Digital Services \(PSDS\) application so that government service agents can use the generative AI skills in CSM Configurable Workspace and in Public Sector Digital Services Core UI.

## About this task

Government service agents can utilize case summarization, powered by Now LLM, to gain contextual understanding of constituent issues throughout the case's lifecycle. The case summarization skill auto-generates informative summaries that distill key details from work notes, comments, and other case data, which can help agents resolve cases faster.

**Note:** The base system includes a pre-configured case summarization skill.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Features** to access the **Now Assist Features** tab of the Now Assist Admin console.

2.  In the dropdown, select **Customer** &gt; **PSDS**.

    ![Now Assist Panel showing NA skills and features in PSDS](../image/now-assist-psds-panel.png)

3.  On the Government case feature card, select **View Details**, then select **Case Summarization** under Active Skills.

    By default, the case summarization skill is activated for Now Assist for PSDS. If it is not active, select **Activate Skill** in the All available Chat skills section of the case recommendation card.

4.  In the Active skills section, locate the **Government case summarization** skill.

5.  Select the More actions icon![More actions icon](../image/more-actions-na-psds.png) for the skill in the Active skills section, and create a copy that you can customize by selecting **Make a copy**.

    The copy that you make is listed in the Active skills section.

6.  Select the copied skill from the Active skills section to open it.

    A guided setup leads you through the configuration of the general details, input, prompt, availability, display, review, and activation of the customized skill. If you complete the entire walk-through, the case summarization skill is activated.

7.  In the General details step, fill in the fields.

    For information about the inputs and triggers for each skill, see [Skill inputs for Now Assist for Public Sector Digital Services \(PSDS\)](now-assist-psds-skill-inputs.md).

    1.  Enter a name and description for the skill.

    2.  Select **Save and continue** to go to the next step.

8.  View the input data for each skill, such as the base input fields and related lists for the different input templates \(Case new, Case work in progress, and Case resolved states\).

    Configure the base input table fields and related lists for the different input templates \(Case new, Case work in progress, and Case resolved states\) for the skill.

    Each skill relies on a base input table and input fields with descriptions to provide context for the Now LLM Service to generate a response.

    Select only those related tables that are offered as the base system, as part of the input data.

    1.  For each input template state \(New, Work in progress, and Resolved\), select **+New base input field** and configure the base input table fields.

        Add multiple base input fields, as necessary.

        ![View of all the input tables and fields that are used to define the prompt that will determine where to pull the data from.](../image/choose-input-data-na-psds.png "View input step")

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

 For example, `Short description of case, provides brief information about the issue.`

</td></tr></tbody>
</table>    2.  For each input template state \(New, Work in progress, and Resolved\), configure the rule conditions by using the condition builder to filter the data.

        The rule conditions determine when the input template is used. By default, the record state determines the input template that the Now LLM Service uses.

        You can build the condition out further by selecting **+New condition set** and configuring additional parameters.

        The following table lists the input template states.

        |State|Description|
        |-----|-----------|
        |New|State is New.|
        |Work in progress|State is Work in Progress.|
        |Resolved|State is Resolved.|

    3.  For each input template state \(New, Work in progress, and Resolved\), select **+New data source** to configure the additional related table and activity stream data, as needed.

        Adding input data sources, like the related tables and activity streams, provide more context to the Now LLM Service in a related list.

        You can also add the rule conditions to these additional data sources.

        The selection of the related table fields may have a direct impact on the quality of the corresponding prompt header. For example, if a prompt header requires a specific field from the related table, but that field isn’t selected as input, the summary for that prompt header will contain missing information. For example, as a base case, you see one related table, such as Service level agreement \(SLA\), that includes all the required fields and filtering conditions for the prompt header. The SLA prompt header is preselected to help you understand how the related table, its fields, and the prompt header work together to produce a summary. You can use the SLA as a reference to configure the other related tables to determine which fields to select and which description adds the requirements of their respective prompt headers. Apply any additional conditions to filter the data further.

    4.  Select **Save and continue** to go to the next step.

9.  Customize the prompt.

    Review and test the prompt for each input template configuration. You can edit the prompt by adding new predefined sections and reordering them, as needed.

    1.  For each input template state \(New, Work in progress, and Resolved\), select the prompt sections from the list of available sections to include in the generated summary.

        To add a section, you must configure the relevant input data prior to this step.

        The available prompt sections that you can select:

        -   **Issue**
        -   **Key Actions Taken**
        -   **Resolution**
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

Resolved

</td><td>

-   Issue
-   Key Actions Taken
-   Resolution


</td></tr></tbody>
</table>        You can add the **Waiting on customer** prompt to cases only if the case has an **Awaiting info** state. Otherwise, adding this header to other states could cause the Now LLM Service to generate inaccurate or unreliable results.

    2.  Select **Save** to continue to the test response.

    3.  Select a case record in the Test response section, and test the prompt response output format by selecting **Run Test**.

    4.  Select **Save and continue** to go to the next step.

10. Define how the skill is available to your users.

    1.  Configure the skill to be always available to users, or select conditions that must be met before the skill is available.

        Selecting **Customize skill availability** displays a condition builder to filter the data further.

    2.  Select **Save and continue** to go to the next step.

11. Configure where to display the case summarization.

    1.  Select either **In-product**, or **Now Assist panel**.

        -   **In-product**: When selected, the Now Assist skills are displayed on the forms and workspaces.

            For the skills that appear in-product, select the down arrow to identify the roles that can use the skill.

        -   **Now Assist panel**: When selected, the Now Assist skills are available in the Now Assist panel.

            If you don't see this option, you must activate the Now Assist panel. For more information, see [Activate the Now Assist panel standard chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/activate-now-assist-panel.md).

            For the skills that appear in the Now Assist panel, select the down arrow to identify the roles that can use the skill.

    2.  Select **Save and continue** to go to the next step.

12. Review your choices and select **Activate** to complete the skill customization.

    ![Review and activate step for Now Assist case summarization.](../image/case-summarization-activate-now-assist-psds.png)


