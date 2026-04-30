---
title: Customize a Now Assist for Common Finance and Supply Chain features skill
description: If you have the admin role, you can customize a Now Assist for Sourcing and Procurement Operations \(SPO\) skill so that fulfillers and requesters can use the generative AI skills in Source-to-Pay Workspace, Shopping Hub, and in Core UI.
locale: en-US
release: yokohama
product: Now Assist for FSC Common
classification: now-assist-for-fsc-common
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 6
breadcrumb: [Configure Now Assist for Common FSC features, Now Assist for Common Finance and Supply Chain features, Now Assist for Finance and Supply Chain, Finance and Supply Chain]
---

# Customize a Now Assist for Common Finance and Supply Chain features skill

If you have the admin role, you can customize a Now Assist for Sourcing and Procurement Operations \(SPO\) skill so that fulfillers and requesters can use the generative AI skills in Source-to-Pay Workspace, Shopping Hub, and in Core UI.

## Before you begin

Role required: admin

## About this task

From the Now Assist Admin console, you can select the input table, related records, and fields for each input template of the Summarization for fulfillers skill, and then configure the prompt headers to include in the general summary.

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Skills** to access the **Now Assist Skills** tab of the Now Assist Admin console.

2.  In the **Finance and Supply Chain** workflow group, select **Common Finance and Supply Chain features** to view the skills for the Now Assist for Common Finance and Supply Chain features.

3.  Create a copy of a skill and customize the input fields.

    1.  On the Purchase order summarization for fulfillers feature card, select the More actions icon \(![More actions icon.](../image/more_vertical_icon.png)\).

    2.  Select **Make a copy**.

        A guided setup leads you through the configuration of the general details, input, prompt, availability, display, review, and activation of the customized skill. If you complete the entire walk-through, the skill is activated.

4.  In the General details step, fill in the fields.

    For information about the inputs and triggers for each skill, see [Skill inputs for Now Assist for Sourcing and Procurement Operations \(SPO\)](../reference/input-triggers-now-assist-spo.md).

    1.  Enter a name and description for the skill.

    2.  Select **Save and continue** to go to the next step.

5.  View the input data for each skill, such as the base input fields and related lists for the different input templates.

    Configure the base input table fields and related lists for the different input templates for the skill.

    Each skill relies on a base input table and input fields with descriptions to provide context for the Now LLM Service to generate a response.

    Select only those related tables that are offered as the base system, as part of the input data.

    1.  For each input template state, select **+New base input field** and configure the base input table fields.

        Add multiple base input fields, as necessary.

        ![Choose input screen.](../image/na-choose-input-fsc.png "Choose input step")

        The following table lists the base input table fields and descriptions, including a relevant example.

<table id="table_c53_vp5_dbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Base input field

</td><td>

Field in the Purchase Order table whose value this skill uses in its response.

 For example, `Order type`.

</td></tr><tr><td>

Field description

</td><td>

Description of the base input field value.

 For example, `Type of the purchase order`.

</td></tr></tbody>
</table>    2.  For each input template state, configure the rule conditions by using the condition builder to filter the data.

        The rule conditions determine when the input template is used. By default, the record state determines the input template that the Now LLM Service uses.

        You can build the condition out further by selecting **+New condition set** and configuring additional parameters.

    3.  For each input template state, select **+New data source** to configure the additional related table and activity stream data, as needed.

        You can add input data sources like related tables, activity streams and relationships to provide more context to the Now LLM Service. You can also add rule conditions to these additional data sources.

        You can also add the rule conditions to these additional data sources.

        The selection of the related table fields may have a direct impact on the quality of the corresponding prompt header. For example, if a prompt header requires a specific field from the related table, but that field isn’t selected as input, the summary for that prompt header will contain missing information. For example, as a base case, you see one related table, such as Service level agreement \(SLA\), that includes all the required fields and filtering conditions for the prompt header. The SLA prompt header is preselected to help you understand how the related table, its fields, and the prompt header work together to produce a summary. You can use the SLA as a reference to configure the other related tables to determine which fields to select and which description adds the requirements of their respective prompt headers. Apply any additional conditions to filter the data further.

    4.  Select **Save and continue** to go to the next step.

6.  Customize the prompt.

    Review and test the prompt for each input template configuration. You can edit the prompt by adding new predefined sections and reordering them, as needed.

    1.  For each input template state, select the prompt sections from the list of available sections to include in the generated summary.

        To add a section, you must configure the relevant input data prior to this step.

        The available prompt sections that you can select:

        -   **Overview for PO**
        -   **Actions completed for PO**
        -   **Next steps for PO**
        The following table lists the mandatory prompt headers.

<table id="table_av3_xhw_2bc"><thead><tr><th>

Input template state

</th><th>

Mandatory prompt header

</th></tr></thead><tbody><tr><td>

Open

</td><td>

-   Overview for PO
-   Actions completed for PO
-   Next steps for PO


</td></tr><tr><td>

Closed

</td><td>

-   Overview for PO
-   Actions completed for PO


</td></tr></tbody>
</table>    2.  Select **Save** to continue to the test response.

    3.  Select a record in the Test response section, and test the prompt response output format by selecting **Run Test**.

    4.  Select **Save and continue** to go to the next step.

7.  Define how the skill is available to your users.

    1.  Configure the skill to be always available to users, or select conditions that must be met before the skill is available.

        Selecting **Customize skill availability** displays a condition builder to filter the data further.

    2.  Select **Save and continue** to go to the next step.

8.  Configure where to display the record summarization.

    1.  Select either **In-product**, or **Now Assist panel**.

        -   **In-product desktop**: When selected, the customized Purchase order summarization for fulfillers skill is shown on the forms and workspaces in all Common Finance &amp; Supply Chain features products.

            For the skills that appear in-product, select the down arrow to identify the roles that can use the skill.

        -   **Now Assist panel**: When selected, the Now Assist skills are available in the Now Assist panel.

            Now Assist skills are available in the Now Assist panel. Turn on multi-language support for user-entered text with Dynamic Translation in Now Assist applications. For more information, see [Configure multilingual service for Now Assist applications](https://www.servicenow.com/docs/access?context=enable-dynamic-translation-for-now-assist-applications&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US).

            **Note:** If you don't see this option, you must activate the Now Assist panel. For more information, see [Activate Now Assist panel standard chat](https://www.servicenow.com/docs/access?context=activate-now-assist-panel&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

            For the skills that appear in the Now Assist panel, select the down arrow to identify the roles that can use the skill.

    2.  Select **Save and continue** to go to the next step.

9.  Review and activate the skill.

    Review your choices and select **Activate** to complete the skill customization.

    The fulfillers having the sn\_fsc\_genai.now\_assist\_fulfiller role can now select **Summarize** for a purchase order record in the Source-to-Pay Workspace to generate the summary for the purchase order.


**Parent Topic:**[Configuring Now Assist for Common Finance and Supply Chain features](configure-now-assist-fsc.md)

**Related topics**  


[Skill inputs for Now Assist for Common Finance and Supply Chain features](../reference/input-triggers-now-assist-fsc.md)

[Customize supplier summarization for fulfillers skill](cust-na-fsc-supplier-skill.md)

