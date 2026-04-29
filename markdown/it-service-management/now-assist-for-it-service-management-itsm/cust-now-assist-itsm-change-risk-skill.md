---
title: Customize the Now Assist for IT Service Management \(ITSM\) change risk explanation skill
description: Enhance the efficiency to explain the risk of a change request by customizing it with different inputs and prompts using the skill configuration guided setup.
locale: en-US
release: australia
product: Now Assist for IT Service Management \(ITSM\)
classification: now-assist-for-it-service-management-itsm
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
keywords: [Now Assist, Agentic AI, generative AI, Gen AI]
breadcrumb: [Configure, Now Assist for IT Service Management \(ITSM\), IT Service Management]
---

# Customize the Now Assist for IT Service Management \(ITSM\) change risk explanation skill

Enhance the efficiency to explain the risk of a change request by customizing it with different inputs and prompts using the skill configuration guided setup.

## About this task

You can modify and edit prompts using the Now Assist Skill Kit \(NASK\). Navigate to **All &gt; Now Assist Skill Kit &gt; Home**, and select the required skill.

## Before you begin

Role required: sn\_nowassist\_admin.nsa\_admin

You need the sn\_skill\_builder.admin role to customize the prompt in the Now Assist Skill Kit \(NASK\).

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Skills**.

2.  In the **Technology** feature group, select **ITSM** from the product list.

3.  Activate and copy the change risk explanation skill for customization.

    1.  In the All available skills section, locate the skill that you would like to activate and select **Activate skill**.

        You can choose to make a copy of the skill before activating it.

    2.  Select the More actions icon ![More actions icon.](../../itsm-workspace/image/more-actions-icon.png) for the skill in the Active skills section, and create a copy that you can customize by selecting **Make a copy**.

        A confirmation message is displayed.

    3.  Select the **Make a copy** button in the confirmation message.

        A guided setup leads you through the configuration of the general details, input, prompt, availability, display, review, and activation of the customized skill.

4.  In the General details step, fill in the fields.

    For information about the inputs and triggers for each skill, see [Skill inputs and triggers for Now Assist for IT Service Management \(ITSM\)](../reference/now-assist-itsm-skills.md).

    1.  Enter a name and description for the skill.

    2.  Select **Save and continue** to go to the next step.

5.  Choose the change request input data.

    Configure the base input table and fields that are used as the source to generate a response.

    Each skill relies on a base input table and input fields with descriptions to provide context for the Now LLM Service to generate a response.

    Select only those related tables that are offered with the base system as part of the input data.

    1.  Add base input table fields.

        The following Base input fields values are available by default:

        -   Short description
        -   Risk
        -   Implementation plan
        -   Description
        -   Backout plan
        You can edit or remove the **Implementation plan**, **Description**, and **Backout plan** fields. You can also add new fields and descriptions for them by selecting **+New base input field**.

        **Important:** If you add a new field with the same name as an existing field, the name and description of the new field will override the description of the existing field.

        ![Change request risk form with editable input fields: Implementation plan, Description, Backout plan, and option to add new fields.](../image/itsm-now-assist-change-choose-input.png)

        The following table lists the base input table fields and descriptions, including a relevant example.

<table id="table_c53_vp5_dbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Base input field

</td><td>

Field in the Change request table, for example, `Short description`. The LLM uses the values in this field as one of inputs to generate a response.

</td></tr><tr><td>

Field description

</td><td>

Description of the base input field value.

 For example, `Short description field in the Change request table provides quick info about the issue.`

</td></tr></tbody>
</table>    2.  Add additional input data sources.

        The data sources could include related tables and relationships. The Change Risk Details related input table with read-only fields is available by default. You can’t edit the existing data source fields but you can add new related tables or relationships by selecting **+New data source** and then selecting the desired option.

        ![Additional input data sources](../image/itsm-now-assist-additional-input.png)

<table id="table_pcg_3zw_pdc"><thead><tr><th>

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

**Important:** When you add a new related table with the same name as an existing table, the fields and the descriptions in the new table will override the fields and descriptions in the existing table.

</td></tr><tr><td>

Relationship

</td><td>

Relationship between the input table and the table field.

</td></tr></tbody>
</table>    3.  Select **Save and continue** to go to the next step.

    4.  Select input data from past similar changes.

        Adding tables and fields as the input data sources provides more context to the Now LLM Service to generate the explanation.

        If you turn the **Use similar changes as a data source** toggle button off, past similar changes won’t be included.

        **Note:**

        -   You must have AI Search implemented to retrieve similar changes. For more information on AI Search, see [AI Search](https://www.servicenow.com/docs/access?context=overview-ais&version=australia&pubname=australia-platform-administration&ft:locale=en-US).
        -   The search criteria to retrieve similar changes is based on the conditions set in the Change Requests search source. For information on search source, see [Search Source form](https://www.servicenow.com/docs/access?context=search-source-form-ais&version=australia&pubname=australia-platform-administration&ft:locale=en-US).
        ![Similar changes for change risk explanation](../image/itsm-now-assist-change-similar-changes.png)

        The **Short description** field is available by default. You can edit or remove the following fields:

        -   Description
        -   Risk
        -   Implementation plan
        You can also add new fields and descriptions for them by selecting **+New base input field**.

        **Important:** If you add a new field with the same name as an existing field, the name and description of the new field will override the description of the existing field.

        The Incident Caused by Change input table is available by default as an additional data source. In this table, the **Short description** field is read only. You can edit or remove the **Description** and **Priority** fields.

        **Important:** When you add a new related table with the same name as an existing table, the fields and the descriptions in the new table will override the fields and descriptions in the existing table.

        ![Similar changes additional input](../image/itsm-now-assist-similar-changes-additional-input.png)

    5.  Select **Save and continue** to go to the next step.

6.  Test the output.

    1.  Select the change record in the Test output section, and test the prompt response output format by selecting **Run Test**.

        If the result shows that risk isn’t calculated for the change request, then the prompt created isn’t effective. If the output displays a prompt response, then the LLM has used the configurations in the previous steps and has passed them to the prompt to create the explanation.

        ![Testing the output in change request risk explanation](../image/itsm-now-assist-test-output.png)

    2.  Select **Save and Continue** to go to the next step.

7.  Define availability.

    Define how the skill will be available to users.

    1.  Configure the skill to be always available to users, or select the conditions that must be met before the skill is available.

        Selecting **Customize skill availability** displays a condition builder to filter the data further.

    2.  Select **Save and continue** to go to the next step.

8.  Select display.

    Configure where to display the Change request risk explanation skill.

    1.  Select either **In-product**, or **Now Assist panel**.

        -   **In-product**: When selected, Now Assist skills are displayed in all ITSM products \(on forms and in workspaces\).

            For the skills that appear in-product, select the down arrow to identify the roles that can use the skill.

        -   **Now Assist panel**: When selected, Now Assist skills are available in the Now Assist panel.

            If you don't see this option, you must activate the Now Assist panel. For more information, see [Activate the Now Assist panel standard chat](https://www.servicenow.com/docs/access?context=activate-now-assist-panel&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

            For the skills that appear in the Now Assist panel, select the down arrow to identify the roles that can use the skill.

    2.  Select **Save and continue** to go to the next step.

9.  Review and activate.

    Review your choices and select **Activate** to complete the skill customization.


