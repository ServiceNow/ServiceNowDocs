---
title: Customize supplier summarization for fulfillers skill
description: If you have the admin role, you can customize the supplier summarization for fulfillers skill so that fulfillers can use the generative AI skills in Source-to-Pay Workspace to view relevant supplier information.
locale: en-US
release: australia
product: Now Assist for FSC Common
classification: now-assist-for-fsc-common
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Configure, Features, Now Assist for Finance and Supply Chain, Finance and Supply Chain]
---

# Customize supplier summarization for fulfillers skill

If you have the admin role, you can customize the supplier summarization for fulfillers skill so that fulfillers can use the generative AI skills in Source-to-Pay Workspace to view relevant supplier information.

## Before you begin

**Important:** This Now Assist skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

Role required: admin

## About this task

From the Now Assist Admin console, you can select the input table, related records, and fields for each input template of the Summarization for fulfillers skill, and then configure the prompt headers to include in the general summary.

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Skills** to access the **Now Assist Skills** tab of the Now Assist Admin console.

2.  In the **Finance and Supply Chain** workflow group, select **Common Finance and Supply Chain features** to view the skills for the Now Assist for Common Finance and Supply Chain features.

3.  Create a copy of a skill and customize the input fields.

    1.  On the Supplier summarization for fulfillers feature card, select the More actions icon \(![More actions icon.](../image/more_vertical_icon.png)\).

    2.  Select **Make a copy**.

        A guided setup leads you through the configuration of the general details, input, prompt, availability, display, review, and activation of the customized skill. If you complete the entire walk-through, the skill is activated.

4.  In the General details step, fill in the fields.

    For information about the inputs and triggers for each skill, see [Skill inputs for Supplier summarization for fulfillers skill](../reference/input-triggers-na-fsc-supplier.md).

    1.  Enter a name and description for the skill.

    2.  Select **Save and continue** to go to the next step.

5.  View the input data for each skill, such as the base input fields and related lists for the different input templates.

    Configure the base input table fields and related lists for the different input templates for the skill.

    Each skill relies on a base input table and input fields with descriptions to provide context for the Now LLM Service to generate a response.

    Select only those related tables that are offered as the base system, as part of the input data.

    1.  For each input template state, select **+New base input field** and configure the base input table fields.

        Add multiple base input fields, as necessary.

        ![Choose input screen](../../source-to-pay-operations/image/na-choose-input-fsc-supplier.png "Choose input step")

        The following table lists the base input table fields and descriptions, including a relevant example.

<table id="table_c53_vp5_dbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Base input field

</td><td>

Field in the Supplier table whose value this skill uses in its response.

 For example, `Legal name`.

</td></tr><tr><td>

Field description

</td><td>

Description of the base input field value.

 For example, `Legal name of the supplier`.

</td></tr></tbody>
</table>    2.  For each input template state, configure the rule conditions by using the condition builder to filter the data.

        The rule conditions determine when the input template is used. By default, the record state determines the input template that the Now LLM Service uses.

        You can build the condition out further by selecting **+New condition set** and configuring additional parameters.

    3.  For each input template state, select **+New data source** to configure the additional related table and activity stream data, as needed.

        You can add input data sources like related tables, activity streams and relationships to provide more context to the Now LLM Service. You can also add rule conditions to these additional data sources.

        You can also add the rule conditions to these additional data sources.

        The selection of the related table fields may have a direct impact on the quality of the corresponding prompt header. For example, if a prompt header requires a specific field from the related table, but that field isn’t selected as input, the summary for that prompt header will contain missing information. For example, as a base case, you see one related table, such as Service level agreement \(SLA\), that includes all the required fields and filtering conditions for the prompt header. The SLA prompt header is preselected to help you understand how the related table, its fields, and the prompt header work together to produce a summary. You can use the SLA as a reference to configure the other related tables to determine which fields to select and which description adds the requirements of their respective prompt headers. Apply any additional conditions to filter the data further.

    4.  Select **Save and continue** to go to the next step.

6.  Customize prompt output.

    Select **Active** and **Save and continue**.

    The following prompt sections will be displayed while using the skill:

    -   **Key Supplier Details**
    -   **Procurement Specialist specific details**
    -   **AP specialist specific details**
    -   **Supplier Manager specific details**
7.  Define how the skill is available to your users.

    1.  Configure the skill to be always available to users, or select conditions that must be met before the skill is available.

        Selecting **Customize skill availability** displays a condition builder to filter the data further.

    2.  Select **Save and continue** to go to the next step.

8.  Define who can access this skill.

    1.  Edit the Access control lists \(ACLs\) to determine who has access to this skill \(optional\).

    2.  Select **Save and continue** to go to the next step.

9.  Review and activate the skill.

    Review your choices and select **Activate** to complete the skill customization.

    The fulfillers having the sn\_fsc\_genai.now\_assist\_fulfiller role can now select **Summarize** for a supplier record in the Source-to-Pay Workspace to generate the summary of the supplier.


-   **[Skill inputs for Supplier summarization for fulfillers skill](../reference/input-triggers-na-fsc-supplier.md)**  
You can configure some of the inputs for a generative AI skill. Inputs permit you to determine how and when a skill is used.

**Parent Topic:**[Configuring Now Assist for Common Finance and Supply Chain features](configure-now-assist-fsc.md)

**Related topics**  


[Customize a Now Assist for Common Finance and Supply Chain features skill](cust-now-assist-fsc-skill.md)

