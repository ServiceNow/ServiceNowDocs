---
title: Customize a skill in Now Assist for TMT
description: If you have the admin role, you can customize a Now Assist for Telecommunications, Media and Technology \(TMT\) skill so that agents can use the generative AI skills in CSM Configurable Workspace and in Core UI.
locale: en-US
release: zurich
product: Now Assist for Telecom, Media and Technology
classification: now-assist-for-telecom-media-and-technology
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Configure, Now Assist for TMT, Telecommunications, Media, and Technology \(TMT\)]
---

# Customize a skill in Now Assist for TMT

If you have the admin role, you can customize a Now Assist for Telecommunications, Media and Technology \(TMT\) skill so that agents can use the generative AI skills in CSM Configurable Workspace and in Core UI.

## Before you begin

Role required: admin

## About this task

From the Now Assist Admin console, you can select the input table, related records, and fields for each input template of the account onboarding and service problem management, and then configure the prompt headers to include them in the general summary.

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Features** to access the **Now Assist Features** tab of the Now Assist Admin console.

2.  In the **Customer** workflow group, select **TMT** to view the skills for the Now Assist for TMT features.

3.  Activate and copy the Now Assist for TMT feature case summarization skill for customization.

    1.  On the feature card that is associated with the skill that you would like to activate, select **View details**.

    2.  In the All available skills section, locate the skill you would like to activate and select **Activate skill**.

        You can choose to make a copy of the skill before activating it.

    3.  Select the More actions icon for the skill in the Active skills section, and create a copy that you can customize by selecting **Make a copy**.

        The copy that you make is listed in the Active skills section.

    4.  Select the copied skill from the Active skills section to open it.

        A guided setup leads you through the configuration of the general details, input, prompt, availability, display, review, and activation of the customized skill. If you complete the entire walk-through, the case summarization skill is activated.

4.  In the General details step, fill in the fields.

    For information about the inputs and triggers for each skill, see [Skill inputs for Now Assist for Telecommunications, Media and Technology \(TMT\)](../concept/now-assist-skill-inputs.md).

    1.  Enter a name and description for the skill.

    2.  Select **Save and continue** to go to the next step.

5.  View the input data for each skill, such as the base input fields and related lists for the different input templates.

    Configure the base input table fields and related lists for the different input templates for the skill.

    Each skill relies on a base input table and input fields with descriptions to provide context for the Now LLM Service to generate a response.

    Select only those related tables that are offered as the base system, as part of the input data.

    1.  For each input template, select **+New base input field** and configure the base input table fields.

        Add multiple base input fields, as necessary.

        ![View of all the input tables and fields that are used to define the prompt that will determine where to pull the data from.](../image/customize-now-assist-tmt.png "View input step")

        ![View of all the input tables and fields that are used to define the prompt that will determine where to pull the data from.](../image/customize-service-problem-case.png "View input step")

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
</table>    2.  For each input template, configure the rule conditions by using the condition builder to filter the data.

        The rule conditions determine when the input template is used. By default, the record state determines the input template that the Now LLM Service uses.

        You can build the condition out further by selecting **+New condition set** and configuring additional parameters.

    3.  For each input template, select **+New data source** to configure the additional related table and activity stream data, as needed.

        Adding input data sources, like the related tables and activity streams, provide more context to the Now LLM Service in a related list.

        You can also add the rule conditions to these additional data sources.

    4.  Select **Save and continue** to go to the next step.

6.  Customize the prompt.

    Review and test the prompt for each input template configuration. You can edit the prompt by adding new predefined sections and reordering them, as needed.

    1.  For each input template, select the prompt sections from the list of available sections to include in the generated summary.

        To add a section, you must configure the relevant input data prior to this step.

        You can add the **Waiting on customer** prompt to cases only if the case has an **Awaiting info** state. Otherwise, adding this header to other states could cause the Now LLM Service to generate inaccurate or unreliable results.

    2.  Select **Save** to continue to the test response.

    3.  Select a case record in the Test response section, and test the prompt response output format by selecting **Run Test**.

        ![Selection of new sections that can be included in the summary for each input template.](../image/customize-prompt-now-assist-tmt.png "Customize prompt step")

        ![Selection of new sections that can be included in the summary for each input template.](../image/customize-prompt-service-problem-case.png "Customize prompt step")

    4.  Select **Save and continue** to go to the next step.

7.  Customize the prompt for customer service summary skill.

    Review the prompt for each input template.

    ![customize prompt output.](../image/customize-prompt-customer-service-skill.png)

    1.  Select **Edit prompt in Now Assist Skill Kit** to visit Now Assist Skill Kit.

        ![edit prompt.](../image/edit-prompt-now-assist-skill-kit.png)

    2.  Select **Go to Now Assist Skill Kit** to review and modify the prompt.

8.  Customize the prompt for risk signal and issues summary skill.

    Review the prompt for each input template.

    ![customize prompt output.](../image/customize-prompt-risk-signals.png)

    1.  Select **Edit prompt in Now Assist Skill Kit** to visit Now Assist Skill Kit.

        ![edit prompt.](../image/edit-prompt-risk-signals.png)

    2.  Select **Go to Now Assist Skill Kit** to review and modify the prompt.

9.  Select **Save and continue** to go to the next step.

10. Define how the skill is available to your users.

    1.  Configure the skill to be always available to users, or select conditions that must be met before the skill is available.

        Selecting **Customize skill availability** displays a condition builder to filter the data further.

    2.  Select **Save and continue** to go to the next step.

11. Configure where to display the case summarization.

    1.  Select either **In-product**, or **Now Assist panel**.

        -   **In-product**: When selected, the Now Assist skills are displayed on the forms and workspaces.

            For the skills that appear in-product, select the down arrow to identify the roles that can use the skill.

        -   **Now Assist panel**: When selected, the Now Assist skills are available in the Now Assist panel.

            If you don't see this option, you must activate the Now Assist panel. For more information, see [Activate the Now Assist panel standard chat](https://www.servicenow.com/docs/access?context=activate-now-assist-panel&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

            For the skills that appear in the Now Assist panel, select the down arrow to identify the roles that can use the skill.

    2.  Select **Save and continue** to go to the next step.

12. Review and activate the skill.

    Review your choices and select **Activate** to complete the skill customization.

    You can now select **Summarize** in a case to generate the case summary.


