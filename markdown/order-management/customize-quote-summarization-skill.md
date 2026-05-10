---
title: Customize a quote summarization skill in Now Assist for Configure, Price, Quote \(CPQ\)
description: Configure the Now Assist for Configure, Price, Quote \(CPQ\) application so that the agent can use the generative AI skills in the CSM/FSM Configurable Workspace and Business Portal.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Configure, Now Assist for CPQ]
---

# Customize a quote summarization skill in Now Assist for Configure, Price, Quote \(CPQ\)

Configure the Now Assist for Configure, Price, Quote \(CPQ\) application so that the agent can use the generative AI skills in the CSM/FSM Configurable Workspace and Business Portal.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Now Assist Skills**.

2.  In the **Customer** workflow group, view the skills for Now Assist for CPQ under Sales CRM.

3.  Make a copy of an active quote summarization skill by selecting the More actions icon ![](../../tmt-order-mgt/image/more-options.png) and then select **Make a copy** to create a version that you can customize.

4.  In the General details step, fill in the fields.

    1.  Enter a name and description for the skill.

    2.  Select **Save and continue** to go to the next step.

    **Note:** The **More details on the skills** fields are read-only.

5.  In the View quote input step, configure the base input table fields and related lists for the Quote template.

    **Note:** The **Choose base table** field is ready-only.

    Each skill relies on a base input table and input fields with descriptions to provide context for the Now LLM Service to generate a response.

    1.  Add base input table fields by selecting **New base input field**.

        The following table lists the base input table fields and descriptions.

<table id="table_c53_vp5_dbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Base input field

</td><td>

Field in the base input table whose value this skill uses in its response.

 For example, `Number`.

</td></tr><tr><td>

Field description

</td><td>

Description of the base input field value.

 For example, `Quote number`.

</td></tr></tbody>
</table>    2.  Configure the rule conditions to filter the data by using the condition builder.

        The rule conditions determine when the input template is used. By default, the record state determines the input template that the Now LLM Service uses.

        You can build the condition out further by selecting **New condition set** and configuring additional parameters.

    3.  Select the **New data source** field to configure the additional input data sources, as needed.

        Adding input data sources \(such as the related tables, activity streams, and relationships\) provide more context to the Now LLM Service in a related list.

        You can also add the rule conditions to these additional data sources.

        You can build the condition out further by selecting the **New condition set** field and configuring additional parameters.

        The selection of the related table fields has a direct impact on the quality of the corresponding prompt header.

    4.  Select **Save and continue** to go to the next step.

6.  Customize the prompt output.

    Review and test the default prompt provided. The prompt is fixed and can’t be customized directly within this step or from the Now Assist Admin screen.

    To customize or create prompts, select **Edit prompt in Now Assist Skill Kit**. You are redirected to the Now Assist Skill Kit, where you can manage prompt configurations for the skill. For more information, see [Now Assist Skill Kit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skill-kit/now-assist-skill-kit-landing.md).

    1.  Select a record in the Test output section and test the prompt response output format by selecting **Run Test**.

    2.  Select **Save and continue** to go to the next step.

7.  Use the Define availability section to define how the skill is available to users.

    1.  Configure the skill to be available to users, or select the conditions that must be met before the skill is available.

        Selecting the **Customize skill availability** field displays a condition builder to filter the data further.

        Select the **New condition set** field to configure additional conditions, as needed.

    2.  Select **Save and continue** to go to the next step.

8.  Specify which users can access the skill in the Define access section.

    By selecting specific roles, you're controlling who can use the skill. The roles that you choose will also be available in the Select display step.

    Default and Custom roles:

    -   If no changes are made, the default role automatically appears in **User access - Access Control List \(ACL\)**.
    -   Apply role restrictions when the skill is invoked by selecting **Roles** and defining which data and resources \(for example, tables\) the user can access in **Role restrictions to skill**.

        **Note:** If you add a role in the Define Access step, you must manually select it in the **Select Display** field to make it active.

9.  Configure the **In-product desktop** field to display the quote summarization.

    1.  Display Now Assist skills on the forms and workspaces by selecting the **In-product desktop** field.

        For the skills that appear in-product, select the arrow to identify the roles that can use the skill.

    2.  Select **Save and continue** to go to the next step.

10. Review and activate the skill.

    1.  Review your choices and select **Activate** to complete the skill customization.

    2.  Generate the quote summary by selecting **Summarize** in a quote.


**Parent Topic:**[Configuring Now Assist for Configure, Price, Quote \(CPQ\)](../concept/configure-now-assist-cpq.md)

