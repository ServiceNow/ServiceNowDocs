---
title: Customize a ServiceNow Otto for Supplier Lifecycle Operations \(SLO\) skill for Case summarization
description: If you have the admin role, you can customize a ServiceNow Otto for Supplier Lifecycle Operations \(SLO\) skill. By customizing a skill, supplier managers can use the generative AI skills in Source-to-Pay Workspace and in Core UI.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/supplier-lifecycle-operations/now-assist-slo-cust-skill.html
release: australia
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
keywords: [generative AI, gen AI, genai, artificial intelligence, Case summarization, Now Assist Admin, input template]
breadcrumb: [Configure, ServiceNow Otto for SLO, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Customize a ServiceNow Otto for Supplier Lifecycle Operations \(SLO\) skill for Case summarization

If you have the admin role, you can customize a ServiceNow Otto for Supplier Lifecycle Operations \(SLO\) skill. By customizing a skill, supplier managers can use the generative AI skills in Source-to-Pay Workspace and in Core UI.

## Before you begin

Role required: admin

## About this task

From the AI Admin Hub, you can select the input table, related records, and fields for each input template of the Case summarization skill. You can then configure the prompt headers to include them in the general summary.

## Procedure

1.  Navigate to **All** &gt; **AI Admin Hub** and select the **AI Skills** tab.

2.  In the **Finance and Supply Chain** workflow group, select **Supplier Lifecycle Operations** to view the AI skills for the ServiceNow Otto for SLO features.

3.  Create a copy of an active skill and customize the input fields.

    1.  From the listed active skills, locate the skill that you'd like to copy and select the More actions icon \(\[Omitted image "more\_vertical\_icon.png"\] Alt text: More actions icon.\).

    2.  Select **Make copy**.

        A guided setup leads you through the configuration of the general details, input, prompt, availability, display, review, and activation of the customized skill. If you complete the entire walk-through, the skill is activated.

4.  In the General details step, fill in the fields.

    For information about the inputs for each skill, see [Configure skill input for ServiceNow Otto for Supplier Lifecycle Operations \(SLO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/now-assist-slo-skill-input-triggers.md).

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

6.  Customize the prompt output.

    Review and test the prompt for each input template configuration. You can edit the prompt by adding new predefined sections and reordering them, as needed.

7.  Define how the skill is available to your users.

    1.  Configure the skill to be always available to users, or select conditions that must be met before the skill is available.

        Selecting **Customize skill availability** displays a condition builder to filter the data further.

    2.  Select **Save and continue** to go to the next step.

8.  Define who can use the skill using Access control lists \(ACLs\).

    Roles selected here will be available in the ‘Select display’ step.

9.  Configure where to display the supplier case summarization.

    1.  Select the **In-product desktop** **Display** toggle to display the AI skill on forms and workspaces.

        For the skills that appear in the in-product desktop, select the down arrow to identify the roles that can use the skill.

    2.  Select the **ServiceNow Otto panel** **Display** toggle to activate the AI skill in the ServiceNow Otto panel.

    3.  Select **Save and continue** to go to the next step.

10. Review and activate the skill.

    Review your choices and select **Activate** to complete the skill customization.

    You can select **Summarize** in a record to generate the summary for the supplier case.


**Related topics**  


[Customize ServiceNow Otto for Supplier Lifecycle Operations \(SLO\) to use the Virtual Agent chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/cust-now-assist-slo-va.md)

[Configure skill input for ServiceNow Otto for Supplier Lifecycle Operations \(SLO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/now-assist-slo-skill-input-triggers.md)

