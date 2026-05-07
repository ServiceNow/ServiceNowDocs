---
title: Customize the Now Assist for IT Service Management \(ITSM\) change request summarization skill
description: Enhance the efficiency of the change request summarization skill by customizing it with different inputs and prompts using the skill configuration guided setup.
locale: en-US
release: australia
product: Now Assist for IT Service Management \(ITSM\)
classification: now-assist-for-it-service-management-itsm
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Configure, Now Assist for IT Service Management \(ITSM\), IT Service Management]
---

# Customize the Now Assist for IT Service Management \(ITSM\) change request summarization skill

Enhance the efficiency of the change request summarization skill by customizing it with different inputs and prompts using the skill configuration guided setup.

## About this task

You can modify and edit prompts in the Now Assist Skill Kit \(NASK\) by selecting the **Edit prompt in Now Assist Skill Kit** option in step 6.

## Before you begin

Role required: sn\_nowassist\_admin.nsa\_admin

You need the sn\_skill\_builder.admin role to customize the prompt in the Now Assist Skill Kit \(NASK\).

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Skills**.

2.  In the **Technology** feature group, select **ITSM** from the product list.

3.  Activate and copy the change request summarization skill for customization.

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

    Configure the base input table and fields that are used as the source to generate a response for the input template states - Assess, Authorize &amp; Scheduled, Implement &amp; Review, Closed.

    Each skill relies on a base input table and input fields with descriptions to provide context for the Now LLM Service to generate a response.

    Select only those related tables that are offered with the base system as part of the input data.

    1.  Add base input table fields.

        The following base input fields values are available by default:

        -   Short description
        -   Description
        -   Work notes
        -   Additional comments
        -   Risk
        -   Impact
        -   Justification
        -   Implementation plan
        -   Risk and impact analysis
        -   Test plan
        -   Backout plan
        -   Close code
        -   Close notes
        -   Service offering
        -   State
        -   Conflict status
        -   Type
        You can edit or remove the Work notes, Additional comments, Risk, Impact, Justification, Implementation plan, Risk and impact analysis, Test plan, Backout plan, Close code, Close notes, Service offering, State, Conflict status, and Type fields. You can also add new fields and descriptions for them by selecting **+New base input field**.

        **Important:** If you add a new field with the same name as an existing field, the name and description of the new field will override the description of the existing field.

        ![Customizing the change request summarization skill with input data](../image/now-assist-cust-change-summarization-1.png)

    2.  Add rule conditions to determine when the input template is used.

        By default, record state determines which input template the LLM uses.

    3.  Add additional input data sources.

        The data sources could include related tables, activity streams, and relationships. The Change Risk Details, Conflict, Applied Change Policy, Impacted CIs, and Affected CIs related input tables are available by default. You can edit these tables or add new related tables, activity streams, or relationships by selecting **+New data source** and then selecting the desired option.

        ![Add new data source](../image/now-assist-cust-change-summarization-2.png)

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

</td></tr><tr><td>

Activity: Email

</td><td>

Email that is attached to the change request in the change summarization.

</td></tr><tr><td>

Activity: Attachment

</td><td>

Attachment added to the change request.

</td></tr></tbody>
</table>    4.  Select **Save and continue** to go to the next step.

6.  Customize the prompt.

    Review and test the prompt for each input template configuration.

<table id="choicetable_ipx_pkr_2hc"><thead><tr><th align="left" id="d347426e436">

To

</th><th align="left" id="d347426e439">

Do this

</th></tr></thead><tbody><tr><td id="d347426e445">

**Evaluate a prompt for each input template**

</td><td>

1.  Select a change record in any of the states such as:
    -   Assess
    -   Authorize &amp; Scheduled
    -   Implement &amp; Review
    -   Closed
2.  Select **Run Test**. ![Evaluate prompt output for the change request summarization skill](../image/now-assist-cust-prompt-change-summ-1.png)
Review and test the prompt for each input template configuration and make sure it meets your expectations.The prompt response is shown. You can make changes to the change state selections and retest as needed.

</td></tr><tr><td id="d347426e484">

**Edit the prompt in the Now Assist Skill Kit and then test the prompt**

</td><td>

1.  Select **Edit prompt in Now Assist Skill Kit**.
2.  Select **Go to Now Assist Skill Kit**. ![Edit prompt in Now Assist Skill Kit](../image/now-assist-cust-promt-change-summarization-2.png)
3.  In the **Skill contents** pane, select the **Edit Skill Input** icon and add any inputs that you'd like to add to the prompt. ![Edit skill input in Now Assist Skill Kit](../image/now-assist-cust-prompt-change-summ-3.png)
4.  In the **Prompt** screen, clone the required prompt and save it. ![Clone and edit prompt in Now Assist Skill Kit](../image/now-assist-cust-prompt-change-summ-4.png)
5.  Select **Run test**.

The prompt displays in the Test prompt screen.

</td></tr></tbody>
</table>7.  Define availability.

    Define how the skill will be available to users.

    1.  Configure the skill to be always available to users, or select the conditions that must be met before the skill is available.

        Selecting **Customize skill availability** displays a condition builder to filter the data further.

    2.  Select **Save and continue** to go to the next step.

8.  Define access.

    1.  Add access control lists \(ACLs\) to determine who has access to this skill in the User access - Access Control List \(ACL\) section by selecting the **Edit ACL** icon.

        Roles selected here will be available in the ‘Select display’ step.

    2.  Define which data and resources the role can access in the **Role restrictions to skill** field.

9.  Select display.

    Configure where to display the change request summarization skill.

    1.  Enable either the **In-product desktop**, or **Now Assist panel** option.

        -   **In-product desktop**: When selected, Now Assist skills are displayed in all ITSM products \(on forms and in workspaces\).

            For the skills that appear in-product, select the down arrow to identify the roles that can use the skill.

        -   **Now Assist panel**: When selected, Now Assist skills are available in the Now Assist panel.

            If you don't see this option, you must activate the Now Assist panel. For more information, see [Activate the Now Assist panel standard chat](https://www.servicenow.com/docs/access?context=activate-now-assist-panel&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

            For the skills that appear in the Now Assist panel, select the down arrow to identify the roles that can use the skill.

    2.  Select **Save and continue** to go to the next step.

10. Review and activate.

    Review your choices and select **Activate** to complete the skill customization.


